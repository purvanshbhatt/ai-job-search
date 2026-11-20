# Handoff
_Updated by the last agent session. Keep under 40 lines._

## Current state (2026-11-20)
- Profile populated from documents/cv/ resumes (/setup Path A): CLAUDE.md, 01/02/04/05/07 skill files,
  cv/main_example.tex, job-scraper/search-queries.md. Items marked ⚠ are still unconfirmed.
- Work auth: F-1 STEM OPT to July 2027; open to relocation (US, CA, UK, EU, SG, JP, UAE, QA, AU, NZ).
- Sweep: 752 postings screened -> job_scraper/seen_jobs.json; 29-job shortlist in
  job_scraper/shortlist_2026-11-20.md (both gitignored).
- Batch 1 drafted (10 jobs, CV 2p + cover 1p, compiled + ATS-checked, status `drafted` in
  job_search_tracker.csv): Deloitte (Jersey City), Notion NY, Remitly, Replit, Google AI Protection,
  Amazon SIRT, Stripe, Refractal (London), Plaud (SG), Littlepay (LU). NOTHING submitted.
- Tools installed on Windows box: Bun 1.4.5, MiKTeX 25.12 (user scope, AutoInstall=1), pypdf (user site).

## Blocking before any submission
- Confirm Filmy AI title and Cod-Ingenuity title/duties. Every batch-1 CV routes them through
  \filmytitle / \codtitle macros (marked PENDING CONFIRMATION) - sed both macros, then recompile.
- Confirm Bunchful pentest scope and the one-resume-only tools (Splunk, Burp, FTK, ...).
- LinkedIn profile URL not recorded yet.

## Next steps
1. Apply confirmations -> update 01-candidate-profile.md first, then macros in cv/main_*.tex.
2. Submit batch 1 one by one, with the user's yes per form (user signs in to portals).
3. Outreach "1+3" per startup: user to choose (a) drafts + user clicks, or (b) browser at <20/day.
4. Batch 2 from the shortlist (#5, 9-12, 16-29).

## Open questions / gotchas
- Firecrawl credits exhausted on 2026-11-20 (daily refresh); WebSearch works.
- LinkedIn guest search caps ~20 results/query - use city-level locations for the US.
- GateGuard hook blocks first edit of every file; state facts then retry.
- Sponsorship unverified for Notion, Plaud, Littlepay, Stripe (E-Verify) - ask recruiters.
