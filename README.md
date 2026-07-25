# Echo

Turn a text prompt into a live, editable Next.js application — instantly.

![Demo Screenshot](./public/demo.png)

## Stack

| Layer | |
|---|---|
| Framework | Next.js 15 (App Router) |
| Styling | Tailwind CSS v4, shadcn/ui |
| API | tRPC v11 + TanStack React Query |
| ORM | Prisma + PostgreSQL |
| Auth | Clerk |
| AI | Gemini 2.0 Flash (`@inngest/agent-kit`) |
| Sandboxes | E2B Code Interpreter |
| Jobs | Inngest |

## Quick Start

```bash
git clone https://github.com/acegikmoo/echo.git
cd echo
bun install
docker compose up -d          # PostgreSQL
bun db:push                   # push schema
bun dev                       # next.js
npx inngest-cli@latest dev    # worker (separate terminal)
```

Copy `.env.example` to `.env` and fill in your keys (Clerk, Gemini, E2B).

## Structure

```
app/          pages + API routes
components/  React components + shadcn/ui
trpc/         tRPC routers
lib/          Prisma client, utils
src/inngest/  AI agent, tools, prompt
prisma/       schema
```

## Deploy

Vercel + managed PostgreSQL (Neon/Supabase). Set env vars, connect Clerk + Inngest production instances.

## License

MIT
