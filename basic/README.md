# MLflow Tracing with Express and OpenAI

TypeScript implementation of MLflow tracing with session context using Express and OpenAI.

## Setup

1. Install dependencies:
```bash
yarn install
```

2. Create `.env` file:
```bash
cp .env.example .env
# Edit .env and add your OpenAI API key
```

3. Run the application:
```bash
# Development mode with hot reload
yarn dev
```

## Example Request

```bash
curl -X POST http://localhost:8000/chat \
  -H "Content-Type: application/json" \
  -H "X-Session-ID: session-123" \
  -H "X-User-ID: user-456" \
  -d '{"message": "Hello, how are you?"}'
```

Then go to the MLflow UI and you should see the generated trace.
