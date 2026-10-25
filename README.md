# Homebrew tap for Stackurity

```sh
brew install stackurity/tap/stackurity
stackurity --version
```

This installs the `stackurity` binary (CLI, agent and server in one) for macOS and Linux, from the signed [GitHub releases](https://github.com/stackurity/stackurity/releases). Typical use on a laptop or CI machine:

```sh
export STACKURITY_SERVER=https://stackurity.example.com
export STACKURITY_TOKEN=...   # a collector token
stackurity scan . --fail-on critical
```

The formula is regenerated within the hour after each release by [`update.yml`](.github/workflows/update.yml): it verifies the release's Sigstore-signed checksums, then installs and tests the formula on macOS and Linux before committing it.

For servers, use the Docker image or the Helm chart instead; see the [installation guide](https://github.com/stackurity/stackurity/blob/main/docs/install.md).
