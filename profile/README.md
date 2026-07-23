# Mark Danielson

I design systems, define architecture, and write code. Over the past year I've shifted to using agentic AI for most of my actual development work while leading high-performing teams in Azure-based enterprise environments.

On my own time I love building personal projects on the Cloudflare edge: full-stack apps, developer tooling, and financial analysis tools that run with zero traditional servers. These are the experiments that keep me sharp and excited about what's next.

## Reference Architecture

MNPPI maintains current stack standards, delivery controls, and adoption guidance at [architecture.mnppi.org](https://architecture.mnppi.org/).

GitHub Actions validates changes, and GitHub rulesets authorize merges.
Cloudflare Workers Builds owns normal production builds and deployments.

## Stack

| Layer                | Technology                                                              |
| -------------------- | ----------------------------------------------------------------------- |
| Languages            | TypeScript (strict mode), Python                                        |
| Package Manager      | pnpm                                                                    |
| Runtime              | Cloudflare Workers with Static Assets                                   |
| Applications         | Astro for static sites; React with Vite for interactive applications    |
| APIs                 | Hono with Zod validation                                                |
| Data                 | Cloudflare D1 with Drizzle ORM; R2 and other managed services as needed |
| Authentication       | Cloudflare Access for staff; magic links or Better Auth for public apps |
| Testing              | Vitest with the Cloudflare Workers pool                                 |
| Merge Authority      | GitHub Actions and GitHub rulesets                                      |
| Build and Deployment | Cloudflare Workers Builds                                               |
| Observability        | Workers Logs, release metadata, runtime measures, and approved pilots   |

## Featured Projects

**[wkd-proxy-worker](https://github.com/MNPPI/wkd-proxy-worker)** - I built this Cloudflare Worker that proxies OpenPGP Web Key Directory requests to Proton Mail for custom domains. It makes PGP key discovery just work for your own domain. It runs on a free Cloudflare Worker instance — try it today!

**[AdventureWorks Sales CRM](https://demo-crm.markdanielson.net)** - I built this proof-of-concept full-stack edge CRM on Cloudflare Workers, D1, Hono, tRPC, React, and Drizzle ORM. It's a real application running entirely at the edge with no traditional server infrastructure. Check out the [Scalar Documentation](https://demo-crm.markdanielson.net/docs) — it's fully API-driven and REST Level 3 HATEOAS compliant.

## Connect

[LinkedIn](https://www.linkedin.com/in/mdanielson)

## Public Pull Request Checks

GitHub runs required security and plain-language checks for each public pull request.
These checks use free standard GitHub-hosted runners.
They do not use private MNPPI packages, registries, reusable workflows, or package credentials.
