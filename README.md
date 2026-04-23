# cyoda-platform Homebrew Tap

Homebrew tap for [cyoda-go](https://github.com/cyoda-platform/cyoda-go) — a lightweight Go EDBMS that serves as a digital twin of the Cyoda platform.

## Install

```sh
brew tap cyoda-platform/cyoda-go
brew install cyoda
```

## Formula

`Formula/cyoda.rb` is auto-generated and committed by the cyoda-go
[release workflow](https://github.com/cyoda-platform/cyoda-go/blob/main/.github/workflows/release.yml)
via [GoReleaser](https://goreleaser.com) on each `v*` tag push. Don't edit
manually — the next release would overwrite your changes.

## Verifying a release

Each release artifact is signed via [cosign](https://github.com/sigstore/cosign)
keyless signing (OIDC). To verify a Docker image published alongside the
brew formula:

```sh
cosign verify ghcr.io/cyoda-platform/cyoda:<version> \
  --certificate-identity-regexp="https://github.com/cyoda-platform/cyoda-go" \
  --certificate-oidc-issuer="https://token.actions.githubusercontent.com"
```

## Upstream

Source, issues, releases, and documentation all live at
<https://github.com/cyoda-platform/cyoda-go>.
