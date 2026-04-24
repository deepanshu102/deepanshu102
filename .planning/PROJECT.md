# Project: deepanshu102 GitHub Profile Overhaul

## What This Is
A professional transformation of the `deepanshu102/deepanshu102` GitHub profile repository. It aims to tell a coherent technical story that aligns with the premium cyberpunk aesthetic of the [system-architect portfolio](https://deepanshu102.github.io/), positioning Deepanshu Gupta as a Senior Backend Engineer and System Architect.

## Core Value
**Narrative Consistency:** Every signal on the profile (stats, pins, bio, timeline) must reinforce the "Senior Golang/K8s/AWS Architect" narrative and match the portfolio's visual and professional identity.

## Requirements

### Validated
(None yet — ship to validate)

### Active
- [ ] **FR-01: Identity Layer** — Communicate seniority (5.2+ years), stack, and availability in the first viewport.
- [ ] **FR-02: Stack Visibility** — Implement a visual badge row for core technologies (Go, K8s, gRPC, AWS, Node.js).
- [ ] **FR-03: Experience Timeline** — Add a compact, accurate career table matching the portfolio.
- [ ] **FR-04: Language Optimization** — Configure stats cards to hide legacy C/C++ data and prioritize Golang.
- [ ] **FR-05: Visual Theme** — Use `tokyonight` theme across all stats cards for cyberpunk alignment.
- [ ] **FR-06: Connectivity** — Prominent links to portfolio, LinkedIn, and Email.
- [ ] **FR-07: Pinned Repository Strategy** — Curation of 6 high-impact repos demonstrating distributed systems and cloud expertise.

### Out of Scope
- Portfolio site modifications (handled in separate project).
- LinkedIn profile automation.
- Automated README generation scripts (manual Markdown is preferred for control).

## Context
- The user is currently a Senior Software Engineer at Kairos Technologies.
- The user has 61 public repositories, many of which are legacy student projects inflating language stats.
- The portfolio uses a "Technical HUD" aesthetic which the README must approximate using Markdown-compatible components.

## Constraints
- **Markdown-Only**: No custom CSS or JavaScript allowed in GitHub Profile README.
- **Service Dependency**: Relies on `github-readme-stats` for dynamic data.

## Key Decisions
| Decision | Rationale | Outcome |
|----------|-----------|---------|
| Manual Initialization | Environment restrictions on GSD tools | — Pending |
| Archive Legacy Repos | Improve language stats without deleting history | — Pending |
| Static Timeline | Low maintenance burden and high reliability | — Pending |

## Evolution
This document evolves at phase transitions and milestone boundaries.

**After each phase transition:**
1. Requirements invalidated? → Move to Out of Scope
2. Requirements validated? → Move to Validated
3. New requirements emerged? → Add to Active

---
*Last updated: April 2026 after project initialization*
