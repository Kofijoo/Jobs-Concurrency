# GitHub Actions Jobs Concurrency

A learning project demonstrating GitHub Actions workflow management, concurrency control, and matrix strategies.

## Overview

This project contains examples of:
- **Concurrency Control**: Workflow execution management with cancel-in-progress
- **Matrix Strategies**: Multi-OS and multi-image job execution
- **Job Dependencies**: Coordinated workflow execution
- **Conditional Deployment**: Branch-based deployment logic
- **Docker Integration**: Container build and deployment pipeline

## Workflows

| File | Purpose |
|------|---------|
| `conc.yml.disable` | Concurrency control with Docker build/deploy |
| `matrix.yml.disable` | Basic matrix strategy across OS and images |
| `advanced-matrix.yml.disable` | Advanced matrix with exclusions and limits |
| `conditional-deploy.yml.disable` | Conditional deployment based on branch |

## Usage

1. Remove `.disable` extension from desired workflow file
2. Uncomment the `on:` trigger section
3. Configure required secrets and variables:
   - `DOCKER_HUB_TOKEN` (secret)
   - `DOCKER_USERNAME` (variable)

## Docker

The included Dockerfile creates an Nginx-based portfolio site container.

## Getting Started

```bash
# Activate a workflow
mv .github/workflows/conc.yml.disable .github/workflows/conc.yml

# Edit triggers
# Uncomment the 'on:' section in the workflow file
```