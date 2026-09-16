# KyubeyV1 — Agent Instructions

## Running the Bot

Secrets are managed via Infisical. Never commit `.env` files.

```bash
infisical run -- python3 -m app.main
```

> **Never** run `python3 app/main.py` — it breaks package imports. Always use `-m app.main`.

## Project Structure

```
app/
  __init__.py
  main.py
  config/
    __init__.py
    env.py      # Environment variables via os.environ
    paths.py
```

## Conventions

- Use `infisical run` to inject secrets — do not hardcode or use `.env` files directly.
- Keep imports as absolute: `from app.config.env import ...`
