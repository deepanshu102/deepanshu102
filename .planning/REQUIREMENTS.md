# Requirements: GitHub Profile Overhaul

## 1. Functional Requirements (FR)

### FR-01: First-Viewport Identity
The README must communicate the following without scrolling:
- Name: **Deepanshu Gupta**
- Title: **Senior Software Engineer / System Architect**
- Seniority: **5.2+ Years**
- Core Signal: **Available for Freelance** (Cyan/Green badge)

### FR-02: Stack Visibility (HUD Style)
A horizontal badge row with the following order/links:
1. **Golang** (Primary)
2. **Kubernetes**
3. **gRPC**
4. **AWS**
5. **Node.js**
6. **MongoDB**
7. **Docker**
8. **Java / Spring Boot**

### FR-03: Experience Timeline
A compact Markdown table matching the portfolio exactly:
- Kairos Technologies (SSE) -> Present
- Ascendion Engineering (SE) -> 2024
- Coforge Ltd (SSE) -> 2022
- NIIT Technologies (Trainee) -> 2020

### FR-04: Language Stats Filtering
Top Languages card must:
- Hide `C` and `C++`.
- Show `Golang` as dominant.
- Show max `6` languages.

### FR-05: Visual Theme Consistency
Stats cards must use:
- Theme: `tokyonight`
- Background: Transparent (`bg_color=00000000`)
- Border: Hidden

---

## 2. Non-Functional Requirements (NFR)

### NFR-01: Visual Aesthetic
Approximate the "Cyberpunk Technical HUD" look using:
- Monospaced typography styling (Backticks/Code blocks).
- Hex Codes: Cyan (`#00f5ff`) and Green (`#39FF14`).
- Minimal emoji (max 1 per section).

### NFR-02: Narrative Truth
- `count_private=false` to avoid inflated contribution stats.
- No "Currently learning" tags that contradict Senior status.

---

## 3. Out of Scope
- Automated sync between portfolio and GitHub.
- Modification of existing code inside legacy repositories.
