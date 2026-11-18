# Minecraft 26.3-JM CDN package

This repository prepares the authorized 26.3-JM browser build for delivery through jsDelivr's npm CDN.

## Publish
1. Create an npm access token with permission to publish packages.
2. In this GitHub repository, open **Settings → Secrets and variables → Actions**.
3. Add a repository secret named `NPM_TOKEN` containing that token.
4. Open **Actions → Build and publish Minecraft CDN package → Run workflow**.

The workflow downloads the pinned upstream release, verifies its SHA-256 checksum, splits it into 10 MiB binary chunks, and publishes the package `@tonybalony76/njmfdqbes-26.3` as version `1.0.0`.

The chunks will be served from:
`https://cdn.jsdelivr.net/npm/@tonybalony76/njmfdqbes-26.3@1.0.0/chunks/part-000.bin`

The package is not published until the workflow is run with a valid `NPM_TOKEN`.
