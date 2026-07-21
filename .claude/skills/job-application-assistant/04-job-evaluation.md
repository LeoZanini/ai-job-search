# Job Evaluation Framework

<!-- SETUP: Skill match areas and career goals are personalized by running /setup -->

## Scoring Dimensions

Evaluate each job posting against these five dimensions:

### 1. Technical Skills Match (0-100)
How well do the required/preferred skills align with the candidate's capabilities?

| Score | Meaning |
|-------|---------|
| 80-100 | Core requirements are primary skills |
| 60-79 | Most requirements match, 1-2 gaps that are learnable |
| 40-59 | Partial match, significant upskilling needed |
| 0-39 | Fundamental mismatch |

**Strong match areas:** React, Next.js, TypeScript/JavaScript, Tailwind CSS, Node.js - the full JS/TS front-to-back stack
**Moderate match areas:** Python, SQL/PostgreSQL, DevOps (Docker, CI/CD, N8N), AI/LLM integration and agent development
**Weak match areas:** Deep CS fundamentals/algorithms (self-taught, no CS degree), large-scale distributed systems, formal software architecture experience, native mobile development (iOS/Android)

### 2. Experience Match (0-100)
Does work history align with what they're looking for?

| Score | Meaning |
|-------|---------|
| 80-100 | Direct experience in the same domain and role type |
| 60-79 | Related experience, transferable skills clear |
| 40-59 | Adjacent experience, would need to make the case |
| 0-39 | Unrelated experience |

**Strong:** Full-stack SaaS development (Connfit), production automation/integration work (Kodama)
**Moderate:** Technical consulting/client scoping, B2B client-facing technical sales, teaching/curriculum design
**Entry-level:** Never held a formally-titled "Junior Developer" role at a company (path so far is self-taught + co-founder + freelance-style consulting) - a real gap for postings that specifically screen for a prior "junior developer" job title, even though the shipped production work is substantial

### 3. Behavioral/Culture Fit (0-100)
Does the role and company culture match the behavioral profile?

| Score | Meaning |
|-------|---------|
| 80-100 | Culture strongly matches behavioral preferences |
| 60-79 | Mixed signals but mostly compatible |
| 40-59 | Some friction areas |
| 0-39 | Significant culture mismatch |

**Red flags to research:** Department disorganization, work dominated by maintenance over development, poor chemistry with leadership, culture mismatches. Check reviews, media coverage, LinkedIn connections, and network contacts for insider perspective.

### 4. Location & Logistics (Pass/Fail + Notes)
- Fully remote, any country/timezone: PASS (primary target)
- Remote but restricted to residents/citizens of a specific country/region the candidate doesn't hold: FLAG (check visa/work-authorization requirement before proceeding)
- Requires relocation from Pato Branco, PR, Brazil: FAIL (deal-breaker)
- On-site or hybrid role based in Brazil: FLAG (not the current search focus, but not automatically excluded - discuss with user if the opportunity is compelling)

### 5. Career Alignment & Motivation (0-100)
Does this role advance career goals and contain tasks that energize?

| Score | Meaning |
|-------|---------|
| 80-100 | Strongly aligned with career direction, clear growth path |
| 60-79 | Good role but only partially aligned with long-term goals |
| 40-59 | Decent job but doesn't build toward career goals |
| 0-39 | Dead end or backwards step |

**Career goals:**
- Land a first formally-titled Junior Full-Stack or Junior Front-End Developer role, ideally remote and international, to build recognized team-based experience beyond the self-taught/co-founder path
- Maximize learning velocity - prefers exposure to multiple projects/domains at once over a single narrow track
- Build confidence and depth in technical English communication (architecture discussions specifically)
- Keep freelance/contract work (Workana, Upwork, similar) as a parallel or interim income source while pursuing a full-time remote role

**Motivation filter:** Evaluate not just whether you *can* do the tasks, but whether the tasks will *energize* you. Consider:
- Tasks that energize: creative technical problem-solving, cross-functional work connecting code to client/business needs, learning new stacks or domains, short-cycle work with visible output
- Tasks that drain: constant project-switching without ever shipping, no room for creative input on the solution, no visible path to grow
- Non-task factors: direct/frequent feedback, mentorship availability, degree of autonomy on how a problem gets solved

**Life situation alignment:** Consider personal constraints:
- **Security**: Needs paid income now; explicitly willing to adapt to larger, more structured/corporate environments purely for pay and stability if a smaller-team fit isn't available
- **Flexibility**: Based in Pato Branco, PR, Brazil; not relocating; open to any country/timezone for a remote role
- **Professional development**: Prioritizes gaining a formally-titled "junior" role and deepening technical English and software architecture knowledge over immediate compensation

### 6. Salary Benchmark (Optional)

If the salary lookup tool is configured (`salary_data.json` exists), look up the company:
```
python salary_lookup.py "<Company Name>" --json
```

If a city is known from the posting, add `--city "<City>"` to narrow results.

Present findings as:
```
### Salary Benchmark
| Metric | Value |
|--------|-------|
| [Category] index | XX.X (+/-X.X% vs baseline) |
| Overall index | XX.X (+/-X.X% vs baseline) |
```

Interpret results relative to the baseline defined in the data file's metadata. For index-based data, higher typically means above-market compensation.

If the salary tool is not configured, skip this section.

## Output Format

Present the evaluation as:

```
## Job Fit Evaluation: [Role] at [Company]

| Dimension | Score | Notes |
|-----------|-------|-------|
| Technical Skills | XX/100 | [brief note] |
| Experience Match | XX/100 | [brief note] |
| Behavioral Fit | XX/100 | [brief note] |
| Location | PASS/FAIL | [brief note] |
| Career Alignment | XX/100 | [brief note] |

**Overall Score: XX/100** (weighted average of scored dimensions)

### Verdict: [Strong Fit / Good Fit / Moderate Fit / Weak Fit / Poor Fit]

### Key Strengths for This Role
- [bullet points]

### Gaps to Address
- [bullet points]

### Recommendation
[1-2 sentences: apply/skip/apply with caveats]

### Company Research Checklist
- [ ] Checked company website (mission, values, recent news)
- [ ] Checked review sites (Glassdoor, Jobindex, etc.)
- [ ] Checked LinkedIn for team size, recent hires, connections
- [ ] Checked media for restructuring, growth, or workplace issues
- [ ] Identified network contacts who may know the team/manager
```

## Weighting
- Technical Skills: 30%
- Experience Match: 25%
- Behavioral Fit: 15%
- Career Alignment: 30%

(Location is pass/fail, not weighted)

## Thresholds
- **Strong Fit** (75+): Definitely apply, tailor everything
- **Good Fit** (60-74): Apply, address gaps in cover letter
- **Moderate Fit** (45-59): Consider carefully, discuss with user
- **Weak Fit** (30-44): Probably skip unless strategic reasons
- **Poor Fit** (<30): Skip

## Pre-Application: Call the Employer (Best Practice)

Before writing the application, consider whether the candidate should call the contact person listed in the posting. **Only call if there are substantive questions** - never call just to "be remembered."

### When to Suggest Calling
- The posting has unclear or ambiguous requirements
- It's unclear which competencies are essential vs. nice-to-have
- The role description is vague about day-to-day tasks
- There's a named contact person who invites questions

### Good Questions to Ask
- "What are the primary challenges in this role?"
- "How is time typically divided across the listed responsibilities?"
- "Which competencies are most critical for success in this position?"
- "What does success look like in the first 6-12 months?"

### Rules for the Call
- Prepare a 30-second "elevator pitch" about your background in case they ask
- The call's purpose is **gathering information**, not delivering a pitch
- Take notes - use what you learn to tailor the application
- Reference the conversation naturally in the cover letter ("After speaking with [name], I was especially drawn to...")
