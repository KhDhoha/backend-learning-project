# Backend Learning Project — Checklist

## Phase 1 — Project setup

- [x] Create GitHub repo and clone locally
- [x] Set up virtual environment
- [x] Install FastAPI, Uvicorn, SQLAlchemy, Alembic, python-dotenv
- [x] Create folder structure (`app/`, `routes/`)
- [x] First commit pushed to GitHub

## Phase 2 — Database layer

- [ ] Write `database.py` (engine, session, Base)
- [ ] Write `models.py` — Task model (id, title, done, created_at)
- [ ] Initialize Alembic (`alembic init`)
- [ ] Configure `alembic.ini` to point to your DB
- [ ] Create first migration (`alembic revision --autogenerate`)
- [ ] Apply migration (`alembic upgrade head`)
- [ ] Verify tasks table exists in `tasks.db`

## Phase 3 — REST API routes

- [ ] Write `main.py` (create app, include routers)
- [ ] Write Pydantic schemas (TaskCreate, TaskResponse)
- [ ] `GET /tasks` — return all tasks
- [ ] `GET /tasks/{id}` — return one task
- [ ] `POST /tasks` — create a task
- [ ] `PUT /tasks/{id}` — update a task
- [ ] `DELETE /tasks/{id}` — delete a task
- [ ] Test all routes in `/docs` (Swagger UI)

## Phase 4 — Authentication

- [ ] Add User model (id, email, hashed_password)
- [ ] Install `passlib` and `python-jose`
- [ ] `POST /register` — hash password and save user
- [ ] `POST /login` — verify password, return JWT token
- [ ] Write auth middleware (verify JWT on protected routes)
- [ ] Protect POST/PUT/DELETE task routes with auth
- [ ] Test auth flow end to end in `/docs`

## Phase 5 — Polish and deploy

- [ ] Add proper error handling (404, 400 responses)
- [ ] Write a solid README (what it does, how to run it)
- [ ] Add `.env.example` file (so others know what vars are needed)
- [ ] Make sure `.env` is in `.gitignore`
- [ ] Deploy to Railway or Render (free tier)
- [ ] Add live URL to GitHub repo description
- [ ] Final commit — project complete
