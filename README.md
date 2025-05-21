# sensa-cloud-init

This repository manages a `cloud-init.yaml` configuration file for cloud-init provisioning.

## Features

- Stores a version-controlled `cloud-init.yaml` for cloud instance initialization.
- Automatically generates a base64-encoded version of `cloud-init.yaml` (`cloud-init.yaml.b64`) using a GitHub Actions workflow on every change.
- Ensures the encoded file is always up to date for use in cloud platforms or scripts that require base64 input.

## Usage

1. **Edit** `cloud-init.yaml` as needed.
2. **Push** your changes to the repository.
3. The GitHub Actions workflow will:
   - Encode `cloud-init.yaml` to base64.
   - Commit and push the updated `cloud-init.yaml.b64` if there are changes.

## Files

- `cloud-init.yaml` — Main cloud-init configuration.
- `cloud-init.yaml.b64` — Base64-encoded version (auto-generated).
- `.github/workflows/base64-encode.yaml` — GitHub Actions workflow for encoding.

