# Job Application Assistant for Leonardo Zanini Niclote

## Role
This repo is a job application workspace. Claude acts as a career advisor and application assistant for Leonardo Zanini Niclote, helping with:
1. **Job fit evaluation** - Assess job postings against your profile (skills, experience, behavioral traits)
2. **CV tailoring** - Adapt existing CV templates (LaTeX/moderncv) to target specific roles
3. **Cover letter writing** - Draft targeted cover letters using existing templates (LaTeX)
4. **Interview preparation** - Prepare answers, questions, and talking points for interviews
5. **Career strategy** - Advise on positioning and personal branding

## Candidate Profile

### Identity
- **Name:** Leonardo Zanini Niclote
- **Location:** Pato Branco, Paraná, Brazil (not relocating; targeting fully remote roles internationally, any country/timezone)
- **Languages:** Portuguese (native), English (7+ years professional working proficiency)
- **Status:** Employed (Kodama - full stack & automation, ongoing; SENAC - AI instructor, ongoing), actively job-searching for a remote international junior full-stack/frontend role
- **LinkedIn headline:** "Full-Stack Web Developer | AI Technician Instructor at SENAC"

### Education
- **Bachelor of Mechanical Engineering** - UTFPR, Pato Branco, PR, Brazil
  - Topics: Mechanical design, manufacturing processes

### Professional Experience
- **AI Technician Instructor** (Feb 2026 - Present) - **SENAC** (Pato Branco, PR, Brazil)
  - Teaching 30 high school students in a 1200-hour AI Technician program (Python, AI fundamentals, computer architecture, databases, statistics)
  - Building an agent-driven infrastructure for automated lesson/exercise generation using hierarchical LLM orchestration
- **Co-Founder, Software Engineer & Product Strategist** (Feb 2024 - Mar 2026) - **Connfit** (Brazil, remote/distributed)
  - Wrote ~50% of the codebase (React, Next.js, Tailwind CSS, Supabase, PostgreSQL, Prisma, N8N, Docker) for a nutritionist SaaS platform
  - Reached 100+ registered users and 4 paying customers; concluded, via structured interviews with 50-70 nutritionists, that the product lacked strong market fit and wound the venture down
- **Full Stack Developer & Automation Specialist** (Sep 2023 - Present) - **Kodama** (Brazil, remote/distributed)
  - Built and resold a WhatsApp automation product (Vek1) using Evolution API + N8N; later migrated to the official Meta Business Suite API
  - Leads B2B consultative sales and technical scoping for automation clients; mentors a junior developer
- **Programming Logic Instructor** (Mar 2024 - Apr 2024) - **SENAC** (Pato Branco, PR, Brazil)
  - Taught 22 students JavaScript fundamentals in a 50-hour course
- **Junior Project Analyst** (2022 - 2023) - **Atlas Eletrodomésticos** (Brazil)
  - Engineering optimization and 2D/3D mechanical design (SolidWorks, ISO 9001) - prior to the pivot into software

### Technical Skills
- **Primary:** TypeScript/JavaScript, React, Next.js, Tailwind CSS, Node.js
- **Secondary:** Python, SQL/PostgreSQL, Prisma, Supabase, REST APIs, GraphQL, Docker, N8N, GitHub Actions, Vercel, Jest, Playwright
- **Domain:** SaaS product development, WhatsApp/business messaging automation, LLM/AI agent integration, B2B consultative technical sales, LGPD compliance
- **Software:** Supabase, Docker, N8N, Vercel, GitHub Actions, SolidWorks (legacy, from mechanical engineering background)

### Certifications
- **JavaScript Programming** - Codecademy (date not specified in source CV)
- **Web Development** - Udemy (date not specified in source CV)

### Publications
Not applicable.

### Awards
Not applicable.

### Behavioral Profile
<!-- Self-assessment, no formal instrument on file. See 02-behavioral-profile.md for full detail. -->
- **Adaptability** - Moved from mechanical engineering into self-taught full-stack dev, product strategy, and B2B sales; comfortable flexing into larger/more structured environments for stability if needed
- **Multidisciplinary bridge-builder** - Understands both the code and the client/business side, not just engineering in isolation
- **Strengths:** Fast domain-switching, shipping production systems solo/co-founder-style, actively seeking and welcoming direct feedback
- **Growth areas:** Deep technical English for architecture discussions; broader exposure to software architecture patterns beyond self-teaching
- **Thrives in:** Small, high-autonomy teams with short delivery cycles and frequent, direct feedback; prefers an execution-first role for now to build depth before returning to more ownership/leadership

### What Excites You
- Building products end-to-end and owning the full stack from database to deployment
- Teaching/mentoring others and bridging technical work with client/business needs
- Learning new stacks and domains quickly, and working on multiple projects at once

### Target Sectors
- Remote-first tech/SaaS startups (any country) hiring junior full-stack or frontend developers
- AI/automation tooling companies and agencies (adjacent to current work at Kodama)
- Freelance/contract platforms (Workana, Upwork) as parallel or interim income

### Deal-breakers
- Requiring relocation away from Pato Branco, PR, Brazil
- Strictly on-site-only roles (current search is remote-first)

## Repo Structure
- `cv/` - LaTeX CV variants (moderncv template, banking style)
- `cover_letters/` - LaTeX cover letters (custom cover.cls template)
- `.claude/skills/` - AI skill definitions for the application workflow
- `.agents/skills/` - Job search CLI tools

## Workflow for New Job Applications
1. User provides a job posting (URL or text)
2. **Always evaluate fit first**: skills match, experience match, behavioral/culture match. Present this assessment to the user before proceeding.
3. If good fit: create targeted CV (`cv/main_<company>.tex`) and cover letter (`cover_letters/cover_<company>_<role>.tex`)
4. **Verify both documents** (see Verification Checklist below)
5. Prepare interview talking points based on the role requirements and your strengths

**Important:** When mentioning agentic coding or AI tooling in CVs/cover letters, explicitly reference **Claude Code** by name.

## Verification Checklist
After creating or updating a CV or cover letter, re-read the generated file and verify **all** of the following before presenting to the user. Report the results as a pass/fail checklist.

### Factual accuracy
- [ ] All claims match actual profile (CLAUDE.md / candidate profile) - no fabricated skills, experience, or achievements
- [ ] Job titles, dates, company names, and locations are correct
- [ ] Contact details are correct
- [ ] All company-specific claims (partnerships, products, technology, expansions) have been independently verified via WebFetch/WebSearch - do not trust reviewer agent research without verification

### Targeting
- [ ] Profile statement / opening paragraph is tailored to the specific role (not generic)
- [ ] Skills and experience bullets are reframed to match the job requirements
- [ ] Key job requirements are addressed (with gaps acknowledged where relevant)
- [ ] Nice-to-have requirements are highlighted where there is a match

### Consistency
- [ ] CV follows the standard 2-page moderncv/banking format
- [ ] Cover letter uses cover.cls template and established structure
- [ ] Tone is consistent across CV and cover letter
- [ ] No contradictions between CV and cover letter content

### Quality
- [ ] No LaTeX syntax errors (balanced braces, correct commands)
- [ ] No spelling or grammar errors
- [ ] Agentic coding / AI tooling references mention **Claude Code** by name
- [ ] Cover letter is addressed to the correct person (or "Dear Hiring Manager" if unknown)
- [ ] Cover letter fits approximately one page

### Compiled PDF verification (MANDATORY - never skip)
Both documents MUST be compiled and visually inspected via the Read tool on the PDF output. "Looks fine in the .tex" is not acceptable - LaTeX page-break decisions are unpredictable. Iterate until these all pass:
- [ ] CV compiled with **lualatex** (pdflatex often fails on modern MiKTeX with fontawesome5 font-expansion errors). Cover letter compiled with **xelatex** (cover.cls requires fontspec).
- [ ] **CV is exactly 2 pages** - not 1, not 3
- [ ] **No orphaned `\cventry` titles** - a job/education title must never sit at the bottom of a page with its bullets spilling to the next page. Use `\needspace{5\baselineskip}` before each `\cventry` to prevent this, and `\enlargethispage{2-3\baselineskip}` to rescue a trailing section that just barely spills
- [ ] **Cover letter is exactly 1 page** - signature block must fit with the body, never overflow
- [ ] **Cover letter bullet font matches body font** - `\lettercontent{}` must not wrap `\begin{itemize}...\end{itemize}` (the command's trailing `\\` errors on `\end{itemize}`, and moving itemize outside loses the Raleway font). Standard pattern: close `\lettercontent{}`, then wrap the list in `{\raggedright\fontspec[Path = OpenFonts/fonts/raleway/]{Raleway-Medium}\fontsize{11pt}{13pt}\selectfont \begin{itemize}...\end{itemize}\par}`

### ATS & keyword verification (CV)
ATS parsers read the PDF's embedded text layer, not the rendered page. Extract it with `pdftotext -layout` and verify what a parser sees. `pdftotext` (poppler) is optional - if missing, skip the parseability items with a warning and check keyword coverage from the visual PDF read instead.
- [ ] CV text layer extracts cleanly - no `(cid:*)` markers, `�` replacement characters, or text visible in the PDF but absent from the extraction
- [ ] Email and phone appear as **literal text** in the extraction (icon-glyph noise like `MOBILE-ALT`/`Envelope` is harmless, but a contact detail carried only by an icon or hyperlink is invisible to ATS)
- [ ] Reading order of the extracted text matches the visual order (single-column stock template is safe; multi-column custom templates are where this breaks)
- [ ] Posting keywords covered or honestly absent - synonym-only matches tightened to the posting's exact term where truthfully applicable, keywords the profile genuinely supports added to experience bullets, genuine gaps left visible and **never stuffed**
