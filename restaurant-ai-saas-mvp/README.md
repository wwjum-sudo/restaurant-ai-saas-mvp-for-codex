# Restaurant AI SaaS MVP

Mobile-first H5 MVP for a restaurant AI SaaS focused on helping 2–5 store owners identify weekly problems, dispatch actions, and review execution.

## Core MVP loop
Store manager enters data → system identifies issues → boss sees action cards → assigns tasks → manager gives feedback → weekly review.

## Target users
- Boss / investor managing 2–5 stores
- Store manager responsible for execution and data entry

## Tech direction
- Frontend: Next.js + Tailwind
- Backend: Next.js API Routes or NestJS
- Database/Auth: Supabase
- AI layer: model API for explanation and action-card wording
- Business logic: deterministic rules + metrics engine

## Repository structure
- `docs/` product and implementation docs
- `frontend/` H5 client app
- `backend/` API / business logic
- `db/` migrations and schema

## MVP success definition
- Boss can see which store has the most important problem this week
- Boss can assign 1–3 action cards
- Manager can complete data entry and task feedback
- At least one weekly loop is completed: issue → action → feedback → review
