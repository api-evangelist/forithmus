---
name: Join a challenge and submit a solution
description: Authenticate, discover an open Forithmus medical-imaging challenge, join it, submit a Docker container (or prediction file) to a phase, and read the leaderboard.
api: openapi/forithmus-openapi-original.json
api_base_url: https://research.forithmus.com/api
operations:
  - login_auth_login_post
  - list_challenges_challenges_get
  - get_challenge_challenges__slug__get
  - list_phases_challenges__slug__phases_get
  - join_challenge_challenges__slug__members_join_post
  - docker_upload_url_challenges__slug__submissions_docker_upload_url_post
  - docker_upload_complete_challenges__slug__submissions_docker_upload_complete_post
  - upload_file_submission_challenges__slug__submissions_upload_file_post
  - list_submissions_challenges__slug__submissions_get
  - get_leaderboard_challenges__slug__leaderboard_get
---

# Join a challenge and submit a solution

All requests go to `https://research.forithmus.com/api`. Authenticate with a Bearer JWT and send it as `Authorization: Bearer <access_token>` on every call.

## Steps

1. **Authenticate** — `POST /auth/login` (`login_auth_login_post`) with email + password to obtain an access token and refresh token. When the token expires, call `POST /auth/refresh` (`refresh_auth_refresh_post`). (Interactive/CLI users authenticate with the device flow in the `forithmus-cli-authenticate` skill instead.)
2. **Discover challenges** — `GET /challenges` (`list_challenges_challenges_get`). The response is an offset-paginated envelope `{items, total, limit, offset}`; page with `limit` and `offset`, and narrow with `q`/`search`/`sort`.
3. **Inspect one** — `GET /challenges/{slug}` (`get_challenge_challenges__slug__get`) and `GET /challenges/{slug}/phases` (`list_phases_challenges__slug__phases_get`) to find the active phase and its submission rules (`max_submissions_per_user`, `accepting_submissions`, deadlines).
4. **Join** — `POST /challenges/{slug}/members/join` (`join_challenge_challenges__slug__members_join_post`). If the challenge sets `require_approval`, membership stays pending until a host approves.
5. **Submit** — for a container: `POST /challenges/{slug}/submissions/docker-upload-url` (`docker_upload_url_challenges__slug__submissions_docker_upload_url_post`) to get a registry/upload target, push the image, then `POST /challenges/{slug}/submissions/docker-upload-complete` (`docker_upload_complete_challenges__slug__submissions_docker_upload_complete_post`). For a prediction file instead: `POST /challenges/{slug}/submissions/upload-file` (`upload_file_submission_challenges__slug__submissions_upload_file_post`).
6. **Track** — `GET /challenges/{slug}/submissions` (`list_submissions_challenges__slug__submissions_get`) for status, and `GET /challenges/{slug}/leaderboard` (`get_leaderboard_challenges__slug__leaderboard_get`) for scores.

## Rules

- **Auth:** Bearer JWT; refresh rather than re-login. See `authentication/forithmus-authentication.yml`.
- **Pagination:** offset (`limit`/`offset`); read `total` to know when to stop. See `conventions/forithmus-conventions.yml`.
- **Idempotency:** none — the API has no `Idempotency-Key`. Do not blindly retry a submission POST; check `list_submissions` first.
- **Errors:** FastAPI `{"detail": ...}`; `422` returns a `detail[]` array of `{loc,msg,type}`. `402` means insufficient credits/compute. See `errors/forithmus-problem-types.yml`.
