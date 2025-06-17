# Hello World Node.js Application

A simple Node.js application that serves "Hello, World!" when accessed.

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
