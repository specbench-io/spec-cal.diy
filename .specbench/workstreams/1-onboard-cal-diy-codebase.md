# Onboard cal.diy codebase

## Description

Map the existing cal.diy codebase into Specbench, seam by seam: bounded contexts and glossary first, then deep slices starting with booking creation.

## Goals

- Map every in-scope area of cal.diy to a Subdomain and Bounded Context, with a glossary in the app's own words
- Model each context's stored data (Aggregates, Enums, Value Objects) from the Prisma schema
- Specify the main user actions (Use Cases) with steps that read as plain instructions and outcomes that match the app's errors
- Show how contexts talk: Interfaces and Adapters for calls, Integration Events and Event Handlers for notifications, Scheduled Jobs for background work
- Recreate the code faithfully: where it departs from good patterns, model what it does and record the drift as a thread

## Out of scope

- Team scheduling (round robin, collective and managed event types). Cal.diy removed teams; leftover team code is flagged, not specified.
- Organizations, organization blocklists and organization billing (removed in cal.diy)
- Workflows, SMS reminders and Cal AI phone agents (removed in cal.diy)
- Routing Forms, CRM routing and attribute sync (removed in cal.diy)
- SSO, SAML and Directory Sync (removed in cal.diy)
- Credits, platform billing and seat proration (team and organization billing leftovers)
- UI-only concerns with no domain rules: embeds styling, themes, data-table filters
