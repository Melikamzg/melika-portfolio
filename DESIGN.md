# Design Guide — UX Strategy & Standards Timeline

## Design Philosophy

Bold and visionary, but grounded in real problems and real people. The timeline is built on SAP Horizon's light theme — clean, airy, and professional — with SAP blue, indigo, and teal accents providing energy and brand recognition. Not a generic slide deck or corporate template. Something that feels editorial and purposeful, while staying fully on-brand.

The format is a **horizontal scroll canvas**: events are laid out chronologically, with most recent events on the left (shown on load). The user drags right to travel back in time — like rewinding a film reel.

## Color Palette

The timeline uses SAP Horizon's **light theme** as its foundation, with blues, indigos, and teal from the SAP Fiori color spectrum for accents and interactive elements.

### Active Tokens (currently in use)
| Role | Token / Value | Hex |
|---|---|---|
| Page background | — | `#EFF1F2` |
| Panel background (hero, closing) | `--grey-1` | `#F5F6F7` |
| Card surface (standard) | — | `#FFFFFF` |
| Card surface (conference/external) | — | `rgba(0,112,242,0.05)` |
| Card left-border accent (standard) | `--blue-7` | `#0070F2` |
| Card left-border accent (conference) | `--indigo-6` | `#7858FF` |
| Card border (standard) | `--grey-2` | `#EAECEE` |
| Card border (conference) | — | `rgba(0,112,242,0.20)` |
| Card shadow (standard) | — | `rgba(0,112,242,0.08)` |
| Card shadow (conference) | — | `rgba(120,88,255,0.08)` |
| Category pill (standard cards) | `--indigo-6` filled | `#7858FF` |
| Category pill (conference cards) | `--blue-7` filled | `#0070F2` |
| Card date label | `--blue-7` | `#0070F2` |
| Card title | `--grey-11` | `#12171C` |
| Card body text | `--grey-6` | `#5B738B` |
| Primary action / interactive | `--blue-7` | `#0070F2` |
| Accent / highlight | `--blue-6` | `#1B90FF` |
| Indigo accent | `--indigo-6` | `#7858FF` |
| Indigo highlight | `--indigo-4` | `#B894FF` |
| Teal accent (confirmed nodes) | `--teal-4` | `#2CE0BF` |
| Major node (confirmed) | `--blue-7` + halo `rgba(0,112,242,0.20)` | `#0070F2` |
| Minor node (confirmed) | `--blue-7` + halo `rgba(0,112,242,0.15)` | `#0070F2` |
| Upcoming node (pulse) | `--blue-7` + halo `rgba(0,112,242,0.20)` | `#0070F2` |
| Track line | gradient `--blue-7` → `--indigo-6`, 45% opacity | — |
| Connector line | gradient `rgba(0,112,242,0.30)` → `rgba(120,88,255,0.15)` | — |
| Hero / closing glow (indigo) | — | `rgba(120,88,255,0.12)` |
| Hero / closing glow (blue) | — | `rgba(0,112,242,0.10)` |
| Hero / closing glow (teal) | — | `rgba(44,224,191,0.07–0.08)` |
| Footer bar background | — | `rgba(245,246,247,0.92)` |
| Footer border | `--grey-2` | `#EAECEE` |
| Footer text | `--grey-6` | `#5B738B` |
| Progress bar | gradient `--blue-7` → `--indigo-6` | — |
| Text primary | `--grey-11` | `#12171C` |
| Text secondary | `--grey-6` | `#5B738B` |
| Light border | `--grey-2` | `#EAECEE` |

### Reference Tokens (available, not currently applied)
| Role | Token | Hex |
|---|---|---|
| Dark background | `--blue-11` | `#00144A` |
| Dark surface layer | `--indigo-10` | `#1C0C6E` |
| Dark card surface | `--blue-10` | `#002A86` |
| Dark border | — | `rgba(255,255,255,0.10)` |
| Dark text primary | — | `#FFFFFF` |
| Dark text secondary | — | `rgba(255,255,255,0.55)` |

### Usage Rules
- **Page background:** one step darker than `--grey-1` (`#EFF1F2`) so white cards have visible lift
- **Panels (hero, closing):** `--grey-1` (`#F5F6F7`) with indigo + blue + teal radial glows at 10–12% opacity
- **Cards:** white surface with a 3px SAP blue (standard) or indigo (conference) left-border accent
- **Category pills:** always filled — indigo on standard cards, SAP blue on conference/external cards
- **Nodes:** teal for confirmed past events, blue for minor events, indigo (pulsing) for upcoming
- **Track and connectors:** blue→indigo gradient; connectors fade from blue at the node outward
- **Atmospheric effects:** radial gradients in indigo, blue, and teal — always behind content, never in front
- **Accents:** teal (`--teal-4`) for confirmed/positive; indigo (`--indigo-6`) for secondary; blue (`--blue-7`) for primary actions
- **No mango/orange** unless specifically needed for urgency or warning signals

## Typography

**Display font:** SAP 72 (weights: 300 Light, 400 Regular, 500 Medium, 700 Bold)  
**Mono font:** JetBrains Mono — for labels, tags, technical metadata, and short data callouts  
**Fallback stack:** `'72', 'SAP72', 'Segoe UI', -apple-system, Arial, sans-serif`

| Element | Size | Weight | Font | Notes |
|---|---|---|---|---|
| Hero headline | 56–72px | 500–700 | SAP 72 | Line height 1.04, max-width ~860px |
| Hero subheading | 32–44px | 300 | SAP 72 | Line height 1.15 |
| Section title | 32–36px | 300 + **700 on key word** | SAP 72 | Mixed weight for emphasis |
| Body / lead text | 16–18px | 400 | SAP 72 | Line height 1.6, max-width ~620px |
| Card body | 14px | 400 | SAP 72 | Line height 1.6 |
| Labels / tags | 11–12px | 600–700 | JetBrains Mono | Uppercase, letter-spacing 0.12em |
| Technical metadata | 12px | 600 | JetBrains Mono | Used sparingly |

## Spacing & Shape

| Token | Value |
|---|---|
| Base unit | 8px |
| Card padding | 24px |
| Section padding | 80px |
| Gap (grid) | 16–24px |
| Card radius | 8–12px |
| Control radius | 8px |
| Pill radius | 9999px |

## Timeline Layout Patterns

The page is a single full-viewport horizontal canvas. All panels sit side-by-side on the x-axis. Past events are on the left; future events extend to the right.

### 1. Hero Panel (light, atmospheric, fixed-width)
`--grey-1` background with indigo + blue + teal radial glows (10–12% opacity). First panel — `100vw` wide, but skipped on load so the user lands directly on the latest events. Large headline, short subline, key stats. Accessible by dragging right past all events.

### 2. Timeline Track
A continuous horizontal rule (`2px`, gradient `--blue-7` → `--indigo-6`, 45% opacity) runs through the vertical midpoint of the viewport. Event nodes sit on this line. Cards hang above or below in alternating rows.

### 3. Event Card — standard (`.card-dark`)
White surface (`#FFFFFF`), `--grey-2` border, 3px `--blue-7` left-border accent, blue-tinted shadow. Category pill: indigo filled. Date label: `--blue-7`. Used for the majority of events.

### 4. Event Card — conference/external (`.card-light`)
SAP blue tint surface (`rgba(0,112,242,0.05)`), `rgba(0,112,242,0.20)` border, 3px `--indigo-6` left-border accent, indigo-tinted shadow. Category pill: `--blue-7` filled. Used for Sapphire, d-com Berlin, and other externally-facing events.

### 5. Event Node
Circle shape for all nodes — 12px for major events, 10px for minor. All nodes use `--blue-7` (`#0070F2`) with a soft blue halo. Upcoming nodes additionally pulse with the `node-pulse-circle` animation.

### 6. Connector Line
`1px` vertical line from node to card. Gradient from `rgba(0,112,242,0.30)` at the node end to `rgba(120,88,255,0.15)` at the card end.

### 7. Closing Panel (light, statement)
Same treatment as hero: `--grey-1` background with stronger radial glows (indigo + blue + teal). Single large statement, maximum whitespace.

## Imagery

- **UI mockups:** Primary visual content — show the prototype and interface concepts directly in slides
- **Atmospheric effects:** Static CSS radial glows used as background layers — always behind content
- **Icons:** Simple, consistent weight throughout. No decorative illustration.

## Timeline Behaviour

The page is a **horizontal drag-scroll canvas** — not a paginated deck.

- **Scroll axis is horizontal:** `overflow-x: scroll` on the timeline container; `overflow-y: hidden`
- **Drag-to-scroll (click-and-drag):** `mousedown` begins a drag session; `mousemove` updates `scrollLeft` by the delta; `mouseup` / `mouseleave` ends the session. Cursor changes to `grab` on hover, `grabbing` during drag.
- **Touch support:** native `touch-action: pan-x` — horizontal swipe works without JS
- **No snap:** events don't lock into place — the timeline flows freely like a scrubber. The user decides where to stop
- **Keyboard:** `ArrowLeft` / `ArrowRight` scroll by 300px with `scroll-behavior: smooth`
- **Progress indicator:** a thin `2px` progress bar pinned at the very top of the viewport (`position: fixed`) fills from left to right as the user scrolls — same gradient as the timeline track (`--blue-7` → `--indigo-6`)
- **Date label strip:** a fixed bottom bar (`position: fixed; bottom: 0`) shows the date/month label of the event node closest to the horizontal viewport center, updating as the user scrolls. JetBrains Mono, 11px, uppercase, `--text-secondary`

## Motion & Interaction

- **Scroll motion:** free horizontal drag — smooth, not snappy. Drag stops on `mouseup`; no JS inertia loop needed.
- **Card entrance:** cards animate in (`opacity: 0 → 1`, `translateY(12px) → 0`) on page load, staggered by index (`animation-delay: index × 80ms`). No scroll-triggered observer required.
- **Node pulse:** upcoming event nodes (indigo) pulse continuously (`scale 1 → 1.3 → 1`, opacity 1 → 0.4 → 1) to signal they are in the future.
- **Hover states on cards:** slight lift (`translateY(-2px)`) + shadow.
- **Ambient background:** static radial gradients in indigo and blue on the hero and closing panels — no animated drift.
- **Easing:** smooth and restrained (`cubic-bezier(0.4, 0, 0.2, 1)`) throughout.

## What to Avoid

- Generic SaaS card grids — preserve structural distinctiveness
- Swapping color mode mid-deck without clear intent
- Atmospheric effects that compete with or obscure content
- Bullet point lists as primary content — prefer cards, visuals, bold statements
- More than one accent color per slide
- Font sizes below 13px in presentation context
- Decorative gradients that don't reinforce depth or hierarchy
