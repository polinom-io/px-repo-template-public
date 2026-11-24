# px-repo-template-public
Polinom.io template for public repositories

## Versioning

Releases are managed by [release-please](https://github.com/googleapis/release-please) from [Conventional Commits](https://www.conventionalcommits.org/) on `main`. Merging the release PR tags `vX.Y.Z`, updates `CHANGELOG.md` and `version.txt`, and creates a GitHub Release. Never bump versions or edit `CHANGELOG.md` by hand.

- **First release is `0.1.0`** (`initial-version` in `release-please-config.json`; the manifest starts empty).
- **On 0.x:** `fix:` bumps the patch (0.1.0 → 0.1.1); `feat:` and breaking changes (`feat!:`) bump the minor (0.1.0 → 0.2.0).
- **Going to 1.0.0** is deliberate: add a commit with the footer `Release-As: 1.0.0`.

## Ignored files

`.gitignore` holds only cross-cutting rules (macOS, local Claude Code files, secrets and sensitive data). Stack-specific rules live in `gitignore/<stack>.gitignore`, one file per stack. The secret rules must stay the last block of `.gitignore`: Git applies the last matching rule, so nothing added above them can re-include a secret.

## After creating a repo

1. Set `package-name` for the `"."` package in `release-please-config.json`.
2. If the repo publishes an npm package, change `release-type` from `simple` to `node`.
3. Ask an org owner to give the new repo access to the release GitHub App and to its organization variable and secret. Without them, the `release` workflow fails.
4. Paste the `gitignore/<stack>.gitignore` blocks for the repo's `stack-*` topics into `.gitignore`, above the secret rules, then delete the `gitignore/` folder.
