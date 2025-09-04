# First Project Monorepo

This repo is a starter monorepo with:
- Next.js frontend
- NestJS backend with Prisma
- PostgreSQL database (use a managed DB like Vercel Postgres or local Postgres)

Quick start (Windows PowerShell):

1. Copy environment file:

```powershell
cp .env.example .env
```

2. Install dependencies and run apps locally:

```powershell
cd .\apps\backend; pnpm install
cd ..\frontend; pnpm install
# then run dev servers separately
cd ..\backend; pnpm run start:dev
cd ..\frontend; pnpm run dev
```

If you use a managed Postgres (Vercel Postgres), put the connection string in `apps/backend/.env` as `DATABASE_URL` and run Prisma migrations (see `apps/backend/prisma/README.md` or run `pnpm exec prisma migrate dev`).

Files created:
- `apps/backend` (NestJS + Prisma)
- `apps/frontend` (Next.js)

Next steps:
- Add authentication and more endpoints
- Configure CI/CD and deployment environment variables
