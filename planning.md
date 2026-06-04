# Globetrotter — Planning Document
**Destination:** Accra, Ghana

---

## Core Planning Questions

### 1. What location are you building this guide for, and why did you choose it?
Accra, Ghana — the capital city where West African tradition meets a surging contemporary creative scene. Accra carries deep historical weight: it was the epicenter of Ghana's independence movement, a hub of Pan-Africanism, and a city shaped by the legacy of the Transatlantic slave trade. At the same time, modern Accra pulses with Afrobeats, world-class contemporary art galleries, and a growing diaspora community that returns every December for "Detty December." It's a city most people know by name but don't truly know — and that gap is exactly what this guide aims to close.

### 2. Who is your primary audience?
First-time international visitors and diaspora returnees who want to go beyond the tourist surface. These are curious, culturally aware travelers — people who want authentic food, meaningful history, and the city's real social energy, not just sanitized highlights. They may be planning their first trip to Ghana, reconnecting with their heritage, or simply deciding whether Accra belongs on their list.

### 3. What do you want visitors to feel or know after spending 5 minutes on your site?
That Accra is layered — ancient and thrillingly modern at once. Visitors should leave with a sense that the city rewards those who look carefully: that behind the chaotic traffic and the vibrant markets is a place with serious intellectual and cultural depth. The feeling should be: *I need to go there.*

### 4. What's one design decision — color, layout, or tone — that reflects your destination's identity?
The color palette will be anchored in Ghana's national colors — deep forest green, bold gold, and red — which are not just national symbols but also reflect the warmth, earth, and vitality of the city itself. Geometric accents inspired by Kente cloth patterns will appear in section dividers and borders, reflecting Accra's aesthetic philosophy: deliberate, precise ornamentation that rewards the careful observer. The tone throughout will be warm and proud — the Ghanaian spirit of "you are welcome" baked into every page.

---

## Design Intent
*(Added before Milestone 2 CSS work)*

**Color palette and three words that describe the feeling:**
- Primary: Ghana Green (`#006B3F`), Ghana Gold (`#FCD116`), Ghana Red (`#CE1126`)
- Accent: Warm terracotta (`#C2713A`), Ocean blue (`#1A6B8A`), Off-white (`#FAF7F0`)
- Three words: **Vibrant. Rooted. Welcoming.**

**Typography:**
- Headings: *Playfair Display* (Google Fonts) — editorial weight, warmth, gravitas
- Body: *Lato* or *Open Sans* — clean and readable at all sizes
- This pairing reflects a city that takes itself seriously while remaining accessible

**One visual choice that connects to the destination's identity:**
Kente-inspired geometric stripe accents (alternating gold and green thin bars) used as section dividers. Kente cloth is one of Ghana's most recognizable cultural exports — using its structural geometry (rather than literally copying it) acknowledges the design tradition without being literal or superficial.

---

## Flexbox Layout Plan
*(Added before Milestone 3 implementation)*

### Navigation Bar
- Horizontal row of links at desktop width, with the site title/logo on the left and nav links on the right
- Wraps to a stacked centered column on mobile
- `justify-content: space-between` at desktop; `flex-direction: column` + `align-items: center` on mobile

### Home Page
- **Hero section:** Single full-width image/banner, text overlay centered — no flex needed here, just positioning
- **Intro section:** Two-column flex row at desktop (text left, small accent image right); single column on mobile
- **Featured highlights strip:** Three equal cards in a row (`flex: 1`, `gap`), wrapping to single column on mobile

### Top Attractions Page
- Three attraction cards in a horizontal row at desktop (`flex-wrap: wrap`, each card ~30% width)
- Each card: image on top, title below, description below that — stacked internally
- On tablet: 2 columns; on mobile: 1 column

### Food Guide Page
- Three restaurant entries stacked vertically (each entry is a wide horizontal card)
- Each entry: image on the left (fixed width), text block on the right — `flex-direction: row`
- On mobile: image stacks above text — `flex-direction: column`

### Photo Gallery Page
- Five+ images in a wrapping flex grid — `flex-wrap: wrap`, each image roughly 30–45% width
- Each item: image + caption stacked (`flex-direction: column`)
- On mobile: each image fills full width

---

## Breakpoints Plan
*(Added before Milestone 4 implementation)*

**Three device sizes and breakpoints:**
- **Mobile:** up to 767px — single column, stacked layouts, larger tap targets
- **Tablet:** 768px–1023px — two-column layouts where appropriate, nav still horizontal
- **Desktop:** 1024px and above — full multi-column layouts, wider max-width container

**Major layout shifts per section:**

| Section | Mobile | Tablet | Desktop |
|---|---|---|---|
| Nav bar | Stacked column, centered | Horizontal row | Horizontal row |
| Home intro | Single column | Two columns | Two columns |
| Attraction cards | 1 per row | 2 per row | 3 per row |
| Food guide entries | Image above text | Image left, text right | Image left, text right |
| Gallery images | 1 per row (full width) | 2 per row | 3 per row |

**Sections where mobile should feel genuinely different:**
- The navigation bar on mobile should feel like a clean centered menu, not just a squished horizontal bar
- The hero section on mobile should prioritize the image with a compact text overlay, not compete with it
- Gallery images on mobile should be full-width so photos actually have impact at small sizes
