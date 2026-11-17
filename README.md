# AI for Decision Makers – My Job Search Team of Agents

**Course:** ISM 6427C – Business Innovations with Artificial Intelligence (FAU)
**Student:** Aaliyah Yuldasheva

## The idea
In class we created **job skills** (finding jobs on Indeed/Dice, FAU campus jobs, tailoring a resume and cover letter). This project turns those skills into a team of **synthetic employees**: Claude Code sub-agents that are each an expert in one part of the job search. They work together on one decision: *"Should I apply for this job, and how do I win it?"*

## The team (`.claude/agents/`)
| Agent | Role |
|---|---|
| `career-strategist-lead` | Team lead. Splits the question, sends parts to specialists and combines their answers into one bottom line |
| `hr-recruiter` | Judges fit the way a real recruiter or ATS would |
| `resume-reviewer` | Tailors the resume and writes the cover letter (edits, never invents) |
| `interview-coach` | Likely interview questions and STAR answers |
| `fau-campus-scout` | Finds and checks FAU on-campus jobs |
| `work-rules-checker` | The skeptic. Flags whether a job fits student work rules (on-campus, CPT, OPT, W2 vs 1099) |

## Skills the agents use (`.claude/skills/`)
`job-board`, `fau-campus-jobs`, `resume-cover-letter-tailor`, `cover-letter-writer`. These are the skills I built in class, which the agents follow.

## How to use it
1. Open this repo in Claude Code.
2. Ask a question, for example:
   - "Use the career-strategist-lead. Here is a job posting: [paste]. Should I apply? Have the recruiter, resume reviewer and work-rules checker each weigh in, let them respond to each other, then give me the bottom line."
   - "fau-campus-scout: find 3 social on-campus FAU jobs open to grad students, then have the work-rules-checker check each one."
   - "interview-coach and hr-recruiter: I have an interview for an HR Assistant role tomorrow. Prepare me, and have the recruiter tell me what they'd be looking for."
   - "hr-recruiter, you said my fit is a 3. Resume-reviewer, what would make it a 5?"

## Why it's useful
Instead of one general chatbot, I get a small panel of experts who check each other. For example, the recruiter may love a job while the work-rules checker blocks it. The lead then gives me a single decision and next steps. I can reuse the same team for every job I consider.
