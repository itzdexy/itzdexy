# Dexy GitHub Profile README Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Build the approved black-and-white anime/dev GitHub profile for `@itzdexy` using the user's exact banner, factual copy, monochrome stack icons, typing animation, and live GitHub activity.

**Architecture:** The profile is a single GitHub profile `README.md` backed by one local image asset. Visual personality comes from the banner and restrained terminal-style Markdown; dynamic elements are limited to external SVG services for typing, stack icons, streaks, and activity.

**Tech Stack:** GitHub Markdown/HTML, PNG asset, readme-typing-svg, Simple Icons CDN, GitHub Streak Stats, GitHub Readme Activity Graph

**Spec:** `docs/superpowers/specs/2026-08-20-profile-readme-design.md`

## Global Constraints

- Pure black / white presentation; muted gray only where GitHub rendering requires it.
- Use the provided uploaded banner unchanged as `assets/dexy-banner.png`.
- Show exactly C++, Python, Tauri, Rust, and HTML.
- Do not list private repositories or invent project descriptions.
- Do not claim years of experience, employment, expertise, user counts, performance numbers, awards, or open-source impact.
- No gradients, neon accents, rainbow badges, trophy walls, profile-view counters, Spotify widgets, or generic motivational quotes.
- All live activity widgets must use the real username `itzdexy`.

---

### Task 1: Add the exact banner asset

**Files:**
- Create: `assets/dexy-banner.png`

**Interfaces:**
- Consumes: user-provided 2048×682 PNG banner
- Produces: relative README asset path `./assets/dexy-banner.png`

- [ ] **Step 1: Preserve the original pixels**

Use lossless PNG optimization only; do not crop, recolor, resize, redraw, or otherwise alter the visual content.

- [ ] **Step 2: Add the image to the repository**

Store the file exactly at:

```text
assets/dexy-banner.png
```

- [ ] **Step 3: Verify the asset**

Fetch the repository file and confirm it is present on `main` and is a PNG asset.

- [ ] **Step 4: Commit**

```bash
git add -- assets/dexy-banner.png
git commit -m "assets: add Dexy profile banner"
```

### Task 2: Build the profile README

**Files:**
- Create: `README.md`

**Interfaces:**
- Consumes: `./assets/dexy-banner.png`
- Produces: the rendered GitHub profile homepage for `@itzdexy`

- [ ] **Step 1: Create the exact profile Markdown**

```md
<p align="center">
  <img src="./assets/dexy-banner.png" width="100%" alt="Dexy banner" />
</p>

<br />

<h1 align="center">DEXY</h1>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&size=18&duration=2600&pause=900&color=FFFFFF&center=true&vCenter=true&width=720&lines=C%2B%2B+%E2%80%A2+Python+%E2%80%A2+Rust+%E2%80%A2+Tauri+%E2%80%A2+HTML;building+software%2C+tools%2C+and+experiments;most+of+my+work+is+private+right+now" alt="Typing introduction" />
</p>

<p align="center"><code>software · tools · experiments</code></p>

---

### `$ whoami`

```text
Dexy
Building software, tools, and experiments.
Most of what I’m building is private right now.
```

---

### `$ stack`

<p>
  <img src="https://cdn.simpleicons.org/cplusplus/FFFFFF" width="34" height="34" alt="C++" />
  &nbsp;&nbsp;&nbsp;&nbsp;
  <img src="https://cdn.simpleicons.org/python/FFFFFF" width="34" height="34" alt="Python" />
  &nbsp;&nbsp;&nbsp;&nbsp;
  <img src="https://cdn.simpleicons.org/tauri/FFFFFF" width="34" height="34" alt="Tauri" />
  &nbsp;&nbsp;&nbsp;&nbsp;
  <img src="https://cdn.simpleicons.org/rust/FFFFFF" width="34" height="34" alt="Rust" />
  &nbsp;&nbsp;&nbsp;&nbsp;
  <img src="https://cdn.simpleicons.org/html5/FFFFFF" width="34" height="34" alt="HTML" />
</p>

`C++` · `Python` · `Tauri` · `Rust` · `HTML`

---

### `$ work`

Most of what I’m building is private right now.

---

### `$ activity`

<p align="center">
  <img src="https://streak-stats.demolab.com?user=itzdexy&theme=transparent&hide_border=true&ring=FFFFFF&fire=FFFFFF&currStreakLabel=FFFFFF&sideLabels=FFFFFF&currStreakNum=FFFFFF&sideNums=FFFFFF&dates=8B949E&stroke=30363D" alt="GitHub streak" />
</p>

<p align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=itzdexy&bg_color=00000000&color=FFFFFF&line=FFFFFF&point=FFFFFF&area=false&hide_border=true" alt="GitHub contribution activity" />
</p>

---

<p align="center"><sub>@itzdexy</sub></p>
```

- [ ] **Step 2: Verify factual content**

Confirm the README contains no private repository names, no project cards, no invented credentials, and only the approved stack.

- [ ] **Step 3: Verify local links and dynamic usernames**

Confirm:

```text
./assets/dexy-banner.png
```

exists, and every live activity URL contains:

```text
itzdexy
```

- [ ] **Step 4: Commit**

```bash
git add -- README.md
git commit -m "feat: build Dexy GitHub profile"
```

### Task 3: Final profile verification and cleanup

**Files:**
- Verify: `README.md`
- Verify: `assets/dexy-banner.png`
- Remove after execution: `docs/superpowers/specs/2026-08-20-profile-readme-design.md`
- Remove after execution: `docs/superpowers/plans/2026-08-20-profile-readme.md`

**Interfaces:**
- Consumes: completed profile files
- Produces: a clean public profile repository containing only user-facing profile content

- [ ] **Step 1: Fetch the final README**

Check that all approved sections exist in this order:

```text
banner
DEXY
animated typing
$ whoami
$ stack
$ work
$ activity
@itzdexy
```

- [ ] **Step 2: Scan for banned/template content**

The final README must not contain any of these strings or concepts:

```text
passionate developer
full-stack ninja
profile views
trophy
Spotify
years of experience
featured projects
```

- [ ] **Step 3: Remove workflow-only design documents**

Delete the design and plan files so the public profile repository remains intentionally minimal.

- [ ] **Step 4: Verify the final repository**

Confirm `README.md` and `assets/dexy-banner.png` remain accessible on `main` after cleanup.
