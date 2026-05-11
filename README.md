> **AI Agency Command Center for Claude Code** — orchestrates multiple AI teams (Marketing, Sales, Legal, GEO/SEO) into a unified agency workflow. 8 skills, 5 parallel agents, composite scoring, and professional PDF reports.

Type one command. Multiple parallel AI agents audit a business simultaneously. You get a unified score, prioritized findings, and a client-ready proposal with pricing tiers.

Built for agency owners, freelancers, and consultants who want to sell AI-powered services to real businesses.

---

## What Is This?

The AI Agency Command Center is an orchestration layer that sits on top of specialized AI tool suites for Claude Code. It coordinates Marketing, Sales, Legal, and GEO/SEO analysis into a single unified command — letting you run a full-service AI agency from your terminal.

```
> /agency onboard https://example-business.com

Phase 1 — Discovery...
Phase 2 — Launching parallel audit teams...
  ✓ Marketing Agent        — Score: 62/100
  ✓ GEO/SEO Agent          — Score: 71/100
  ✓ Legal Compliance Agent  — Score: 38/100
  ✓ Sales Intelligence Agent — Score: 78/100

Agency Composite Score: 62/100 (Grade: B)

Full report saved to AGENCY-ONBOARD-ExampleBusiness.md
```

---

## Architecture

```
                          /agency onboard <url>
                                  │
                        ┌─────────┴─────────┐
                        │   DISCOVERY PHASE  │
                        │  Fetch + Extract   │
                        └─────────┬─────────┘
                                  │
              ┌───────────┬───────┼───────┬───────────┐
              ▼           ▼       ▼       ▼           ▼
        ┌──────────┐ ┌────────┐ ┌─────┐ ┌─────┐ ┌────────┐
        │MARKETING │ │  SALES │ │LEGAL│ │REPU-│ │GEO/SEO │
        │  AGENT   │ │ AGENT  │ │AGENT│ │TATION│ │ AGENT  │
        │  (25%)   │ │ (20%)  │ │(15%)│ │(20%) │ │ (20%)  │
        └────┬─────┘ └───┬────┘ └──┬──┘ └──┬───┘ └───┬────┘
             │           │        │       │          │
             └───────────┴────┬───┴───────┴──────────┘
                              ▼
                    ┌─────────────────────┐
                    │  SYNTHESIS ENGINE   │
                    │  Composite Score    │
                    │  Unified Report     │
                    │  Service Proposal   │
                    └─────────────────────┘
                              │
              ┌───────────────┼───────────────┐
              ▼               ▼               ▼
        AGENCY-ONBOARD.md  AGENCY-PROPOSAL.md  AGENCY-REPORT.pdf
```

---

## Commands

| Command | Description | Output |
|---------|-------------|--------|
| `/agency onboard <url>` | Full agency onboard — runs ALL audit teams in parallel | `AGENCY-ONBOARD-[Company].md` |
| `/agency quick <url>` | 60-second agency snapshot across all dimensions | Terminal output |
| `/agency propose <business>` | Generate unified agency proposal from all audit data | `AGENCY-PROPOSAL-[Client].md` |
| `/agency pipeline` | Show full prospect pipeline with composite scores | `AGENCY-PIPELINE.md` |
| `/agency client <name>` | Pull up all existing work for a specific client | Terminal output |
| `/agency status` | Dashboard view of all active clients and pending work | Terminal output |
| `/agency report-pdf` | Generate unified PDF combining all audit scores | `AGENCY-REPORT.pdf` |
| `/agency stack` | Show which tool suites are installed and ready | Terminal output |

---

## The Tool Suites

The Agency Command Center orchestrates these independent tool suites. Each can be installed and used on its own, but the Command Center coordinates them into unified deliverables.

| Suite | Skills | What It Covers | Repo |
|-------|--------|---------------|------|
| AI Marketing Suite | 15 skills | Copy, SEO, funnels, ads, email, conversion | [ai-marketing-team-premium](https://github.com/DamianDanelczyk/ai-marketing-team-premium) |
| AI Sales Team | 14 skills | Company research, decision makers, proposals, outreach | [ai-sales-team-premium](https://github.com/DamianDanelczyk/ai-sales-team-premium) |
| AI Legal Assistant | 14 skills | Contracts, compliance, GDPR, CCPA, ADA, privacy | [ai-legal-team-claude](https://github.com/DamianDanelczyk/ai-legal-team-claude) |
| GEO/SEO Audit Tool | 11 skills | AI search visibility, citability, schema, crawlers | [geo-seo-premium](https://github.com/DamianDanelczyk/geo-seo-premium) |

---

## Scoring Methodology

The Agency Composite Score combines weighted scores from all audit dimensions:

```
Agency Score = (Marketing x 0.25) + (GEO/SEO x 0.25)
             + (Legal x 0.20) + (Sales x 0.30)
```

Each dimension scores 0-100 based on its own audit criteria. The composite produces a unified grade:

### Grade Interpretation

| Score | Grade | Interpretation |
|-------|-------|---------------|
| 85-100 | A+ | Excellent — minor optimizations only |
| 70-84 | A | Strong — some areas need attention |
| 55-69 | B | Average — significant improvement opportunities |
| 40-54 | C | Below Average — multiple critical issues |
| 25-39 | D | Poor — urgent intervention needed |
| 0-24 | F | Critical — fundamental problems across the board |

**Sweet spot for new clients:** Businesses scoring 30-60 (grades C-D) have the most pain and the highest willingness to pay for help.

---

## Service Tier Pricing

The `/agency propose` command generates three-tier proposals automatically:

| Tier | Monthly Price | What's Included |
|------|--------------|-----------------|
| Essentials | $500 - $1,500 | Critical fixes, monthly monitoring |
| Growth | $1,500 - $3,500 | Full marketing optimization, GEO/SEO, monthly strategy calls |
| Full Agency | $3,500 - $7,500 | Complete overhaul across all dimensions, content creation, legal compliance, sales outreach, quarterly reviews |

---

## Use Cases

### Agency Owners
Run multi-dimensional audits on prospects in minutes instead of days. Deliver unified reports that justify premium retainers. Manage your entire pipeline from one interface.

### Freelancers
Expand your service offering from one specialty to multiple without hiring. Use audit data to upsell clients into higher-tier packages. Generate professional proposals that close.

### Consultants
Back your recommendations with data from parallel analysis streams. Produce client-ready PDF reports with composite scoring. Track all prospect and client work in one place.

---

## Installation

### Prerequisites

- Claude Code installed and configured
- Python 3.8+ (for PDF report generation)
- reportlab Python package (`pip install reportlab`)

### Quick Install

```bash
curl -fsSL https://raw.githubusercontent.com/DamianDanelczyk/ai-agency-command-center-premium/main/install.sh | bash
```

### Manual Install

```bash
git clone https://github.com/DamianDanelczyk/ai-agency-command-center-premium.git
cd ai-agency-command-center-premium
chmod +x install.sh
./install.sh
```

### Install Tool Suites

The Command Center works best with all tool suites installed:

```bash
# AI Marketing Suite
curl -fsSL https://raw.githubusercontent.com/DamianDanelczyk/ai-marketing-team-premium/main/install.sh | bash

# AI Sales Team
curl -fsSL https://raw.githubusercontent.com/DamianDanelczyk/ai-sales-team-premium/main/install.sh | bash

# AI Legal Assistant
curl -fsSL https://raw.githubusercontent.com/DamianDanelczyk/ai-legal-team-claude/main/install.sh | bash

# GEO/SEO Audit Tool
curl -fsSL https://raw.githubusercontent.com/DamianDanelczyk/geo-seo-premium/main/install.sh | bash
```

### PDF Report Support

```bash
pip install reportlab
```

---

## Uninstall

```bash
chmod +x uninstall.sh
./uninstall.sh
```

### Check Your Stack

After installing, run `/agency stack` in Claude Code to see which suites are ready.

---

## License

MIT License — see [LICENSE](https://github.com/DamianDanelczyk/ai-agency-command-center-premium/blob/main/LICENSE) for details.

---

<p align="center">
  <strong>Part of the Claude Code Skills Series</strong><br>
  <a href="https://github.com/DamianDanelczyk/ai-marketing-team-premium">AI Marketing Suite</a> ·
  <a href="https://github.com/DamianDanelczyk/ai-sales-team-premium">AI Sales Team</a> ·
  <a href="https://github.com/DamianDanelczyk/ai-legal-team-claude">AI Legal Assistant</a> ·
  <a href="https://github.com/DamianDanelczyk/geo-seo-premium">GEO-SEO</a> ·
  <a href="https://github.com/DamianDanelczyk/ai-ads-strategist-premium">AI Ads Strategist</a> ·
  <strong>Agency Command Center</strong>
</p>
