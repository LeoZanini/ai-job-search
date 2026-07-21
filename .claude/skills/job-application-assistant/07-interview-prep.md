# Interview Preparation Guide

<!-- SETUP: STAR examples are personalized by running /setup based on your actual experience -->

## STAR Format

Structure answers as: **Situation** (context), **Task** (your responsibility), **Action** (what you did), **Result** (outcome).

Keep answers to 1-2 minutes. Be specific. End with what you learned or would do differently.

## Ready-Made STAR Examples

### 1. Rebuilding the Connfit scheduling engine (ownership, iterating from user feedback)
**S:** Co-founded Connfit, a SaaS platform for nutritionists. The initial scheduling engine didn't match how nutritionists actually managed patient availability and bookings in practice.
**T:** As the engineer owning roughly half the codebase, responsible for redesigning the scheduling engine so it could scale with real customer workflows instead of assumptions.
**A:** Rebuilt the engine from scratch twice, each time grounding the redesign in structured one-on-one interviews with 50-70 nutritionists (30-60 minutes each, controlled script) before touching the architecture.
**R:** Shipped a scheduling system that supported 100+ registered users and helped convert 4 paying customers at R$279-350/month.
**Use for:** "Tell me about a time you had to rebuild something that wasn't working", "ownership", "using user feedback to drive technical decisions"

### 2. Building Vek1 at Kodama (initiative, technical tradeoffs)
**S:** Kodama wanted to offer WhatsApp automation to clients without waiting on the limitations of the official Meta Business API.
**T:** Build and package a resellable automation product on top of a free, open WhatsApp platform.
**A:** Built an integration using Evolution API and N8N, wrapped in custom UI/UX, self-hosted in Docker on a VPS, and launched it as its own product, Vek1 (vek1.com.br). Later migrated clients to the official Meta Business Suite API as requirements matured.
**R:** Created a standalone product line generating revenue independent of Kodama's core consulting work, and learned firsthand the tradeoffs between an unofficial integration and an official platform API.
**Use for:** "Tell me about a project you built end-to-end", "initiative", "a technical decision with tradeoffs"

### 3. Scoping client work at Kodama (ambiguous requirements, stakeholder communication)
**S:** Kodama's B2B clients often came in with vague requests ("automate our WhatsApp", "we need a CRM") without a clear scope.
**T:** Lead around 2 client meetings per week, turning open-ended asks into scoped, shippable projects.
**A:** Mapped each client's business process in detail, diagnosed whether they actually needed automation, a CRM, or something else, confirmed the direction with them, then scoped a step-by-step implementation plan capped at 5-6 screens for a compact first release, expanding later as trust was established.
**R:** Established a repeatable pattern for turning ambiguous sales conversations into scoped technical delivery, avoiding over-built first releases.
**Use for:** "How do you handle ambiguous requirements", "communicating with non-technical stakeholders", "scoping a project"

### 4. Teaching the AI Technician curriculum at SENAC (fast learning, explaining technical topics)
**S:** SENAC needed an instructor for a 1200-hour AI Technician program covering Python, AI fundamentals, computer architecture (CPU/GPU), databases, and statistics, for 30 high school students.
**T:** Design and deliver hands-on exercises across a technical curriculum that extends well beyond a mechanical engineering background.
**A:** Self-taught and structured teaching materials spanning CPU/GPU architecture to statistics, translating dense technical concepts into practical, hands-on exercises for students with no prior programming background.
**R:** Currently teaching 30 students; also building an agent-driven infrastructure for automated lesson/exercise generation using hierarchical LLM orchestration.
**Use for:** "Explain something technical to a non-expert", "learning something new quickly", "teaching or mentoring"

<!-- Add more STAR examples as needed. Aim for 4-6 covering different competencies. -->

## Common Tough Questions

### "Why did Connfit end?"
> "Connfit set out to build patient-management software for nutritionists. Over 18 months I wrote most of the codebase and we reached 100+ registered users and 4 paying customers, but the structured interviews we ran with 50-70 nutritionists made clear the product hadn't found strong market fit. We made the call to wind it down rather than keep pushing on something the data didn't support. It's the reason I want to bring that full-stack and product experience into a team where I can focus purely on the engineering craft."

### "Why are you looking to leave your current role?"
> "At Kodama I've owned automation products end-to-end, including client scoping and B2B sales, which taught me a lot about connecting engineering to real business needs. What I want next is a role that's purely software engineering, on a team with more experienced developers I can learn architecture and best practices from."

### "You don't have a Computer Science degree or a prior 'Junior Developer' title."
> "My degree is in Mechanical Engineering, and I moved into software by teaching myself and then shipping it in production: I wrote roughly half the codebase for a SaaS platform that reached 100+ users and paying customers, and I currently build and ship automation products for B2B clients. I don't have the CS coursework, but I have real production experience and I'm looking for a team environment to fill in the formal gaps, like deeper architecture patterns, faster."

### "Where do you see yourself in 5 years?"
> "Growing from a junior into a strong mid-level full-stack or frontend engineer, likely specializing further in AI-driven product engineering. I want the next few years to be about building formal, team-based experience on top of what I've already shipped on my own."

### "What's your biggest weakness?"
> "Technical English at the depth needed for in-depth architecture discussions. I've worked in English for 7+ years professionally, but going deep on system design in a second language is still something I'm actively sharpening, partly by working through technical material in English and partly by seeking out teams where I'll get that practice regularly."

### "Why this company specifically?"
> Customize per company. Must reference: specific projects, company values, market position, or team structure. Never give a generic answer.

## Questions You Should Ask Interviewers

### About the Role
- "What does a typical week look like in this role?"
- "What would success look like in the first 6 months?"
- "What's the biggest challenge the team is facing right now?"

### About the Team
- "How big is the team, and how do you divide work?"
- "What does the development/project lifecycle look like, from idea to production?"
- "How do you onboard new team members?"

### About Tech & Growth
- "What's your current tech stack for [relevant area]?"
- "Is there room to grow into more architectural or strategic decisions?"
- "How does the team stay current with new tools and methods?"

### About Culture (use these to prevent disappointment)
- "How would you describe the team culture?"
- "What does professional development look like here?"
- "Is there flexibility for remote/hybrid work?"
- "What's the balance between development/new projects and maintenance work?"
- "How would you describe the leadership style in this team?"
- "What do people who thrive here have in common?"

## Phone/Video Interview Tips
- Have STAR examples written out (use this file)
- Keep a glass of water nearby
- Smile when speaking (it changes your tone)
- Ask for clarification if a question is vague
- It's OK to take 5 seconds to think before answering
- End with: "Is there anything else you'd like to know about my background?"

## After the Application (Best Practice)

### Follow-Up Etiquette
- **Don't call to "stand out"** or to learn more about the role post-submission - this risks a negative impression
- If the employer specified a timeline, respect it and wait
- If no timeline was given and significant time has passed (2+ weeks), a brief call to ask about status is acceptable
- If you have genuinely new, relevant information to share, a short follow-up is fine

### Thank-You Notes
- When you receive any update (interview invitation, rejection, or status update), send a brief thank-you message
- Express appreciation for their time and the process
- Keep it short (2-3 sentences)

## Roleplay Guidelines
When the user asks for interview practice:
1. Ask which role/company to simulate
2. Start with easy warm-up questions ("Tell me about yourself")
3. Progress to role-specific technical questions
4. Include 1-2 behavioral questions using the competencies from the job posting
5. End with a tough question or curveball
6. After each answer, give brief feedback: what worked, what to sharpen
7. Suggest which STAR example would work best for each question
