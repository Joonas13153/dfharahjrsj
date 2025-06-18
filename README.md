# Chatbot Interview API (Estonian)

A FastAPI backend that simulates a job interview in Estonian and rates user responses using the OpenAI API.

## Setup

1. Install dependencies:

```bash
pip install -r requirements.txt
```

2. Copy `.env.example` to `.env`:

```bash
cp .env.example .env
```

3. Paste your OpenAI API key into `.env`:

```
OPENAI_API_KEY=your-key-here
```

4. Run the server:

```bash
uvicorn main:app --host=0.0.0.0 --port=3000
```

## Endpoint

- `POST /chat`
  - Request body:
    ```json
    {
      "message": "Tere, palun tutvusta ennast.",
      "chat_history": []
    }
    ```
  - Response:
    ```json
    {
      "reply": "...",
      "chat_history": [...]
    }
    ```

## Security Note

Never share your `.env` file or API key in public repositories or frontend code.
