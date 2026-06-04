# Globetrotter — Decisions Log

## Milestone 0: Setup and Planning
- **Destination chosen:** Accra, Ghana
- **Primary audience:** First-time international visitors and diaspora returnees seeking authentic cultural and food experiences
- **One design decision that reflects the destination:** Ghana's national green, gold, and red as the primary palette, with Kente-inspired geometric stripe accents as section dividers — referencing the city's aesthetic tradition of precise, meaningful ornamentation
- **Wireframe format used:** Digitally generated labeled diagrams (PNG files in `/wireframes/`)

## Milestone 1: HTML Structure
- **HTML structure choice — `<article>` for attraction cards and food entries:** Each attraction and restaurant is a self-contained piece of content that makes sense on its own, which is exactly what `<article>` is designed for. A `<div>` would work visually but carries no semantic meaning. Using `<article>` signals to browsers, screen readers, and search engines what these content blocks actually represent.
- **HTML structure choice — `<figure>` and `<figcaption>` for gallery images:** The `<figure>` element groups an image with its caption as a single semantic unit, and `<figcaption>` explicitly associates the caption text with the image above it. This is more meaningful than a `<div>` wrapper with a `<p>` tag — it tells the browser these two elements belong together, which matters for accessibility and for anyone reading the source.
- **One thing Claude generated that I changed:** The initial stub used bare placeholder `<!-- comments -->` for all content. I replaced these with real, researched content for each attraction, restaurant, and gallery image — including specific place names, addresses, descriptions, and alt text. Generic placeholder text doesn't let you evaluate whether the structure actually works for the content it's meant to hold.
- **One place where the wireframe guided a specific structure decision:** The food guide wireframe showed a horizontal card layout — image on the left, text block on the right. This required wrapping each `<article>` with both an `<img>` and a `<div class="food-entry-body">` as sibling children, rather than nesting the image inside the text block. The wireframe made it clear upfront that image and text needed to be flex siblings, not a parent-child relationship.

## Milestone 2: CSS Styling
_Add entries after applying styles._

## Milestone 3: Flexbox Layout
_Add entries after implementing Flexbox._

## Milestone 4: Responsive Design
_Add entries after implementing media queries._

## Stretch Features
_Add entries if you implement any stretch features._
