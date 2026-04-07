# sample-dockerized-node-app

A simple Node.js sample app demonstrating a Dockerized project setup.

## Project Overview

This project is a minimal Node.js application that calculates and logs the sum of two numbers. It includes a `Dockerfile` so the app can be run inside a container.

## Files

- `index.js` - sample application entrypoint
- `package.json` - project metadata and npm scripts
- `Dockerfile` - Docker image build instructions
- `README.md` - project documentation

## Requirements

- Node.js 20+ (for local development)
- npm
- Docker (for container builds/runs)

## Run Locally

1. Install dependencies:

```bash
npm install
```

2. Start the app:

```bash
npm start
```

The app prints the sum of two numbers to the console.

## Docker

Build the Docker image:

```bash
docker build -t sample-dockerized-node-app .
```

Run the container:

```bash
docker run --rm sample-dockerized-node-app
```

Run the container with a volume mount for local code changes:

```bash
docker run --rm -v "%cd%:/app" sample-dockerized-node-app
```

> On Linux/macOS, use `-v "$(pwd):/app"` instead of `%cd%`.

## Notes

- The project currently uses `nodemon` for development auto-reloading.
- The `test` script is still the default npm placeholder.
- You can rename the repository to `sample-dockerized-node-app` or a similar descriptive name when pushing to GitHub.
