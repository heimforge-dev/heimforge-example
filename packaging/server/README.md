# Server packaging

Generated local server-side ZIPs are written to `artifacts/packages/` by `./scripts/package.sh`:

- ServerCore
- ServerPack

Membership is defined by `suite.config.json` and validated to exclude client-only projects.
