# 🛡️ CyberHunt AI — Cybersecurity Job Intelligence Platform

> Built by a cybersecurity job seeker who got tired of hearing "no experience."  
> So I spent two months building the tool I wished existed.

**🔴 Live demo:** https://drukson.github.io/cyberhunt-ai

---

## The problem this solves

Every cybersecurity job asks for 2 years SOC experience.  
But you cannot get SOC experience without the job.  
CyberHunt AI breaks that loop.

It reads the job description, reads your resume, understands the gap,  
and produces a tailored resume, cover letter, and recruiter outreach message  
that honestly bridges your experience to what the employer needs —  
without fabricating a single credential.

---

## What it does

### 🔍 Job Discovery
- Fast search using Haiku AI — instant, no rate limits
- Real job search using web search tool — finds actual Seek and LinkedIn listings
- 10-dimension fit scoring per job (role match, skills, experience, tech stack, culture, growth, salary, location, career alignment, interview probability)
- A/B/C/D grade system with honest fit reasons
- Direct apply links to Seek, LinkedIn, Indeed

### 🤖 12-Agent Pipeline (the core)
All agents run with retry logic. A1→A2→A3 are sequential (each feeds the next). A4–A11 run in parallel. A12 is the final gate.

| Agent | Role | Output |
|-------|------|--------|
| A1 | Job Decoder | ATS keywords, tool requirements, bridge strategies |
| A2 | Resume Analyst | Skills confirmed, gaps identified, editorial decisions |
| A2.5 | Career Transition Intelligence | Current role → target role narrative, transition type, summary opening line |
| A3 | Resume Assembler | Full tailored resume — unrelated jobs removed, cyber reframing applied, zero repetition |
| A4 | Cover Letter Specialist | Role-change focused, company-specific, never templated |
| A5 | STAR Story Extractor | 4-6 behavioural interview stories added to persistent bank |
| A6 | Career Mentor | 30-day action plan, cert roadmap, gap question scripts |
| A7 | Company Intelligence | Pre-interview briefing, tech stack, culture, smart questions |
| A8 | Recruiter Outreach | LinkedIn connection + InMail + cold email messages |
| A9 | Cert & Learning Planner | Gap-specific cert roadmap with free resources |
| A10 | Follow-Up Sequence | 3-email sequence: day 3, post-interview, 2-week nudge |
| A11 | Salary Negotiation | AU market rates, negotiation scripts, counter-offer framework |
| A12 | ATS Auditor | Final score, keyword density check, bridge phrase credibility validation |

### 📝 Resume Intelligence
- Reads entire resume (not truncated) — understands full work history
- Career transition type detection: CAREER_CHANGE / PROMOTION / LATERAL / SPECIALISATION
- Removes unrelated jobs entirely (food service, retail) — keeps focus
- Reframes IT/network experience through security lens
- Skills written with practical usage: "Wireshark – Captured and analysed network traffic to identify protocol anomalies..."
- Projects positioned as key differentiator for entry-level candidates

### ✉️ Cover Letter
- Role-change focused narrative
- Company-specific — references what they actually do
- Never starts with "I am writing to express my interest"
- 5-paragraph structure matching Australian recruitment standards
- 350-420 words — professional, not padded

### 🎤 AI Mock Interview
- Plays a real interviewer (SOC Manager, Security Analyst, CISO)
- 8 questions per session, scored in real-time
- Shows what was missed and a stronger model answer
- Tracks improvement across sessions

### 🧠 Career Mentor
- Knows your resume, gaps, and STAR bank
- Ask anything — bridge questions, cert advice, salary, mindset
- Sharpens every session from memory

### 💬 Outreach Suite
- Human story generator — emotionally resonant, genuine
- LinkedIn connection message, InMail, cold email, follow-up
- Auto-generated from results in one click

### 📊 Tracking & Intelligence
- Application pipeline tracker: Applied → Phone Screen → Interview → Offer
- Success dashboard — which ATS scores correlate with interviews
- Market intelligence with live web search
- Cert ROI calculator
- Batch job search

### 🔵 LinkedIn Optimizer
- 3 headline options with character counts
- Full About section rewrite — first-person, keyword-rich, hook opening
- Auto-generated from results after 12 agents complete
- Profile update checklist with High/Medium priorities

---

## How to use

1. Open **https://drukson.github.io/cyberhunt-ai**
2. Get a free Anthropic API key at **console.anthropic.com** (no credit card required to start)
3. Enter your API key in the top right bar and click Save
4. **Recommended workflow:**
   - Go to **Paste Job URL** tab → browse Seek for free → copy the job description →
