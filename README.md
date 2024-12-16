# Sample Repository for CI/CD Workflows

This repository demonstrates a CI/CD pipeline with GitHub Actions for:
1. **Creating Releases**: Generates environment-specific builds using YAML configuration files.
2. **Manual Deployment**: Deploys selected releases to target environments.

## Workflows

### 1. Create Release Workflow
- **Trigger**: Push to `main` branch.
- **Artifacts**: Generates and uploads release assets for `dev`, `test`, and `prod`.

### 2. Manual Deployment Workflow
- **Trigger**: Manual workflow dispatch.
- **Input**: Select environment (`dev`, `test`, or `prod`).
- **Deployment**: Downloads and deploys the respective release asset.

## Directory Structure

```plaintext
.github/workflows/
    create-release.yml       # Release workflow
    deploy.yml               # Deployment workflow
configs/
    dev.yaml                 # Dev configuration
    test.yaml                # Test configuration
    prod.yaml                # Prod configuration
src/
    app.py                   # Sample application
README.md                   # This file
