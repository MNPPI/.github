# Mark Danielson

I design systems, define architecture, and write code. Over the past year I've shifted to using agentic AI for most of my actual development work while leading high-performing teams in Azure-based enterprise environments.

On my own time I love building personal projects on the Cloudflare edge: full-stack apps, developer tooling, and financial analysis tools that run with zero traditional servers. These are the experiments that keep me sharp and excited about what's next.

## Stack

| Layer           | Technology                                                     |
| --------------- | -------------------------------------------------------------- |
| Languages       | TypeScript (strict mode), Python                               |
| Package Manager | pnpm                                                           |
| Runtime         | Cloudflare Workers + Static Assets                             |
| Backend         | Hono (type-safe routes and middleware)                         |
| Database        | Cloudflare D1 + Drizzle ORM                                    |
| Storage         | R2 (objects), KV (sessions/config), Queues (async jobs)        |
| Auth            | Cloudflare Zero Trust Access, Better Auth                      |
| Frontend        | React, Astro, Starlight, Tailwind CSS, Zustand, TanStack Query |
| Testing         | Vitest with Cloudflare Workers pool                            |
| CI/CD           | GitHub Actions (build in GitHub, deploy to Cloudflare)         |
| Observability   | Workers Logs, Traces, Logpush                                  |

## Featured Projects

**[wkd-proxy-worker](https://github.com/MNPPI/wkd-proxy-worker)** - I built this Cloudflare Worker that proxies OpenPGP Web Key Directory requests to Proton Mail for custom domains. It makes PGP key discovery just work for your own domain. It runs on a free Cloudflare Worker instance — try it today!

**[AdventureWorks Sales CRM](https://demo-crm.markdanielson.net)** - I built this proof-of-concept full-stack edge CRM on Cloudflare Workers, D1, Hono, tRPC, React, and Drizzle ORM. It's a real application running entirely at the edge with no traditional server infrastructure. Check out the [Scalar Documentation](https://demo-crm.markdanielson.net/docs) — it's fully API-driven and REST Level 3 HATEOAS compliant.

## Connect

[LinkedIn](https://www.linkedin.com/in/mdanielson)
