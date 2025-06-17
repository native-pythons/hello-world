# Hello World Node.js Application

A simple Node.js application that serves "Hello, World!" when accessed.

[![Release, Build and Publish](https://github.com/native-pythons/hello-world/actions/workflows/release-build-publish.yml/badge.svg)](https://github.com/native-pythons/hello-world/actions/workflows/release-build-publish.yml)

## Prerequisites

- Node.js installed on your machine (for local development)
- Docker (for containerized deployment)

## Getting Started

### Running Locally

1. Clone this repository
2. Navigate to the project directory
3. Run the application:

```bash
npm start
```

4. Open your web browser and visit: `http://localhost:3000/`

### Running with Docker

1. Build the Docker image:

```bash
docker build -t hello-world-nodejs .
```

2. Run the Docker container:

```bash
docker run -p 3000:3000 hello-world-nodejs
```

3. Open your web browser and visit: `http://localhost:3000/`

## Files

- `index.js` - The main application file
- `package.json` - Project metadata and dependencies
- `Dockerfile` - Instructions for building the Docker image
- `.dockerignore` - Files to exclude from the Docker image
- `.github/workflows/release-build-publish.yml` - CI/CD workflow for semantic versioning, building and publishing Docker image

## CI/CD Pipeline

This project uses GitHub Actions to automatically:

1. **Semantic Release**: Analyzes commit messages to determine the next version number
2. **Build Docker Image**: Creates a Docker image based on the Dockerfile
3. **Publish to Container Registry**: Pushes the image to GitHub Container Registry (ghcr.io)

### Container Registry

The Docker image is published to GitHub Container Registry and can be pulled using:

```bash
docker pull ghcr.io/native-pythons/hello-world:latest
```

### Commit Message Format

This project follows the [Conventional Commits](https://www.conventionalcommits.org/) specification for commit messages to automate versioning:

- `fix:` - Patch version bump (1.0.0 -> 1.0.1)
- `feat:` - Minor version bump (1.0.0 -> 1.1.0)
- `feat!:` or `fix!:` or any commit with `BREAKING CHANGE:` in the footer - Major version bump (1.0.0 -> 2.0.0)
