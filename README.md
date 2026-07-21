# runner

GitHub Actions deploy of [Wei-Shaw/sub2api](https://github.com/Wei-Shaw/sub2api).

## Secrets

| Name | Required | Notes |
|------|----------|-------|
| `PRIVATE_REPO_TOKEN` | yes | PAT with `repo` + `workflow` (push backup + dispatch) |
| `ADMIN_PASSWORD` | yes | Sub2API admin password |
| `JWT_SECRET` | yes | hex 32 |
| `TOTP_ENCRYPTION_KEY` | yes | hex 32 |
| `POSTGRES_PASSWORD` | yes | DB password |
| `CF_TUNNEL_TOKEN` | no | Cloudflare Tunnel token for public URL |

Backup repo: `${owner}/storage` (`data.tar.gz`).

## Run

```bash
gh workflow run run.yml -R <owner>/runner
gh run watch -R <owner>/runner
```
