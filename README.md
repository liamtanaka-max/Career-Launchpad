# IS Career Launchpad

A self-contained, single-file web tool built to help BYU Information Systems students explore career paths and practice interview skills — no server or backend required.

## What it does

The tool walks users through three connected screens:

1. **Career grid** — browse common IS specializations (data analytics, software development, consulting, cybersecurity, etc.)
2. **Role detail** — see what a specific role actually involves day to day
3. **Mock interview** — practice answering interview questions tied to that role

Users can jump straight into a mock interview from two different places (the global nav or a "Practice this role" button on a role detail page), and both routes feed into the same interview logic.

## Why I built it

As a team, we wanted something students could actually open and use — not just a slide deck about career paths. Business students exploring the IS program often don't know what these roles look like in practice, so we built something interactive instead of descriptive.

## Tech stack

- Plain HTML, CSS, and JavaScript — no frameworks, no build step
- Data lives in JavaScript arrays instead of a database, so the whole thing runs from a single file with zero setup

## Key decisions

- **One shared function, two entry points.** Instead of writing separate logic for "start interview from nav" and "start interview from role page," both call a single `startInterview(roleId)` function. Less duplicated code, easier to maintain.
- **Scoped features to the deadline.** We considered wiring in the Claude API for personalized interview feedback, but treated that as a stretch goal rather than a core requirement. A simple STAR-method checklist covers the same need reliably, without an external dependency that could break under time pressure.

## What I'd add next

- Claude API integration for real-time feedback on interview answers
- More roles and a way for users to save progress across sessions

## Try it

[Live demo link here once GitHub Pages is enabled]
