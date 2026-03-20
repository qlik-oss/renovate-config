# renovate-config

Qlik OSS configurations for [renovate](https://renovatebot.com/).

Documentation for all options: https://renovatebot.com/docs/configuration-options/

## Usage

Use repository-based presets:

- `github>qlik-oss/renovate-config`
- `github>qlik-oss/renovate-config:groupMinorPatch`

## Exposed presets

### `github>qlik-oss/renovate-config`

Base Qlik OSS preset.

- Extends common Renovate defaults and scheduling preferences
- Adds monorepo grouping rules via:
  - `picassoMono`
  - `nebulaMono`
  - `awMono`
  - `groupMinorPatch`

### `github>qlik-oss/renovate-config:picassoMono`

Groups `picasso.js` ecosystem dependencies into one PR group (`picasso.js packages`).

### `github>qlik-oss/renovate-config:nebulaMono`

Groups `nebula.js` ecosystem dependencies into one PR group (`nebula.js packages`).

### `github>qlik-oss/renovate-config:awMono`

Groups `after-work.js` ecosystem dependencies into one PR group (`@after-work.js packages`).

### `github>qlik-oss/renovate-config:groupMinorPatch`

Groups `minor`/`patch`/`pin` updates into one PR group (`minor and patch`) and enables automerge for that group.

## Matching strategy

Monorepo presets use `matchSourceUrls` as primary matching with `matchPackageNames` fallback to keep grouping reliable when source metadata is missing.

## Rules

Most of the rules are defaults defined here: https://github.com/renovatebot/presets/tree/master/packages/renovate-config-default
