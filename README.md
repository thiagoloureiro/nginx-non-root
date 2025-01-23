# NGINX Docker Image (Non-Root)

[![Build status](https://dev.azure.com/thiagoguaru/AlertHawk/_apis/build/status/nginx%20non-root)](https://dev.azure.com/thiagoguaru/AlertHawk/_build/latest?definitionId=-1)

This repository provides a lightweight, non-root NGINX image built on the `nginx:alpine` base image. It serves content securely by running as a non-root user.

## Features

- Based on the minimal `nginx:alpine` image for reduced size and faster performance.
- Runs as a non-root user (`nginx`) to enhance security.
- Configurable through a custom `nginx.conf` file.
- Exposes the service on port `8080`.

---

## Dockerfile Highlights

1. **Ownership and Permissions:**
   - Ensures key directories and files are owned by the `nginx` user.
   - Sets appropriate permissions for security.

2. **Custom Configuration:**
   - Uses a custom NGINX configuration file (`nginx.conf`).

3. **Non-Root User:**
   - The image runs as the `nginx` user for all operations.

---

## Usage

### Build the Image

```bash
docker build -t custom-nginx:non-root .
