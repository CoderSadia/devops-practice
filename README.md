# DevOps Practice Project

A small Flask app used to practice Git, Docker, and GitHub Actions (CI/CD).

## What the app does
- `/` — returns a "Hello DevOps" message
- `/health` — checks if the app is running correctly

## Run locally

    python3 -m venv venv
    source venv/bin/activate
    pip install -r requirements.txt
    python app/main.py

## Run tests

    pytest

## Run with Docker

    docker build -t devops-practice .
    docker run -p 5000:5000 devops-practice

## CI/CD
Pushing to GitHub triggers `.github/workflows/ci.yml`, which automatically runs tests and builds the Docker image (visible under the Actions tab).
