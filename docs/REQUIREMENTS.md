# GitHub Profile — Requirements Specification
## deepanshu102 — Profile Overhaul

---

## 1. Functional Requirements

### FR-01 — Identity Communication
The profile README must communicate the following within the first viewport (no scroll):
- Full name: Deepanshu Gupta
- Current title: Senior Software Engineer / System Architect
- Current company: Kairos Technologies
- Years of experience: 5.2+
- Availability for freelance: visible as a status badge or inline text
- Location: Delhi/NCR, India

**Acceptance criteria:** A recruiter who lands on the profile can determine seniority, stack, and availability without scrolling.

---

### FR-02 — Stack Visibility
The primary technical stack must be visible as a badge row in the README.

**Required badges (in this order):**
1. Golang
2. Kubernetes
3. gRPC
4. AWS
5. Node.js
6. MongoDB
7. Docker
8. Java / Spring Boot
9. MySQL
10. GitLab CI/CD

**Acceptance criteria:** Each badge links to the relevant official site or documentation. Colour scheme must use `style=flat-square` for visual consistency.

---

### FR-03 — Experience Timeline
The README must contain a compact experience table with the following four roles in reverse chronological order:

| Company | Role | Period |
|---------|------|--------|
| Kairos Technologies | Senior Software Engineer | Nov 2024 – Present |
| Ascendion Engineering | Software Engineer | Nov 2022 – Oct 2024 |
| Coforge Ltd | Senior Software Engineer | Jul 2020 – Nov 2022 |
| NIIT Technologies | Trainee Java Developer | Jan 2020 – Jul 2020 |

**Acceptance criteria:** Table renders correctly on GitHub. Role titles match exactly what appears on the portfolio at `deepanshu102.github.io`.

---

### FR-04 — Language Statistics
The Top Languages card must show Golang as the dominant language.

**Required URL parameters:**
- `hide=c,c%2B%2B` — removes C and C++ from display
- `langs_count=6` — shows 6 languages maximum
- `theme=tokyonight` — matches portfolio visual style
- `hide_border=true` — seamless card appearance
- `bg_color=00000000` — transparent background

**Acceptance criteria:** When a visitor views the profile, C does not appear in the Top Languages card. Golang appears first or second.

---

### FR-05 — GitHub Activity Stats
The general GitHub stats card must be present and configured consistently with the Top Languages card.

**Required parameters:**
- Same theme, border, and background settings as FR-04
- `show_icons=true`
- Do NOT include `count_private=true` — this inflates stats inaccurately

**Acceptance criteria:** Both stat cards use identical visual theme and render without white borders on GitHub's dark theme.

---

### FR-06 — Navigation Links
The README must contain clickable links to all three external profiles in a dedicated connect section.

**Required links:**
1. Portfolio — `https://deepanshu102.github.io`
2. LinkedIn — `https://www.linkedin.com/in/bitsbytesofficial/`
3. Email — `mailto:deepanshuofficials@gmail.com`
4. GitHub organisation — `https://github.com/BitsBytesOfficials`

**Acceptance criteria:** All links open the correct destination. Portfolio link must be displayed prominently, not buried at the bottom.

---

### FR-07 — Current Focus Section
The README must have a current focus section that is accurate and up to date.

**Required content (as of April 2026):**
- Currently working on: Macro-service architecture and K8s orchestration at Kairos Technologies
- Primary stack statement listing Golang, gRPC, Kubernetes, AWS, Node.js
- Invite to ask about distributed systems and cloud-native architecture

**Acceptance criteria:** No reference to "learning Blockchain" or "working on Blockchain-go" as a primary focus. These are outdated and contradict senior engineer positioning.

---

### FR-08 — Pinned Repositories
The profile must have exactly 6 pinned repositories at target state.

**Required pins:**
1. `BlockChain-go` — existing, keep
2. `microservices-demo` OR `golang-microservices-patterns` — new
3. `grpc-go-starter` — new
4. `aws-serverless-go` OR `aws-lambda-dynamo` — new
5. `deepanshu102.github.io` — portfolio source, pin this
6. `system-design-notes` — new, architectural writing

**Acceptance criteria:** At minimum 4 of 6 pinned repos contain Golang as the primary language. All repos have a README. All repos have relevant topic tags.

---

## 2. Content Requirements

### CR-01 — Bio Statement
Must not be generic. Must reflect senior engineering seniority and architectural expertise.

**Prohibited phrases:**
- "passionate developer"
- "currently learning" (unless genuinely current and not contradicting senior status)
- "enthusiastic to learn new things"

**Required elements:**
- Years of experience (5.2+)
- Primary domain (backend, cloud-native, distributed systems)
- Architectural framing (not just implementation)

---

### CR-02 — Profile Metadata (GitHub Settings)
The following must be set in GitHub Settings → Profile, not just the README:

| Field | Required Value |
|-------|---------------|
| Name | Deepanshu Gupta |
| Bio | Senior Backend Engineer · Golang · K8s · AWS · Open to Freelance |
| Location | Delhi/NCR, India |
| Website | https://deepanshu102.github.io |
| Company | @KairosTechnologies (or plain text: Kairos Technologies) |

**Acceptance criteria:** The profile sidebar on desktop shows the website link and location without requiring the user to scroll into the README.

---

### CR-03 — Narrative Consistency with Portfolio
Every piece of information on the GitHub profile must match the corresponding information on the portfolio.

**Consistency checklist:**
- [ ] Role titles match exactly (e.g. "Senior Software Engineer" not "Sr. Software Engineer")
- [ ] Company names match exactly (e.g. "Ascendion Engineering" not "Ascendion")
- [ ] Date periods match exactly (e.g. "Nov 2024 – Present" not "2024 – Present")
- [ ] Project names match exactly across both surfaces
- [ ] Tech stack items use consistent casing (Golang not GoLang, MySQL not MySql)

---

### CR-04 — Repository README Standards
Every pinned repository must contain a README with these sections:

1. **Project title and one-line description**
2. **Problem statement** — what real-world problem does this solve
3. **Architecture** — ASCII diagram or Mermaid diagram showing component relationships
4. **Tech stack** — list of technologies used
5. **Setup instructions** — how to run locally (even if just `go run main.go`)
6. **Key design decisions** — why certain architectural choices were made

---

## 3. Non-Functional Requirements

### NFR-01 — Performance
Stats cards are loaded from external services (vercel). They must use `loading="lazy"` where possible and must have fallback alt text so the profile degrades gracefully if the service is unavailable.

---

### NFR-02 — Visual Consistency
All stats cards must use the same theme (`tokyonight`), same border setting (`hide_border=true`), and same background (`bg_color=00000000`). Mixing themes creates an unprofessional appearance.

---

### NFR-03 — Mobile Readability
GitHub profiles render on mobile. The README layout must be readable at 375px viewport width:
- Badge rows must wrap gracefully, not overflow
- Tables must not require horizontal scroll (keep columns to 3 maximum)
- Images must not exceed 500px width (GitHub scales them but large images can cause layout issues)

---

### NFR-04 — Maintenance Burden
The profile must be designed for low maintenance:
- Stats cards are self-updating — no action required
- Only the Current Focus section requires regular updates (every 1–3 months)
- The experience table only changes when a new role starts
- New pinned repos can be added without editing the README

---

### NFR-05 — No Fabrication
The GitHub profile must not imply skills, contributions, or experience that is not real.

Specifically:
- Do not use `count_private=true` on stats cards to artificially inflate numbers
- Do not pin repositories that you did not write
- Do not add languages to the stack badges that you have not used professionally
- Architecture diagrams in new repositories must reflect how the code actually works, not an idealised version

---

## 4. Out of Scope

The following are explicitly not part of this GitHub profile update:

- Changes to the portfolio site (`deepanshu102.github.io`) — covered by the portfolio plan
- Changes to the LinkedIn profile — separate effort
- Migrating private company repositories to public — not appropriate for proprietary code
- Creating a GitHub Pages site from this repository — the portfolio already covers this need
- Automated README generation scripts — the simplicity of static Markdown is a feature, not a limitation

---

## 5. Dependencies

| Dependency | Required For | Status |
|------------|-------------|--------|
| Portfolio content (`app.js` CONTENT object) | Narrative consistency | Available |
| Formspree account | Contact form on portfolio (not GitHub) | Pending |
| New repository code | FR-08 pinned repos | To be created |
| GitHub profile settings update | CR-02 metadata | Requires GitHub login |
| Repository archiving | FR-04 language stats | Requires GitHub login |
