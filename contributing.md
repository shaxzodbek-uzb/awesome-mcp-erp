# Contributing

Thanks for helping make **Awesome MCP ERP** better! This list catalogs Model Context Protocol (MCP) servers, agents, and production patterns for business software — ERP, CRM, accounting, e-commerce, payments, and vertical SaaS.

## What belongs here

An entry must be **all** of:

- **On topic** — an MCP server, agent framework, auth/consent/observability tool, or pattern/guide that is directly about connecting AI to *business systems*. Generic, unrelated, or purely demo projects do not fit.
- **Real and maintained** — not archived, deprecated, or abandoned. Prefer projects with activity in the last ~12 months.
- **Documented** — has a README or docs a user can actually follow to run it.
- **Working link** — the URL must resolve (no 404s or parked domains).

When in doubt, favor quality over quantity. A short, sharp list beats a long, noisy one.

## Entry format

Add your entry to the most fitting section, as a single bullet:

```
- [Name](https://example.com) - One-line, objective description of what it does.
```

Rules (these are what `awesome-lint` enforces):

- Start the description with a **capital letter** and end it with a **period**.
- Keep it to **one line**, neutral in tone — describe what it does, not marketing copy.
- Use ` - ` (space-hyphen-space) between the link and the description.
- For **official / vendor-published** servers, begin the description with "Official".
- Within a section, official servers are listed first, then community projects, roughly alphabetically.
- No duplicate links anywhere in the list — if something fits two sections, pick its strongest home.

## Adding a new section

If a whole business domain is missing (and you have at least ~4 strong entries for it), propose a new section. Keep section headings short and add a one-line italic intro under the heading.

## Before you open a pull request

Run the checks locally:

```sh
# Structure + formatting (awesome-lint)
npx awesome-lint@latest

# Link health (requires the lychee binary: https://github.com/lycheeverse/lychee)
lychee --no-progress './*.md'
```

> Note: `awesome-lint` includes a rule that the repository be at least 30 days old. That rule only matters when submitting to the [Awesome](https://awesome.re) index; you can ignore it for ordinary content PRs.

Then:

1. Make sure your entry is in the right section and follows the format above.
2. Confirm the link works and the project is maintained and documented.
3. Open the pull request with a short note on **why** the entry belongs.

By contributing, you agree to release your contributions under the [CC0-1.0](license) dedication.
