# cloud-ops-portfolio

A minimal Cloud/DevOps portfolio built with Python and Flask, containerized with Docker, and deployed publicly on Google Cloud Run.

Built as my personal completion of the DEV Community **New Year, New You Portfolio Challenge** using Google AI.

## Live Demo

Deployed on Google Cloud Run:

https://cloud-ops-portfolio-503482512915.europe-west1.run.app

## Stack

- Python
- Flask
- Gunicorn
- Docker
- Google Cloud Run
- Google Cloud Build
- Artifact Registry
- Google AI Studio

## What it shows

The portfolio highlights:

- Cloud/DevOps skills
- selected projects
- GitHub profile
- a responsive dark interface
- a live cloud deployment

Featured projects include:

- `env-check`
- `log-triage`

## Local Development

Create and activate a virtual environment:

```bash
python3 -m venv .venv
source .venv/bin/activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Run locally:

```bash
python3 app.py
```

Then open:

```text
http://localhost:8080
```

## Docker

Build the image:

```bash
docker build -t cloud-ops-portfolio .
```

Run the container:

```bash
docker run --rm -p 8080:8080 cloud-ops-portfolio
```

Then open:

```text
http://localhost:8080
```

## Google Cloud Run

The application was deployed from source with:

```bash
gcloud run deploy cloud-ops-portfolio \
  --source . \
  --region europe-west1 \
  --allow-unauthenticated
```

The deployment uses the repository `Dockerfile`, Google Cloud Build, Artifact Registry, and Cloud Run.

## Google AI

Google AI Studio was used to help generate and refine the initial portfolio interface.

The generated design was then integrated into the Flask application and prepared for containerized deployment.

## Project Structure

```text
cloud-ops-portfolio/
├── app.py
├── Dockerfile
├── .dockerignore
├── requirements.txt
├── templates/
│   └── index.html
├── README.md
└── LICENSE
```

## Challenge

Inspired by the DEV Community **New Year, New You Portfolio Challenge**.

The goal was to create a developer portfolio using Google AI and deploy it to Google Cloud Run.