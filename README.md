# Job Search NA — Product Management Edition

A Claude Code skill that automates job searching for **Product Management professionals** in the **United States and Canada**.

Adapted from [mayankjoshii/claude-job-skill](https://github.com/mayankjoshii/claude-job-skill) (India Edition) — rebuilt for North American PM roles, platforms, and hiring norms.

## What It Does

- Searches **12+ North American job platforms** (LinkedIn, Indeed, Glassdoor, Otta, BuiltIn, Wellfound, Levels.fyi, ProductHired, Mind the Product, Y Combinator, Dice, Hired)
- Scores each role against your PM profile (skills, experience, domain, seniority, product type)
- Generates **ATS-optimized PM resumes** tailored to each specific job description
- Writes **targeted cover letters** referencing each company's product strategy
- Tracks all applications in `job_tracker.xlsx` with status flow and follow-up reminders
- Connects to Gmail to auto-detect interview invites, rejections, case study assignments, and offers
- Runs **nightly automated searches** and delivers morning reports
- Self-corrects strategy based on rejection patterns (ATS gaps, level mismatches, case study failures)

## Installation

Copy the `job-search-na/` folder into your Claude Code skills directory:

```
~/.claude/skills/job-search-na/
├── SKILL.md      # Skill definition (Claude Code reads this)
└── README.md     # This file
```

Claude Code will auto-detect the skill on next launch.

## Commands

| Command | Description |
|---------|-------------|
| `/job-search-na help` | Show usage guide and all capabilities |
| `/job-search-na search` | Search all platforms, score matches, generate materials |
| `/job-search-na automate` | Set up nightly automated job search pipeline |
| `/job-search-na status` | Check application status (Gmail or manual) |

You can also use natural language:
- "Find me Senior PM jobs in Seattle"
- "Search for Group PM roles in NYC, $250k+ TC"
- "What's the status of my applications?"

## First Run

On first use, the skill collects your profile:
1. **Resume** — upload PDF/DOCX/text, it extracts your PM experience, skills, and tools
2. **Preferences** — target roles (PM, Senior PM, GPM, Director, VP), locations, company types, seniority
3. **Optional** — salary range, industries, deal-breakers, visa status

Your profile is remembered for the session — you won't be asked again.

## Platforms Searched

| # | Platform | Best For |
|---|----------|----------|
| 1 | LinkedIn | Largest PM board, recruiter activity |
| 2 | Indeed | High volume aggregator |
| 3 | Glassdoor | Salary data + reviews |
| 4 | Otta | Curated startup PM roles |
| 5 | BuiltIn | Tech companies, startups |
| 6 | Wellfound | Funded startups, equity |
| 7 | Levels.fyi | Comp-transparent, big tech |
| 8 | ProductHired | PM-specific board |
| 9 | Mind the Product | PM community board |
| 10 | Y Combinator | YC-backed startups |
| 11 | Dice | Tech-focused roles |
| 12 | Hired | Reverse marketplace |
| 13 | Direct career pages | FAANG, Stripe, Shopify, etc. |

## Target Companies

- **FAANG/Big Tech**: Google, Meta, Amazon, Apple, Microsoft, Netflix
- **Growth Tech**: Stripe, Airbnb, Databricks, Figma, Notion, Canva, Plaid, Ramp, Brex, Rippling
- **Enterprise SaaS**: Salesforce, ServiceNow, Datadog, Snowflake, Confluent, HashiCorp, MongoDB
- **Canadian Tech**: Shopify, Wealthsimple, Clio, Hootsuite, 1Password, Lightspeed
- **Fintech**: Square/Block, Robinhood, Chime, SoFi, Affirm, Coinbase

## Fitness Scoring

Each role is scored 0–100% based on:

| Factor | Weight |
|--------|--------|
| PM skills overlap | 3x |
| Years of PM experience | 2x |
| Domain relevance | 2x |
| Seniority alignment | 2x |
| Product type match (B2B/B2C/platform) | 1x |
| Education/MBA fit | 1x |

- **80%+** = Strong fit
- **60-79%** = Moderate fit (worth applying)
- **<60%** = Stretch (flagged)

## Resume Format (US/Canada)

- 1 page maximum
- No photo, no personal details
- Impact metrics on every bullet (revenue, adoption, NPS, retention)
- PM sections: Product Impact Summary → Experience → Skills → Education
- ATS keyword match >= 70% against each JD

## Credits

- Original skill: [mayankjoshii/claude-job-skill](https://github.com/mayankjoshii/claude-job-skill) (India Edition)
- Adapted by: Ali Khan (PM-Ali)
- Built with: Claude Code

## License

MIT
