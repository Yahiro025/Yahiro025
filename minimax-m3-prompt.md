# MiniMax M3 Execution Spec — GitHub Profile README Redesign

## Mission

Redesign the repository's existing `README.md` into a polished, compact, cyber-terminal-style GitHub profile README for **Bennett Payoyo / `Yahiro025`**.

The result should feel **badass but disciplined**: neon-violet command-center visuals, restrained motion, strong hierarchy, compact project cards, and excellent mobile readability. Edit the actual `README.md`; do not merely describe a redesign or return a mockup.

Read the current `README.md` before editing. Treat its facts, links, projects, and existing local assets as the source of truth.

---

## Priority Zero — Protect the Existing Quote Header

The quote artwork and caption at the top are already complete and correct. **Do not regenerate, restyle, move, rename, resize, recolor, replace, or delete them.** Do not try to load Bleeding Cowboys as live text.

The beginning of `README.md` must retain this exact block byte-for-byte:

```html
<div align="center">

<img src="./assets/quote-header.png" width="85%" alt="Sua quisque fortuna faber est. — Each is the architect of his own fortune."/>

<p align="center"><sub><i>Sua quisque fortuna faber est. — Each is the architect of his own fortune.</i></sub></p>
```

Also leave these files untouched:

- `assets/quote-header.png`
- `assets/fonts/BleedingCowboys.ttf`

The image already contains the genuine **Bleeding Cowboys** glyphs. The caption must remain exactly:

`Sua quisque fortuna faber est. — Each is the architect of his own fortune.`

All redesign work begins **after** that protected caption.

---

## Lessons From the Previous Failed Attempt

GitHub README rendering is not a normal website. Follow these restrictions strictly:

1. **No custom live fonts.** GitHub does not reliably honor `@font-face`, imported fonts, local `.ttf` references, or CSS font declarations in README content.
2. **No CSS or JavaScript.** Do not add `<style>`, `<script>`, event handlers, canvas, WebGL, or animation libraries.
3. **No iframe, video, or embedded web app.** GitHub sanitizes or blocks them.
4. **No base64 font trick or font-dependent inline SVG.** Do not repeat the old self-contained SVG fallback. The quote PNG is the correct workaround and is already finished.
5. **No fake glassmorphism or hover effects.** They require CSS and will not work. Create hierarchy with native Markdown, supported HTML, spacing, tables, `<details>`, badges, and rendered images.
6. **Animations must be image-based.** Use only a reputable remote GIF or an SVG service rendered through `<img>`/Markdown image syntax.
7. **Do not invent unsupported HTML attributes.** Safe attributes include `align`, `width`, `height`, `src`, `href`, `alt`, and standard `<details open>` behavior.
8. **Do not rely on absolute local paths.** Repository assets must use relative paths such as `./assets/quote-header.png`.
9. **Never reference an asset that does not exist.** Do not add a contribution snake URL unless its generation workflow and output branch are also implemented and verified. A broken animation is worse than no animation.
10. **Do not install packages or download another font.** This redesign needs only Markdown/HTML and the image services already used by the README.

---

## Visual Direction

### Theme: `VIOLET OPS // PH SYSTEMS BUILDER`

Use a coherent dark cyber palette **only where color can actually be controlled**—remote cards, badges, graphs, and rendered SVGs:

| Role | Hex |
| --- | --- |
| Deep background | `0B0B1A` |
| Raised panel | `121225` |
| Deep violet | `1B0B3A` |
| Primary violet | `8B5CF6` |
| Light violet | `A78BFA` |
| Electric cyan accent | `22D3EE` |
| Primary text on cards | `E9D5FF` |
| Muted text on cards | `A1A1AA` |

Do not try to set the GitHub page background or body text color; README CSS cannot do that. Keep enough contrast for both GitHub light and dark modes.

### Typography System

Use only these reliable layers:

- **Protected quote:** existing Bleeding Cowboys PNG; unchanged.
- **Animated hero line:** `JetBrains Mono` through `readme-typing-svg` (the font is rendered by that image service, not by GitHub).
- **Section labels:** GitHub-native monospace via `<code>` inside headings, for example `<h2 align="center"><code>01 // IDENTITY</code></h2>`.
- **Body copy:** GitHub's native sans-serif for readability.
- **Status/config content:** fenced `yaml` code block, which naturally uses GitHub's monospace font.
- **Micro-labels:** Shields.io badges using one consistent style.

Do not use decorative Unicode alphabets, gothic Unicode substitutions, or excessive ALL CAPS in body paragraphs. They damage accessibility and searchability.

### Motion Budget

Use motion deliberately, not everywhere. The final README should contain only these animation layers:

1. One compact `readme-typing-svg` hero line.
2. One slim animated divider GIF between the hero and profile content (reuse the current known-working GIF).
3. The existing `capsule-render` footer with `animation=fadeIn`.

The contribution graph and stats may be dynamic images, but do not add more decorative GIFs. Do not add a contribution snake in this pass because it requires a separate Actions workflow/output branch and would otherwise render as a broken image.

---

## Required Information Architecture

Rebuild the content below the protected caption in this order. Preserve all truthful information from the current README, but remove unnecessary duplication.

### 1. Compact Hero Console

Immediately after the protected caption, add one compact typing SVG—**not** the current oversized multiline `900 × 160` block.

Use `https://readme-typing-svg.demolab.com` with these design properties:

- Font: `JetBrains Mono`
- Weight: `600`
- Size: approximately `20–23`
- Height: approximately `55–65`
- Width: responsive-looking, no more than `800`
- Color: `A78BFA` or `22D3EE`
- Centered vertically and horizontally
- Duration: around `2600–3000`
- Pause: around `800–1000`
- Repeating, one line at a time
- URL-encode punctuation and spaces correctly

Use concise lines based only on current facts, such as:

- `Building AI systems for real Philippine problems.`
- `RAG • Full-stack • Social impact`
- `Learn. Build. Ship. Repeat.`

Then show a compact status row with consistent Shields.io badges:

- `BS Computer Science • PUP Manila`
- `Manila, Philippines`
- `Open to OSS + Hackathons`

Under it, show the existing contact destinations as a uniform button row:

- LinkedIn: `https://www.linkedin.com/in/bennett-payoyo-a942a0379`
- Email: `mailto:bennettpayoyo025@gmail.com`
- GitHub: `https://github.com/Yahiro025`
- Portfolio: keep `Coming Soon`, but display it as a non-clickable badge; remove the dead `href="#"` link.

Use `style=for-the-badge` consistently. Brand logos are welcome, but keep badge backgrounds within the violet/cyan/dark palette where practical.

Reuse this existing divider after the contact row:

```html
<img src="https://user-images.githubusercontent.com/74038190/212284100-561aa47a-cf87-4a7a-b6c0-7d86678c2d6a.gif" width="60%" alt="Animated neon divider"/>
```

Do not add a second divider GIF elsewhere.

### 2. `<code>01 // IDENTITY</code>`

Write a short, high-signal introduction using the current facts:

- Bennett Payoyo
- Sophomore, B.S. Computer Science
- Polytechnic University of the Philippines, Manila
- Builds applied AI/RAG apps, social-good prototypes, and small-business tooling for Philippine contexts
- Learns by shipping

Keep this to one concise paragraph. Follow it with one GitHub-native callout:

```markdown
> [!IMPORTANT]
> **Open to:** open-source collaboration and hackathon teams.
```

Do not invent employment, clients, years of experience, or claims not present in the current README.

### 3. `<code>02 // TECH ARSENAL</code>`

Make the stack considerably more compact than the current five vertically separated subsections.

Use centered `skillicons.dev` rows with short labels, or one clean table with these factual groups:

- **Languages:** C, C++, TypeScript
- **Frontend:** React, Next.js, Tailwind CSS
- **Backend & Data:** Node.js, PostgreSQL, Supabase
- **AI:** LangChain
- **Tooling:** Git, Vercel

Requirements:

- Keep the current `theme=dark` skill icons.
- Keep LangChain as a Shields.io badge if Skill Icons does not support it.
- Remove `<a href="#">` wrappers; icons do not need dead links.
- Do not add technologies that are not in the existing README.
- Prefer two dense rows over five large subsections.

### 4. `<code>03 // AI SYSTEMS</code>`

Retain the two existing expertise domains and their details:

- LLM/RAG application engineering
- AI for social-good prototyping

Use a clean three-column Markdown table: `Domain`, `Signal`, `What I build`.

Replace the visually noisy ten-character proficiency bars with concise, non-inflated labels such as `Core focus` and `Active focus`, or keep shorter five-block indicators. Do not claim expert/senior-level status. Preserve the factual LangChain.js, RAG, vector-store, streaming chat, vision, OCR, classification, and Philippine-context details.

### 5. `<code>04 // FEATURED BUILDS</code>`

Keep all four projects and every existing factual link:

1. **BANTAYOG** — blockchain-backed subsidy system addressing childhood stunting
2. **TANGLAW** — scholarship-matching RAG tool for Filipino students
3. **Bicol Dictionary** — regional-language preservation app
4. **Clarity Books** — quarterly bookkeeping assistant for Philippine small businesses

Present them as GitHub-safe interactive cards using `<details>`:

- Make BANTAYOG `<details open>` because it is the award-winning lead project.
- Keep the other three collapsed by default.
- Use a strong `<summary>` containing the project name and a one-line mission.
- Inside each card, include no more than: one outcome-focused paragraph, a compact metadata table, and button badges for available `LIVE`, `SOURCE`, or `DEMO` links.
- For private repositories, show a non-clickable `PRIVATE / SCHOOL` or `PRIVATE` badge instead of inventing a URL.
- Preserve BANTAYOG's role, stack, team size, award, date, demo URL, and repository URL.
- Preserve TANGLAW's stack, live URL, private/school context, and class-project context.
- Preserve Bicol Dictionary's Supabase detail, live URL, and private/personal status.
- Preserve Clarity Books' stack, receipt extraction/classification purpose, VAT/tax-estimate context, and live URL.

Do not invent screenshots, repository stars, user counts, performance metrics, awards, or demos.

### 6. `<code>05 // SIGNAL LOG</code>`

Keep the SparkFest recognition once in a compact achievement callout or one-row table:

- `1st Runner-Up — GDG SparkFest Hackathon`
- BANTAYOG
- Four-person team
- July 9

Do not repeat the same award description in multiple standalone sections beyond its necessary mention in the BANTAYOG card.

Then merge the redundant current-status content into one terminal-like block titled `<code>NOW.yml</code>`:

```yaml
status: sophomore @ PUP Manila
learning:
  - shipping real things
  - applied AI for Philippine contexts
building:
  - Clarity Books
  - TANGLAW
  - BANTAYOG
  - Bicol Dictionary
exploring:
  - AI policy and ethics
  - mobile-first UX
  - Philippine tech community and OSS
```

Keep this readable and truthful. Do not add fake command output or fake system metrics.

### 7. `<code>06 // GITHUB TELEMETRY</code>`

Create a compact analytics area instead of several disconnected sections.

First row, centered:

- GitHub stats card for username `Yahiro025`
- Existing streak stats card for username `Yahiro025`

Use matching colors:

- Background `0B0B1A`
- Border hidden
- Titles/rings `A78BFA` or `8B5CF6`
- Icons/fire/accents `22D3EE`
- Text `E9D5FF`

Use percentage widths around `48–49%` so the pair is compact on desktop and scales with the container. Give every image useful alt text. Do not use `count_private=true` or claim private contribution totals from a public endpoint.

Below the cards, retain one full-width contribution activity graph from `github-readme-activity-graph.vercel.app`, recolored to the same violet/cyan palette. Keep `hide_border=true`, `area=true`, and username `Yahiro025`.

Do not add trophy walls, profile-view counters, top-language cards, WakaTime cards, or fabricated metrics. The goal is signal, not dashboard clutter.

### 8. Footer

Retain a `capsule-render` waving footer with `animation=fadeIn` and the message `Thanks for visiting!`, but make it slimmer (approximately `110–130` px high) and match the palette gradient:

`0B0B1A → 1B0B3A → 5B21B6 → 8B5CF6`

Keep meaningful alt text and `width="100%"`.

---

## UX and Layout Rules

1. **Hierarchy:** One visual hero, numbered monospace section labels, then compact content blocks.
2. **Density:** Avoid excessive `<br/>` elements. Use blank lines and a single `---` between major sections where needed.
3. **No separator spam:** Never place two `---` rules together. Do not put a horizontal rule immediately beside the animated divider.
4. **Balanced HTML:** Every opened `<div>`, `<p>`, `<a>`, `<details>`, and table element must close correctly. The current README has an extra/nested `<div align="center">` around the analytics/activity area; repair it.
5. **Markdown parsing:** Close centered `<div>` containers before starting Markdown tables, alerts, lists, fenced code blocks, or `<details>` content when nesting could stop GitHub from parsing them.
6. **Responsive images:** Prefer percentage widths for large cards/graphs and avoid fixed widths wider than the README viewport.
7. **Accessibility:** Every image requires descriptive `alt` text. Link labels must describe their destination. Do not communicate status by color alone.
8. **Performance:** Keep external image services to the small set already used plus one GitHub stats card. Avoid duplicated requests and giant decorative assets.
9. **Reliability:** Keep known-working service hosts and HTTPS. Properly URL-encode query text. Do not invent service parameters without checking their supported syntax.
10. **Consistency:** Use one badge style, one palette, one heading pattern, and one terminal metaphor.
11. **Content integrity:** Preserve all working live/demo/source/contact links exactly unless only converting them into linked badges.
12. **No dead controls:** Remove all `href="#"` links. A non-link badge is the correct UI for `Coming Soon` or `Private`.

---

## Files and Scope

You may modify:

- `README.md`

Do not modify:

- `assets/quote-header.png`
- `assets/fonts/BleedingCowboys.ttf`
- Any source-code or configuration file

Do not create a GitHub Actions workflow, new generated artwork, or new font asset for this pass.

---

## Execution Procedure for MiniMax M3

1. Read all of the current `README.md` before editing.
2. Copy the protected opening block and verify it remains byte-for-byte identical.
3. Inventory every factual claim and URL in the existing README.
4. Rewrite the content below the protected caption in one coherent pass using the required information architecture.
5. Remove duplicated sections, dead `#` links, redundant separators, excessive line breaks, and malformed/nested alignment containers.
6. Check every remote image URL for valid URL encoding and every local path for repository-relative syntax.
7. Count/inspect opening and closing HTML tags manually; ensure no section is accidentally wrapped in an unclosed center-aligned `<div>`.
8. Review the final file in raw Markdown and, if a renderer is available, preview it using GitHub-flavored Markdown.
9. Do not stop at a plan. Save the completed redesign to `README.md`.
10. In your final response, briefly state what changed, what was preserved, and any rendering check you could not perform. Do not claim GitHub rendering was verified unless it actually was.

---

## Acceptance Checklist

The task is complete only if all of these are true:

- [ ] The protected quote image line is unchanged.
- [ ] The protected quote caption is unchanged, including spelling, punctuation, italics, and em dash.
- [ ] `assets/quote-header.png` and `assets/fonts/BleedingCowboys.ttf` are untouched.
- [ ] The quote remains the first visual element in the README.
- [ ] The old oversized multiline typing block is replaced by one compact JetBrains Mono typing SVG.
- [ ] The design uses a coherent violet/cyan/dark palette on rendered images and badges.
- [ ] Motion is limited to the typing SVG, one divider GIF, and the animated footer.
- [ ] All four projects remain present with accurate details and links.
- [ ] BANTAYOG is the open lead project card; the other cards are collapsed.
- [ ] Tech stack content remains accurate and is more compact.
- [ ] Current/learning/building/exploring information is consolidated without factual loss.
- [ ] Analytics use `Yahiro025`, have useful alt text, and do not claim private metrics.
- [ ] All `href="#"` dead links are gone.
- [ ] There are no custom CSS, JavaScript, iframe, video, external-font, base64-font, or fake-hover implementations.
- [ ] There are no broken references to ungenerated contribution-snake assets.
- [ ] HTML tags are balanced and Markdown components are not trapped inside malformed HTML.
- [ ] No redundant `---` separators or excessive `<br/>` spacing remain.
- [ ] The README remains readable on both desktop and narrow mobile screens.
- [ ] No facts, technologies, links, metrics, or achievements were invented.

If a visual idea conflicts with GitHub compatibility, **choose compatibility and reliability**. The intended result is a real GitHub profile README, not a web-page concept that only works in a browser sandbox.
