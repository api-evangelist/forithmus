---
name: Create and configure a challenge (host)
description: As a challenge host, create a challenge, add a phase, and upload the phase's test data, ground truth, and evaluation container so participants can submit.
api: openapi/forithmus-openapi-original.json
api_base_url: https://research.forithmus.com/api
operations:
  - create_challenge_challenges_post
  - create_phase_challenges__slug__phases_post
  - list_phases_challenges__slug__phases_get
  - get_challenge_stats_challenges__slug__stats_get
---

# Create and configure a challenge (host)

Hosting flow on `https://research.forithmus.com/api`. Requires an authenticated user with host privileges (Bearer JWT).

## Steps

1. **Create the challenge** — `POST /challenges` (`create_challenge_challenges_post`) with title, slug/acronym, category, visibility, and submission limits. The response returns the created challenge (`ChallengeOut`) including its `slug`.
2. **Add a phase** — `POST /challenges/{slug}/phases` (`create_phase_challenges__slug__phases_post`). List phases any time with `GET /challenges/{slug}/phases` (`list_phases_challenges__slug__phases_get`).
3. **Upload phase assets** (host-only, via the CLI which wraps these endpoints — see `cli/forithmus-cli.yml`):
   - test data — `forithmus upload-data`
   - ground truth — `forithmus upload-gt`
   - evaluation container — `forithmus upload-eval`
4. **Monitor** — `GET /challenges/{slug}/stats` (`get_challenge_stats_challenges__slug__stats_get`) for participant and submission counts.

## Rules

- **Auth:** Bearer JWT with a host role on the challenge; `403` means the role/membership is insufficient.
- **Compute:** submissions run on tiers `cpu-4`, `gpu-t4`, `gpu-l4`, `gpu-v100`, `gpu-a100`; hosts can cap cost via challenge settings (`eval_cost_limit`, `participant_pays_compute`).
- **Errors / pagination / idempotency:** see `errors/forithmus-problem-types.yml` and `conventions/forithmus-conventions.yml` (offset pagination, no idempotency key).
