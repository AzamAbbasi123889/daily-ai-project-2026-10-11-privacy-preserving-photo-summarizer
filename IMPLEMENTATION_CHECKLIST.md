# Implementation Checklist

Build the application yourself using `PROJECT_BRIEF.md`.

## Initial setup

- [ ] Read the project specification.
- [ ] Review the architecture and data model.
- [ ] Create a Python virtual environment.
- [ ] Install and pin the required dependencies.
- [ ] Configure credentials through environment variables.
- [ ] Review the data privacy and security requirements.

## Project acceptance criteria

- [ ] Upload of ≥50 images succeeds without error
- [ ] Embedding vector (512‑dim) stored in PostgreSQL
- [ ] Processing time ≤0.3 s per image on a typical laptop
- [ ] Clusters count auto‑adjusts between 3‑10 for 50‑200 images
- [ ] Silhouette score ≥0.25 on the local test set
- [ ] User can view cluster thumbnails in UI
- [ ] Generated summary ≤80 characters
- [ ] No external API call logged (verified via network capture)
- [ ] Summaries pass a basic grammar check (>90% pass)
- [ ] Dashboard loads <2 s after backend start
- [ ] Exported PDF contains all images and generated text
- [ ] All UI actions work offline
- [ ] Set up Docker‑Compose with FastAPI, PostgreSQL, Ollama
- [ ] Implement CLIP ingestion endpoint
- [ ] Create clustering script and integrate with API
- [ ] Add LLM prompt flow for summaries
- [ ] Build React upload & gallery UI
- [ ] Write unit tests for ingestion and clustering
- [ ] Unit tests for CLIP embedding function (mock image inputs)
- [ ] Integration test: upload 10 images → verify DB rows count
- [ ] Clustering test: known synthetic embeddings produce expected number of clusters
- [ ] LLM mock test: intercept prompt and assert required placeholders are present
- [ ] Privacy test: capture network traffic during full run and assert no outbound connections
- [ ] Docker‑Compose for local development (ports 8000 & 3000)
- [ ] Optional Kubernetes manifest for self‑hosted deployment on a private server
- [ ] Environment variables to toggle GPU usage for CLIP/Ollama
- [ ] CI pipeline builds Docker images and runs the full test suite on push

## Before completion

- [ ] Implement the planned MVP features.
- [ ] Add unit and integration tests.
- [ ] Run the test suite.
- [ ] Measure the evaluation metrics in the brief.
- [ ] Record actual results and known limitations.
- [ ] Document setup and deployment.
- [ ] Update the README to reflect the implemented features.
- [ ] Add only verified outcomes to your resume.
