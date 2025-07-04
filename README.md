# Deploy Workflows

A centralized deployment system that manages automated deployments across multiple repositories using GitHub Actions workflows.

## Features

- Sequential deployments based on predefined order
- Multi-environment support (DEV, SIT, UAT, PROD)
- Status tracking and error handling

## Prerequisites

- `GH_TOKEN` - Place your PAT token with required permissions for workflow operations in actions secrets

## Usage

Trigger the pre-deploy workflow with:

```json
{
  "id": "unique_deployment_id",
  "environment": "DEV",
  "repos": [
    {
      "repo_name": "foo-frontend",
      "commit_hash": "abc123"
    },
    {
      "repo_name": "bar-frontend",
      "commit_hash": "def456"
    },
    {
      "repo_name": "baz-backend",
      "commit_hash": "ghi789"
    }
  ]
}
```