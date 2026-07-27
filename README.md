# sports-store-catalog-service

FastAPI microservice for the Sports Store product catalog — product listing, detail,
and search. Owns the `catalog_db` MongoDB database. Consumed by `cart-service` and
`order-service` to resolve product data.

## Stack

FastAPI, MongoDB (Motor), pytest.

## Local development

```bash
cp .env.example .env
pip install -r requirements.txt
uvicorn main:app --reload
```

Health check: `GET /health`.

## Branching convention

- `feature/<short-description>` — new functionality
- `bugfix/<short-description>` — non-urgent fixes
- `hotfix/<short-description>` — urgent production fixes

All changes land on `main` via pull request with at least 1 approval (enforced by repository ruleset).
