# Personal Blog

Astro blog with "The Quiet Object" design — Japanese Ma (negative space) + Swiss typographic precision, with Tufte-style sidenotes and epistemic status labels.

## Stack

- Astro 5 with MDX support
- Tailwind CSS v4 (via Vite plugin)
- Google Fonts: EB Garamond (serif) + IBM Plex Mono (monospace)
- Static output (no SSR adapter)

## Design System

### Palette (warm monochrome)
- `--bg: #F7F6F3` — warm paper
- `--text: #1A1917` — warm near-black
- `--text-muted: #8A8778` — warm gray (dates, metadata)
- `--border: #E2E0DB` — subtle separator lines
- `--accent: #4A4639` — links, subtle dark warm

### Typography
- EB Garamond for all prose text (headings weight 400, body 400/500)
- IBM Plex Mono for metadata: dates, epistemic status, nav links, sidenotes, footer
- Content column: 640px max-width (optimal serif line length)
- Page container: 960px max-width

### Key Design Elements
- **Dropcap**: First letter of first paragraph in blog posts via `::first-letter`
- **Vertical dates**: `writing-mode: vertical-rl` on index page, collapses to horizontal on mobile
- **Epistemic status**: Optional frontmatter field (`seedling` | `growing` | `evergreen`), shown as monospace badge
- **Sidenotes**: Tufte-style `<Sidenote id="n">` component for MDX. Right margin on desktop, toggle on mobile
- **Fade-in**: Staggered animation on index entries, page-level on posts/about

## Content

### Blog Post Frontmatter
```yaml
title: string (required)
description: string (required)
pubDate: date (required)
updatedDate: date (optional)
heroImage: image (optional, not displayed but kept in schema)
epistemicStatus: 'seedling' | 'growing' | 'evergreen' (optional)
```

### Using Sidenotes in MDX
```mdx
import Sidenote from '../../components/Sidenote.astro';

Some text <Sidenote id="1">This appears in the right margin on desktop</Sidenote> continues here.
```

## Routes

- `/` — Blog listing (homepage)
- `/blog/[slug]` — Individual post
- `/about` — About page
- `/blog` — Redirects to `/`
- `/rss.xml` — RSS feed

## Conventions

- Homepage IS the blog listing — no separate landing page
- The aesthetic is "quiet" — avoid adding shadows, borders, bright colors, or decorative elements
- Hero images are supported in the schema but intentionally not displayed
- Keep the monochrome warmth — if adding color, it should be a single muted earth tone
