# Práctica 7 — CORS, logs y tests

Continuación de la práctica 6. Agrega CORS, logs técnicos y de auditoría, y pruebas de la API.

## Rutas

- `POST /api/auth/token/`
- `POST /api/auth/token/refresh/`
- `POST /api/auth/logout/`
- `GET /api/auth/logs/auditoria/` y `GET /api/auth/logs/tecnico/` (solo staff)
- `/api/usuarios/users/`
- `/api/productos/products/`

Orígenes CORS: `http://localhost:3000`, `http://localhost:4200`, `http://127.0.0.1:3000`.

## Arranque

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
cp back_end_django/.env.example back_end_django/.env
cd back_end_django
python manage.py migrate
python manage.py runserver
```

Docker:

```bash
cd back_end_django
docker compose up --build
```

## Tests

```bash
cd back_end_django
python manage.py test
```
