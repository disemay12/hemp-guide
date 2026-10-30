# HemP Guide — design notes

## Direction

A field manual for a game-automation tool: dark control-room canvas, warm amber for active controls, precise mono labels, and schematic UI illustrations instead of screenshots. The page should feel like a technical binder a player can keep open on a second monitor, not a marketing landing page.

## Tokens

| Role | Value |
|---|---|
| Page background | `#0a0d11` |
| Surface | `#121820` |
| Surface 2 | `#171f28` |
| Surface 3 | `#1d2732` |
| Border | `#2a3642` |
| Border soft | `#1c252f` |
| Text | `#edf2f7` |
| Text secondary | `#c5d0dc` |
| Muted | `#9aa9b8` |
| Dim | `#7d8d9e` |
| Accent | `#f4b45f` |
| Success | `#72dfa6` |
| Warning / danger | `#ff8585` |
| Info | `#8bb8ff` |

Type: Segoe UI Variable / system UI for reading, Cascadia Code / system mono for labels, keys, coordinates and schematics. Scale: 9, 10, 11, 12.5, 14, 15.5, 18, 22, 26, 40–60. Spacing: 4, 8, 12, 16, 24, 32, 48. Radii: 7, 9, 11, 16. Motion: 120–200 ms, ease-out; press feedback on buttons and tabs; no scroll reveals; reduced-motion is respected.

## Layout

- Max width 1240 px; 64 px page gutters on desktop, 32 px tablet, 16 px mobile.
- Sticky header with brand and four module tabs. Tab bar is the primary navigation; panels are mutually exclusive.
- Each panel: cover block, quick start, chapters, sticky table of contents on desktop; the TOC becomes a wrapping chip row below 1120 px.
- Reading column capped by the grid; tables scroll horizontally inside a labelled region.
- Figures are self-made schematics: UI maps, focus diagram, timeline, fleet topology, shop map, budget receipt. No screenshots and no external images.

## Accessibility

- Tabs use `role="tablist"` / `role="tab"` / `role="tabpanel"`, arrow keys, Home/End, visible focus, and a live announcement.
- All tables have captions; horizontal scroll regions are keyboard-focusable.
- Text contrast targets WCAG 2.2 AA; callouts pair color with icon and text.
- Reduced motion disables smooth scrolling and transitions.
- Print styles switch to a light palette and hide navigation.

## Content rules

- Surface-level instructions only: what to click, where to set it, what to check. No internals, offsets, packets or memory details.
- Every section starts from a task, not from a feature name.
- Screenshots are intentionally absent. Schematics are labelled as schemes and use the real UI wording where it helps recognition.
