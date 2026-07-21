# Search Queries for Job Scraper

<!-- Candidate is based in Pato Branco, PR, Brazil, not relocating, targeting fully remote
international roles. The built-in Danish CLI tools (jobindex-search, jobbank-search,
jobdanmark-search, jobnet-search under .agents/skills/) do not apply here and should be
ignored for this candidate. The linkedin-search CLI (.agents/skills/linkedin-search) IS
usable - it's country-agnostic and supports `--location "Remote"`. Everything else below
runs via WebSearch site: queries, same mechanism the job-scraper skill already uses. -->

## Search Sites

Primary (remote/international, junior-friendly):
- **linkedin.com/jobs** - use the `linkedin-search` CLI directly when possible (`bun run skills/linkedin-search/cli/src/cli.ts search -q "<query>" -l "Remote" --jobage 14`), or `site:linkedin.com/jobs` via WebSearch as a fallback
- **remoteok.com** - remote-only job board, has a junior/entry filter
- **weworkremotely.com** - large remote job board, mostly web dev
- **himalayas.app** - remote job board with seniority filters
- **remotive.com** - remote tech jobs, has a junior/entry-level category
- **wellfound.com** (formerly AngelList Talent) - startup jobs, better odds for junior candidates than big-company boards

Secondary (freelance / contract, good for building track record while job-hunting):
- **workana.com** - largest LatAm freelance platform, good fit for a Brazil-based candidate, has web dev gigs in English and Portuguese
- **upwork.com** - international freelance platform, generalist

If any of these turn out to be worth scraping on a recurring basis with a dedicated CLI (like the Danish portals have), consider running `/add-portal` to build one.

**Wellfound note:** individual job posting URLs found via `site:wellfound.com` WebSearch churn fast and are frequently expired (410) by the time they're indexed. Prefer browsing Wellfound's own live role pages directly (e.g. `wellfound.com/role/r/frontend-engineer`, `wellfound.com/role/r/react-developer`) over trusting a Google-indexed job URL. Also check each listing's "Location Requirement" / "Hires remotely in" field carefully - many Wellfound "remote" postings are restricted to candidates physically located in one country (commonly the US) despite being tagged remote.

## Query Categories

Queries are grouped by priority. All roles are remote by default - do not add a city/commute filter. Combine with "remote" explicitly since many of these sites list hybrid/onsite roles too.

### Priority 1: Junior Full-Stack Developer (React / Next.js / Node / TypeScript)

Primary target - most desired career direction.

```
site:remoteok.com "junior full stack" React
site:weworkremotely.com "junior" "full stack" TypeScript
site:remotive.com "junior full stack developer"
site:linkedin.com/jobs "junior full stack developer" remote
site:wellfound.com "junior full stack" remote
```

### Priority 2: Junior Frontend Developer (React / Next.js / Tailwind CSS)

Secondary target, same core stack, frontend-only postings.

```
site:remoteok.com "junior frontend" React OR "Next.js"
site:weworkremotely.com "junior" frontend React
site:remotive.com "junior front end developer"
site:linkedin.com/jobs "junior frontend developer" remote
```

### Priority 3: AI/Automation-Adjacent Roles (pivot using Kodama/Connfit experience)

Adjacent roles that value LLM integration, agent development, and automation experience even without a formal "junior" title.

```
site:remoteok.com "junior" "AI engineer" OR "automation developer"
site:weworkremotely.com "no-code" OR "automation" N8N
site:linkedin.com/jobs "junior AI engineer" remote
site:himalayas.app "LLM" OR "AI agent" junior
```

### Priority 4: Freelance / Broader Net (income while building track record)

Wider net, includes freelance/contract gigs and general remote developer postings without a strict junior filter.

```
site:workana.com "React" OR "Next.js" desenvolvedor
site:upwork.com "React developer" junior
site:remoteok.com developer entry-level
site:linkedin.com/jobs "junior developer" remote React
```

## Remote Eligibility Filter

There is no commute range for this candidate - the filter is remote eligibility, not distance:
- Fully remote, open to any country: **PASS** (primary target)
- Remote but restricted to residents/citizens of a specific country/region (e.g. "must be US-based", "EU residency required"): **FLAG** - note the restriction, most likely a fail unless the candidate holds that residency
- Requires relocation to any location: **FAIL** (deal-breaker - candidate is not moving from Pato Branco, PR, Brazil)
- On-site or hybrid role based in Brazil: **FLAG** - not the current focus, but surface it rather than silently dropping it, in case it's compelling

## Reality Check on "Junior" + "Remote" + "International"

This combination is one of the harder segments of the remote job market - most international remote postings ask for 2-3+ years of experience even when titled "junior". Treat postings asking for up to ~2 years of experience as in-scope. Don't filter out roles just because they say "0-2 years" or "early career" instead of literally "junior". Freelance platforms (Workana, Upwork) are a realistic parallel path while the full-time search continues, not a fallback to be deprioritized.

## Date Filter

Only include jobs posted within the last 14 days, or with an application deadline that has not yet passed. If a posting date cannot be determined, include it but flag as "date unknown".

## Adapting Queries

If the user specifies a focus area, select queries from the matching category and also generate 2-3 custom queries for that focus. For example:
- "/scrape freelance" -> Priority 4 queries + custom freelance-specific queries
- "/scrape AI" -> Priority 3 queries + custom queries combining "AI" with React/Next.js
