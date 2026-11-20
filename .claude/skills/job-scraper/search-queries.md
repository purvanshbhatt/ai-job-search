# Search Queries for Job Scraper

<!-- Personalized for Purvansh Bhatt by /setup -->

## Installed portal CLIs (primary for `/scrape`)

`/scrape` discovers every portal skill under `.agents/skills/*/SKILL.md` and runs its CLI first. Enabled: `linkedin-search`, `freehire-search`. The four Danish portals stay **disabled** (not Purvansh's market).

The `site:` query templates in this file are the **WebSearch fallback** - for company career pages, startup job boards, or when a CLI fails.

**Language scope:** English only (the only declared working language). Postings that *require* German, Dutch, French, Japanese, Arabic etc. as a job condition fail the Language Gate; postings merely *written* in another language but working in English are fine.

## Search Sites

Primary:
- **linkedin.com/jobs** - via `linkedin-search` CLI, one call per region below
- **FreeHire** - via `freehire-search` CLI
- **Startup boards (WebSearch fallback):** wellfound.com (AngelList), workatastartup.com (YC), jobs.ashbyhq.com, boards.greenhouse.io, jobs.lever.co

Secondary (company career pages via Google):
- `site:jobs.ashbyhq.com`, `site:boards.greenhouse.io`, `site:jobs.lever.co` with role keywords - most startups post here first

## Regions (LinkedIn `--location` strings)

Run every priority category against each region. Add `--remote remote` runs for "United States" and "European Union".

| Region | `--location` value |
|--------|--------------------|
| US | `United States` (+ `--remote remote`), `New York, United States` |
| Canada | `Canada` |
| UK | `United Kingdom` |
| Europe | `European Union` (+ `--remote remote`), `Netherlands`, `Germany`, `Luxembourg`, `Ireland`, `Switzerland` |
| Singapore | `Singapore` |
| Japan | `Japan` |
| UAE | `United Arab Emirates` |
| Qatar | `Qatar` |
| Australia | `Australia` |
| New Zealand | `New Zealand` |

## Query Categories

**Organize by function, not job title.** Each category lists title variants to search.

### Priority 1: Security Engineering - Detection, Response & Cloud

The strongest and most desired direction.

```
"security engineer"
"detection engineer"
"detection and response engineer"
"cloud security engineer"
"security automation engineer"
"incident response engineer"
site:jobs.ashbyhq.com "security engineer"
site:boards.greenhouse.io "detection engineer"
site:linkedin.com/jobs "security engineer" startup
```

### Priority 2: AI / LLM Security

The differentiator (ResilAI, AI Red Team Lab). Startups hire heavily here.

```
"AI security engineer"
"LLM security"
"AI red team"
"machine learning security engineer"
"AI safety engineer" security
site:jobs.ashbyhq.com "AI security"
site:wellfound.com "AI security engineer"
```

### Priority 3: Security Operations - SOC, IR, DFIR

```
"security analyst"
"SOC analyst"
"incident response analyst"
"cyber security analyst"
"threat detection analyst"
"DFIR analyst"
```

### Priority 4: GRC, Risk & AppSec (broader net)

```
"GRC analyst"
"security risk analyst"
"security compliance analyst"
"application security engineer"
"product security engineer"
"penetration tester"
```

## Seniority Filter

Keep: titles with no level, "I", "II", "Associate", "Engineer", "Analyst", and "Senior" at startups (flag as stretch).
Drop: Staff, Principal, Distinguished, Director, Head of, VP, Manager, Architect, and any posting demanding 7+ years.

## Location Filter

Purvansh is open to relocation (2-3 weeks) and remote/hybrid. All target regions above are **PASS** on location. The real filter is the **Eligibility Gate** in `04-job-evaluation.md`:
- US: drop citizenship / green card / clearance / "no sponsorship now or in future"
- Elsewhere: drop "must already have the right to work" / "no visa sponsorship" / nationals-only
- Prefer postings that mention visa sponsorship or relocation support

## Language Filter

Your working languages and levels are in CLAUDE.md's Languages table. When filtering scraped results, apply `04-job-evaluation.md`'s Language Gate: a posting requiring a language you haven't declared at all is excluded; a posting requiring a higher level than you declared in a language you do work in is not excluded, flag it clearly instead (see `job-scraper/SKILL.md`'s Step 3 "Quick Fit Assessment" for how the flag surfaces in `/scrape` output). Postings simply *written* in a language you don't work in, that don't require it on the job, are fine.

## Date Filter

Only include jobs posted within the last 14 days, or with an application deadline that has not yet passed. If a posting date cannot be determined, include it but flag as "date unknown".

## Startup Preference

When ranking otherwise-equal postings, prefer startups (Series Seed-C, <500 employees, or YC / top-VC backed). Every company is acceptable.

## Adapting Queries

If the user specifies a focus area, select queries from the matching category and also generate 2-3 custom queries for that focus. For example:
- "/scrape AI security" -> Priority 2 queries + custom focus-specific queries
- "/scrape europe" -> all categories, Europe regions only
