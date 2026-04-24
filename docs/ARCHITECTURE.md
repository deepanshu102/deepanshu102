# GitHub Profile Architecture
## deepanshu102 — System Architect & Backend Engineer

---

## Overview

This document defines the architecture of the `deepanshu102/deepanshu102` GitHub profile repository. The profile README is the first thing a recruiter, collaborator, or freelance client sees when they click through from the portfolio at `deepanshu102.github.io`. It must tell a coherent technical story in under 10 seconds while being consistent with the portfolio's narrative.

---

## Profile Identity Layer

### Core Signal (What the profile communicates)
- **Seniority:** 5.2+ years, currently Senior Software Engineer at Kairos Technologies
- **Domain:** Backend engineering, distributed systems, cloud-native architecture
- **Primary Stack:** Golang, gRPC, Kubernetes, AWS, Node.js
- **Availability:** Open to freelance — visible in the first section
- **Personality:** Builder mindset, architectural thinker, not just an executor

### Audience Hierarchy
1. **Technical recruiter** — scanning for stack match, seniority signal, recent activity
2. **Freelance client** — looking for proof of delivery and a way to contact
3. **Engineering peer** — evaluating depth, pinned repos, contribution quality

---

## README Structure (Section Layout)

```
┌─────────────────────────────────────────────────────┐
│  HEADER BLOCK                                       │
│  Name + Title + Location + Availability Badge       │
├─────────────────────────────────────────────────────┤
│  IDENTITY STATEMENT                                 │
│  2-3 line bio — architectural framing, not generic  │
├─────────────────────────────────────────────────────┤
│  CURRENT FOCUS                                      │
│  What you are actively building / learning now      │
├─────────────────────────────────────────────────────┤
│  CORE STACK (visual badge row)                      │
│  Golang · gRPC · Kubernetes · AWS · Node.js · Java  │
├─────────────────────────────────────────────────────┤
│  EXPERIENCE TIMELINE (compact)                      │
│  4 roles in a clean table — company, role, period   │
├─────────────────────────────────────────────────────┤
│  GITHUB STATS BLOCK                                 │
│  Stats card + Language card (with C hidden)         │
├─────────────────────────────────────────────────────┤
│  CONNECT / CTA BLOCK                                │
│  Portfolio link + LinkedIn + Email                  │
└─────────────────────────────────────────────────────┘
```

---

## Language Stats Architecture

### Problem
The `github-readme-stats` Top Languages card counts bytes across all 61 public repositories. Older C/Java/Python university projects inflate non-professional languages.

### Solution Architecture

```
All Public Repos (61)
        │
        ▼
┌───────────────────┐     ┌─────────────────────────┐
│  Archive Layer    │     │  Active Layer            │
│  Old student repos│     │  Professional / current  │
│  → hidden from    │     │  → counted in stats      │
│    stats          │     │                          │
└───────────────────┘     └─────────────────────────┘
        │                           │
        ▼                           ▼
        ×                    Golang dominant
                             + Node.js
                             + Java (secondary)
```

### Stats URL Parameters
```
Base:    github-readme-stats.vercel.app/api/top-langs/
Params:  ?username=deepanshu102
         &layout=compact
         &theme=tokyonight
         &hide_border=true
         &bg_color=00000000
         &hide=c,c%2B%2B
         &langs_count=6
         &count_private=false
```

The `&hide=c,c%2B%2B` removes C and C++ from display.
The `&langs_count=6` shows the top 6 remaining languages.

---

## Pinned Repository Architecture

### Target State (6 pinned repos)

| Slot | Repository | Language | Purpose |
|------|-----------|----------|---------|
| 1 | `BlockChain-go` | Go | Already pinned — keep |
| 2 | `microservices-demo` | Go | New — showcase distributed systems |
| 3 | `grpc-go-patterns` | Go | New — showcase gRPC expertise |
| 4 | `aws-lambda-dynamo` | Go | New — showcase cloud-native work |
| 5 | `deepanshu102.github.io` | HTML/CSS/JS | Portfolio source |
| 6 | `system-design-notes` | Markdown | Architecture thinking / documentation |

### Repository Content Standards
Each new repository must contain:
- A `README.md` with problem statement, architecture diagram (ASCII or Mermaid), tech stack, and setup instructions
- At least one meaningful commit showing actual implementation (not just README)
- Topics/tags set: `golang`, `microservices`, `backend`, `cloud-native`, `grpc` etc.
- A LICENSE file

---

## Visual Design Consistency

The GitHub profile must visually align with the portfolio's cyberpunk aesthetic without being able to use CSS. Achievable through:

- **Dark theme stats cards** — `theme=tokyonight` matches the portfolio palette
- **Badge colours** — use shields.io badges with hex `#00f5ff` (cyan) for primary stack items
- **Consistent naming** — same company names, role titles, and project names as the portfolio
- **No emoji overload** — maximum 1 emoji per section header, zero in body text

---

## Data Flow: Portfolio ↔ GitHub Profile

```
Portfolio (deepanshu102.github.io)
        │
        ├─ Links to: github.com/deepanshu102
        ├─ Embeds:   github-readme-stats cards
        └─ Mirrors:  Same experience data, same project names

GitHub Profile (deepanshu102/deepanshu102 README)
        │
        ├─ Links to: deepanshu102.github.io
        ├─ Shows:    Same role titles and companies
        └─ Pins:     Repos that match portfolio project cards
```

Both surfaces must tell identical stories. A recruiter who bounces between the two should feel continuity, not contradiction.

---

## Maintenance Architecture

### What changes frequently
- Current focus / learning section — update every 1–3 months
- Stats cards — auto-update via vercel service, no action needed

### What changes rarely
- Experience timeline — only when a new role starts
- Core stack badges — only when a major technology is added or dropped
- Pinned repositories — review quarterly

### Single source of truth
`app.js` in the portfolio contains the `CONTENT` object with all experience and project data. Any update to that data must also be reflected in the GitHub profile README manually. There is no automated sync — this is a deliberate manual gate to ensure both surfaces are intentionally kept consistent.
