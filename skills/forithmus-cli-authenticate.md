---
name: Authenticate the Forithmus CLI (device flow)
description: Complete the browser-based device authorization used by `forithmus login` — start a CLI session, direct the user to approve it, poll until complete, and store the returned tokens.
api: openapi/forithmus-openapi-original.json
api_base_url: https://research.forithmus.com/api
operations:
  - create_cli_session_auth_cli_session_post
  - poll_cli_session_auth_cli_session__session_id__get
  - complete_cli_session_auth_cli_session__session_id__complete_post
  - refresh_auth_refresh_post
---

# Authenticate the Forithmus CLI (device flow)

The `forithmus` CLI (`pip install forithmus`) authenticates without pasting passwords into the terminal, using a browser-approved device session against `https://research.forithmus.com/api`.

## Steps

1. **Start a session** — `POST /auth/cli-session` (`create_cli_session_auth_cli_session_post`) returns a `session_id` and an approval URL on the Research Hub.
2. **Prompt approval** — open the approval URL in the user's browser; they sign in (email/password or Google) and approve the session. The browser side calls `POST /auth/cli-session/{session_id}/complete` (`complete_cli_session_auth_cli_session__session_id__complete_post`).
3. **Poll** — `GET /auth/cli-session/{session_id}` (`poll_cli_session_auth_cli_session__session_id__get`) on an interval until it reports completion and returns the access + refresh tokens.
4. **Store & refresh** — persist the tokens (the CLI writes them to its local credential file). Refresh with `POST /auth/refresh` (`refresh_auth_refresh_post`) when the access token expires.

## Rules

- Override the API host with `FORITHMUS_API_URL` if not using production.
- Poll politely (a few seconds between calls); stop on completion or expiry.
- All subsequent API calls send `Authorization: Bearer <access_token>`. See `authentication/forithmus-authentication.yml` and `cli/forithmus-cli.yml`.
