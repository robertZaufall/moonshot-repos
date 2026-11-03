# moonshot-repos

Read [shared infrastructure](../infrastructure/AGENTS.md), [project note](../infrastructure/moonshot-repos.md), and [atlas runbook](../repository-atlases/AGENTS.md).

## Ownership and catalog rules

Publish only to robertZaufall/moonshot-repos, main branch. Discover public repositories owned by `moonshotai`; non-fork, non-archived, more than 200 stars, pushed within three calendar months. All qualifying repositories appear in purpose clusters; the traction table shows 25. Clusters: Coding Agents, Inference & Kernels, Models & Evaluation.

## Maintenance

Inspect status and origin; fetch and pull safely before editing. Investigate upstream README, topics, activity and eligibility. Edit update_stats.py for membership/classification; never hand-edit generated rows. Run `python3 -m py_compile update_stats.py`, `python3 update_stats.py`, and `git diff --check`. Preserve stats_history.json for 30-day traction deltas. Review complete API results and rerun generation before publication. Stage intended files, commit, integrate upstream without force, push and verify SHA parity.

## Hosting

GitHub Actions refreshes daily at 06:00 UTC and deploys index.html/favicon.svg to Pages. Local preview: `python3 -m http.server 8000`. API auth: GITHUB_TOKEN, GH_TOKEN, or existing gh CLI credentials. Never commit secrets.

Cloudflare proxy: cloudflare/worker.js and wrangler.jsonc; exact /moonshot and /moonshot/* routes. Canonical https://glaubi.net/moonshot/. From cloudflare/, verify Wrangler auth, dry-run, deploy, then check bare redirect, slash HTML, favicon and missing-path 404. Preserve other routes. Rollback via a reviewed prior revision; retain history.
