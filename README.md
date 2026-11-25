# Next.js Dashboard

A dashboard application built with the Next.js App Router, React, TypeScript, and Tailwind CSS. The project includes dashboard and invoice UI components, PostgreSQL data-access helpers, and a route for loading sample data

## Requirements

- Node.js
- pnpm
- A PostgreSQL database

## Getting started

1. Install dependencies:

   ```bash
   pnpm install
   ```

2. Create a local environment file from the example:

   ```bash
   cp .env.example .env.local
   ```

   Set `POSTGRES_URL` in `.env.local` to your PostgreSQL connection string. The other database connection fields are included for reference; the application connects using `POSTGRES_URL`.

3. Start the development server:

   ```bash
   pnpm dev
   ```

4. Open [http://localhost:3000](http://localhost:3000).

## Sample database data

With `POSTGRES_URL` configured, send a GET request to `/seed` to create the sample tables and populate them with the included demo data:

```bash
curl http://localhost:3000/seed
```

The seed route is intended for local development and demo data. Do not expose it as an unrestricted production endpoint.

## Scripts

| Command | Description |
| --- | --- |
| `pnpm dev` | Start the development server with Turbopack |
| `pnpm build` | Create a production build |
| `pnpm start` | Start the production server |

## Project structure

- `app/` — App Router entry points, database helpers, and API routes
- `app/ui/` — Dashboard, invoice, customer, and shared UI components
- `app/lib/` — Data access, type definitions, formatting helpers, and sample data
- `public/` — Static assets
