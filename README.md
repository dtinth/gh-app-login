# gh-app-login

A simple, single file [GitHub CLI Extension](https://docs.github.com/en/github-cli/github-cli/creating-github-cli-extensions) that authenticates the `gh` CLI a GitHub App installation using a private key.

When you run `gh app-login`, it will [generate an installation access token](https://docs.github.com/en/enterprise-cloud@latest/apps/creating-github-apps/authenticating-with-a-github-app/generating-an-installation-access-token-for-a-github-app) with the provided private key, and pipes it into `gh auth login --with-token`, letting the agent perform actions as a GitHub App installation.

## Prerequisites

- Deno
- Mac or Linux

## Installation

```sh
gh extension install dtinth/gh-app-login
```

## Usage

```sh
gh app-login --app-id <id> --private-key <path/to/key.pem>

# If your app has multiple installations, specify which one:
gh app-login --app-id <id> --private-key <path/to/key.pem> --installation <installation-id>
```
