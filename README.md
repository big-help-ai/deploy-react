# Deploy React Action

This GitHub Action builds and deploys a React website to Amazon S3. It handles checking out both the app repository and a core React repository, building the application, and deploying it to S3.

## Inputs

| Input                   | Description                        | Required | Default          |
| ----------------------- | ---------------------------------- | -------- | ---------------- |
| `organization`          | GitHub organization name           | Yes      | -                |
| `project`               | Project name                       | Yes      | -                |
| `gh-token`              | GitHub token for repository access | Yes      | -                |
| `ref`                   | Git reference to checkout          | Yes      | `main`           |
| `aws-access-key-id`     | AWS Access Key ID                  | Yes      | -                |
| `aws-secret-access-key` | AWS Secret Access Key              | Yes      | -                |
| `s3-bucket`             | S3 bucket name                     | Yes      | `cdn.bighelp.ai` |

## Features

- Checks out both the app repository and react-core repository
- Sets up Node.js environment
- Installs dependencies
- Builds the React application using Vite
- Deploys the built files to S3 with public-read access
