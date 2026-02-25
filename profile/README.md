# Mark Danielson

Software engineering director who stays hands-on. I design systems, define architecture, and write code. Over the past year I've shifted to using agentic AI for most of the actual code authoring.

I use this GitHub organization to manage personal projects in developer tooling, financial technology, and full-stack web applications.

## Stack

| Layer           | Technology                                              |
| --------------- | ------------------------------------------------------- |
| Languages       | TypeScript (strict mode), Python                        |
| Package Manager | pnpm                                                    |
| Runtime         | Cloudflare Workers + Static Assets                      |
| Backend         | Hono (type-safe routes and middleware)                  |
| Database        | Cloudflare D1 + Drizzle ORM                             |
| Storage         | R2 (objects), KV (sessions/config), Queues (async jobs) |
| Auth            | Cloudflare Zero Trust Access, Better Auth               |
| Frontend        | React, Tailwind CSS, Zustand, TanStack Query            |
| Testing         | Vitest with Cloudflare Workers pool                     |
| CI/CD           | GitHub Actions (build in GitHub, deploy to Cloudflare)  |
| Observability   | Workers Logs, Traces, Logpush                           |

## Featured Projects

**[wkd-proxy-worker](https://github.com/MNPPI/wkd-proxy-worker)** - Cloudflare Worker that proxies OpenPGP Web Key Directory (WKD) requests to Proton Mail for custom domains. If you use Proton Mail with your own domain and want PGP key discovery to just work, this handles it.

**[AdventureWorks Sales CRM](https://demo-crm.markdanielson.net)** - Full-stack edge CRM built on Cloudflare's native platform: Workers, D1, Hono, tRPC, React, and Drizzle ORM. Shows how to build a real application at the edge with no traditional server infrastructure. Fully API-driven with [Scalar Documentation](https://demo-crm.markdanielson.net/docs).

## Connect

[LinkedIn](https://www.linkedin.com/in/mdanielson)
