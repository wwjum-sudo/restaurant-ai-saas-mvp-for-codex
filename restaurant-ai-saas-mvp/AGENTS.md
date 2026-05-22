# AGENTS.md

## Product goal
Build a mobile-first H5 MVP for a restaurant AI SaaS focused on **operational control**, not a full ERP/PMS.

The MVP must help a boss managing 2–5 stores:
1. see the most important weekly store issues,
2. get 1–3 action cards,
3. assign actions to a store manager,
4. review execution and weekly results.

## Core users
- `boss`: sees overview, store issues, action cards, task status, weekly review
- `manager`: enters store data, uses OCR-assisted entry, receives tasks, submits feedback

## MVP boundaries
### Build now
- boss overview page
- store list page
- store detail page
- action card center
- task/feedback center
- weekly review page
- manager daily todo page
- manager data entry page
- OCR-assisted upload page
- manager task feedback page
- Supabase schema for core entities
- rules engine v1

### Do NOT build now
- full accounting system
- full auto-reconciliation across multiple channels/platforms
- dynamic real-time gross margin engine
- inventory prediction / procurement forecast
- employee attendance / HR system
- franchise CRM / HQ system
- complex approval workflow
- full automated external integrations

## Product principles
- Keep UI simple and mobile-first.
- Boss should understand the main problem in 10 seconds.
- Boss should be able to assign an action in under 30 seconds.
- Prefer deterministic business logic over model-generated business conclusions.
- Put formulas, thresholds, and issue-detection logic in code, not only in prompts.
- Use the model to explain and phrase actions, not to replace core calculations.

## Technical stack
- Frontend: Next.js + Tailwind CSS
- Backend: Next.js API routes first (unless a cleaner service split is clearly needed)
- Database/Auth: Supabase
- AI: API-based model calls only for explanation / action-card generation

## Implementation guidance
- Start with fake data and scaffolding if needed.
- Build core navigation and forms first.
- Build schema and CRUD before advanced polish.
- Keep components small and easy to replace.

## Suggested modules
- `frontend/app/(boss)/...`
- `frontend/app/(manager)/...`
- `backend/rules/`
- `backend/services/`
- `db/migrations/`

## Minimum deliverable
A working prototype where:
- a manager can submit weekly data,
- the system generates issue results,
- a boss can see the issue list and action cards,
- a boss can assign a task,
- a manager can submit feedback,
- a weekly review can be displayed.

## Before finishing any task
- summarize files changed
- list assumptions made
- run lint / typecheck if available
- do not silently expand scope
