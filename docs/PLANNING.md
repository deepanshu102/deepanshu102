# GitHub Profile Update — Planning Document
## deepanshu102 — Profile Overhaul Plan

---

## Objective

Transform the current GitHub profile from a generic auto-generated README with outdated information into a professional engineering profile that mirrors the narrative of the portfolio at `deepanshu102.github.io` and positions you correctly for senior engineering roles and freelance client engagement.

---

## Current State Assessment

| Element | Current State | Problem |
|---------|--------------|---------|
| Bio | "A passionate developer from India" | Generic, entry-level framing |
| Current work | "Working on Blockchain-go" | Outdated — you are at Kairos Technologies |
| Learning | "Currently learning Blockchain" | Contradicts senior engineer narrative |
| Top language | C | Inflated by old student repos |
| Pinned repos | Only 1 (BlockChain-go) | Insufficient social proof |
| Profile README | No experience timeline | Recruiter has no career context |
| Contact links | YouTube channel only | No direct hire/contact path |
| Stack badges | Missing | No visual stack signal |
| Portfolio link | Not present | Biggest missed opportunity |

---

## Target State

A profile that a technical recruiter or freelance client reads and immediately understands:
- You are a Senior Software Engineer with 5.2+ years
- Your primary stack is Golang, Kubernetes, AWS, gRPC
- You are currently available for freelance work
- Your portfolio is one click away
- Your recent GitHub activity shows active Golang work

---

## Phase 1 — Immediate Fixes (Day 1, ~30 minutes)

These require no new code. Just edits to the existing README.

### Task 1.1 — Update profile bio in README
Replace the current generic bio with the identity statement from the portfolio.

**New content:**
```markdown
### Deepanshu Gupta — System Architect & Backend Engineer

> Architect of resilience. 5.2+ years building high-performance cloud-native 
> backend systems. Currently leading macro-service architecture and K8s 
> orchestration at Kairos Technologies, Pune.

📍 Delhi/NCR, India &nbsp;|&nbsp; 🟢 **Available for Freelance**
```

### Task 1.2 — Update current focus section
```markdown
- 🔭 Currently working on: Macro-service architecture & K8s orchestration at **Kairos Technologies**
- 🛠 Primary stack: **Golang · gRPC · Kubernetes · AWS · Node.js**
- 💬 Ask me about: Distributed systems, cloud-native architecture, backend performance optimisation
- 📫 Contact: deepanshuofficials@gmail.com
- 🌐 Portfolio: [deepanshu102.github.io](https://deepanshu102.github.io)
```

### Task 1.3 — Fix Top Languages stats URL
Add `&hide=c,c%2B%2B` and `&langs_count=6` to the existing image URL in README.

**Before:**
```
https://github-readme-stats.vercel.app/api/top-langs/?username=deepanshu102&show_icons=true&locale=en&layout=compact
```

**After:**
```
https://github-readme-stats.vercel.app/api/top-langs/?username=deepanshu102&layout=compact&theme=tokyonight&hide_border=true&bg_color=00000000&hide=c,c%2B%2B&langs_count=6
```

### Task 1.4 — Add portfolio link to GitHub profile bio
In GitHub Settings → Profile (not the README), update:
- **Website field:** `https://deepanshu102.github.io`
- **Bio field:** `Senior Backend Engineer · Golang · Kubernetes · AWS · Open to Freelance`
- **Location:** `Delhi/NCR, India`

---

## Phase 2 — README Rebuild (Day 1–2, ~2 hours)

Full replacement of the README with structured professional content.

### Task 2.1 — Add stack badge row
Using shields.io badges styled to match the portfolio palette.

```markdown
![Golang](https://img.shields.io/badge/Golang-00ADD8?style=flat-square&logo=go&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-FF9900?style=flat-square&logo=amazonaws&logoColor=white)
![gRPC](https://img.shields.io/badge/gRPC-244c5a?style=flat-square&logo=google&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
```

### Task 2.2 — Add experience timeline table
```markdown
## Experience

| Period | Company | Role |
|--------|---------|------|
| Nov 2024 – Present | Kairos Technologies | Senior Software Engineer |
| Nov 2022 – Oct 2024 | Ascendion Engineering | Software Engineer |
| Jul 2020 – Nov 2022 | Coforge Ltd | Senior Software Engineer |
| Jan 2020 – Jul 2020 | NIIT Technologies | Trainee Java Developer |
```

### Task 2.3 — Update stats cards theme
Replace all existing stats card URLs with the `tokyonight` theme versions that match the portfolio visual language.

### Task 2.4 — Add contact / CTA section
```markdown
## Connect

[![Portfolio](https://img.shields.io/badge/Portfolio-deepanshu102.github.io-00f5ff?style=flat-square)](https://deepanshu102.github.io)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-bitsbytesofficial-0077B5?style=flat-square&logo=linkedin)](https://www.linkedin.com/in/bitsbytesofficial/)
[![Email](https://img.shields.io/badge/Email-deepanshuofficials@gmail.com-D14836?style=flat-square&logo=gmail)](mailto:deepanshuofficials@gmail.com)
```

---

## Phase 3 — Repository Cleanup (Week 1, ~1 hour)

### Task 3.1 — Archive student/legacy repositories
Archive these categories of repos (they inflate old languages and dilute your professional signal):
- Any repo from BCA / MCA coursework
- Tutorial-following repos with no original contribution
- Incomplete or abandoned projects with zero commits after 2020

Archiving keeps them visible on your profile history but removes them from language stats. To archive: Repository → Settings → Danger Zone → Archive.

### Task 3.2 — Add topics to existing repos
Every public repository should have topic tags. Add these to existing repos:
- `BlockChain-go`: `golang`, `blockchain`, `distributed-systems`
- `deepanshu102.github.io`: `portfolio`, `javascript`, `threejs`, `gsap`

Topics make repositories discoverable and signal professional intent.

---

## Phase 4 — New Pinned Repositories (Week 2–4, ~4–8 hours total)

### Repo 1: `golang-microservices-patterns`
**Purpose:** Demonstrates your core professional expertise  
**Content:** 3–4 common microservice patterns in Go: service discovery, circuit breaker, API gateway, gRPC service-to-service  
**Time estimate:** 3–4 hours  
**Why this matters:** This is the repo a technical recruiter checks after seeing your profile says "Golang microservices"

### Repo 2: `grpc-go-starter`
**Purpose:** Demonstrates gRPC expertise that appears in your Kairos experience  
**Content:** A working gRPC server + client in Go with protobuf definitions, unit tests using mock isolation (testify), and a README explaining the architecture  
**Time estimate:** 2 hours  
**Why this matters:** gRPC with testify mock isolation is specifically mentioned in your Kairos bullet points

### Repo 3: `aws-serverless-go`
**Purpose:** Demonstrates AWS Lambda + DynamoDB that appears in Coforge experience  
**Content:** A simple event-driven Lambda function in Go that reads/writes to DynamoDB with a clear architecture diagram in the README  
**Time estimate:** 2 hours  
**Why this matters:** Closes the gap between your portfolio claiming AWS expertise and your GitHub showing no AWS code

### Repo 4: `system-design-notes`
**Purpose:** Demonstrates architectural thinking, not just coding  
**Content:** Markdown documents explaining architectural decisions — when to use microservices vs macro-services, caching strategies, database selection, etc. Based on real decisions from your career  
**Time estimate:** 1–2 hours (writing, not coding)  
**Why this matters:** Differentiates you from engineers who only code and positions you as an architect

---

## Timeline

| Week | Tasks | Outcome |
|------|-------|---------|
| Day 1 | Phase 1 (all tasks) | Profile bio fixed, C removed from stats, portfolio link visible |
| Day 2 | Phase 2 (README rebuild) | Professional README live with stack badges and experience table |
| Week 1 | Phase 3 (cleanup) | Old repos archived, topic tags added |
| Week 2 | Repo 1: golang-microservices-patterns | First new pinned repo live |
| Week 3 | Repo 2: grpc-go-starter | gRPC expertise visible |
| Week 4 | Repo 3 + 4 | Full 6-pin profile complete |

---

## Success Metrics

After completing all four phases, the profile should show:

- [ ] Top Languages card shows Golang as #1
- [ ] Bio correctly states current role at Kairos Technologies
- [ ] Portfolio link is in the GitHub profile bio field and the README
- [ ] 6 pinned repositories visible, at least 4 in Golang
- [ ] Experience table is present and accurate
- [ ] Contact section with LinkedIn, email, and portfolio links
- [ ] No mention of "learning Blockchain" anywhere on the profile
- [ ] All stats cards use the `tokyonight` dark theme
