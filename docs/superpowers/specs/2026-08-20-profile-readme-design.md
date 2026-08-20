# Dexy GitHub Profile README Design

## Goal
Create a restrained black-and-white GitHub profile README for `@itzdexy` that feels intentionally designed rather than template-generated. The uploaded Dexy anime banner is the main visual. The rest of the profile uses clean typography, terminal-inspired labels, factual copy, and real GitHub activity only.

## Visual Direction
- Pure black / white presentation; muted gray only where GitHub rendering requires it.
- No gradients, neon accents, rainbow badges, trophy walls, profile-view counters, Spotify widgets, generic motivational quotes, or fake metrics.
- Anime influence comes primarily from the provided banner, not from decorative clutter.
- Developer influence comes from monospace typing animation, terminal-style section labels, compact stack presentation, and live activity widgets.
- Desktop and mobile layouts must remain readable without horizontal overflow.

## Hero
- Use the provided uploaded banner unchanged as `assets/dexy-banner.png`.
- Display it at full README width.
- Follow with a centered `DEXY` heading.
- Add a white monospace typing animation with only factual lines:
  - `C++ • Python • Rust • Tauri • HTML`
  - `building software, tools, and experiments`
  - `most of my work is private right now`

## Identity / Copy
Use short, factual copy only.

`$ whoami`

Dexy.

`Building software, tools, and experiments.`

`Most of what I’m building is private right now.`

Do not claim years of experience, employment, expertise, open-source impact, user counts, performance numbers, awards, or any other unverifiable credential.

## Stack
Show exactly these technologies:
- C++
- Python
- Tauri
- Rust
- HTML

Use monochrome white technology icons on transparent backgrounds with text labels. Avoid a badge wall.

## Work
Use a minimal `$ work` section with this copy only:

`Most of what I’m building is private right now.`

Do not list private repository names or create fake project cards.

## Activity
Include only real, username-derived widgets:
- monochrome GitHub streak card for `itzdexy`
- monochrome GitHub activity graph for `itzdexy`

Do not include top-language cards because nearly all repositories are private and the result could be misleading.

## Footer
Keep the footer small and plain:

`@itzdexy`

No slogans or fake quotes.

## External Dependencies
Keep third-party SVG dependencies limited to:
- readme-typing-svg for the typing effect
- Simple Icons CDN for monochrome stack icons
- GitHub streak stats for live streak data
- GitHub activity graph for live contribution activity

If a dependency fails to render, the README text must still communicate the profile cleanly.

## Files
- `README.md` — profile layout and copy
- `assets/dexy-banner.png` — user-provided banner

## Verification
- Confirm the profile repository is public and named exactly `itzdexy/itzdexy`.
- Confirm the banner exists and renders from a relative path.
- Confirm the README contains no private repository names, fake claims, rainbow badges, or broken local links.
- Confirm all external widget URLs use `itzdexy` and black/white parameters.
