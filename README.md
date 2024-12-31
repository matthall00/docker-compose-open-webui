# Getting started with the project

## Environment Variables

```bash
cp .example.env .env
```

## Start OpenWebUI

```bash
docker compose up -d
```

Start with Ollama

```bash
docker compose -f docker-compose.yml -f docker-compose.ollama.yml up -d
```

Pull new models into Ollama

```bash
curl http://localhost:11434/api/pull -d '{
  "model": "granite-code"
}'
```

https://ollama.com/library for more models
