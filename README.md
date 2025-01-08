# Getting started with the project

## Environment Variables

```bash
cp .example.env .env
```

## Start OpenWebUI with Ollama

```bash
docker compose up -d
```

## Pull new models into Ollama

```bash
curl http://localhost:11434/api/pull -d '{
  "model": "granite-code"
}'
```

For chat and long form prompts

```bash
curl http://localhost:11434/api/pull -d '{
  "model": "granite3.1-dense:8b"
}'
```

For inline completions

```bash
curl http://localhost:11434/api/pull -d '{
  "model": "granite3.1-dense:2b"
}'
```

Embedding model for indexing code

```bash
curl http://localhost:11434/api/pull -d '{
  "model": "granite-embedding:30m"
}'
```

https://ollama.com/library for more models

List active models

```bash
curl http://localhost:11434/v1/models
```

Test a model

```bash
curl http://localhost:11434/api/generate -d '{
  "model": "granite3.1-dense:8b",
  "prompt":"What is rubber duck debugging?"
}'
```

## Ollama Logs

```bash
docker logs -f ollama
```

## Install Continue.dev VSCODE Extension

```bash
code --install-extension continue.continue
```
