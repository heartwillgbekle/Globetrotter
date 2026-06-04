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
- **Color choice — Ghana national green (`#006B3F`) as the dominant brand color:** It anchors every high-visibility element (nav bar, page headers, card titles, buttons) and immediately reads as Ghanaian to anyone who knows the flag. The gold (`#FCD116`) is reserved for accent and interactive elements — highlights, hover states, active nav link, figcaption borders — which mirrors how Kente uses gold sparingly to make it feel precious rather than decorative noise.
- **Visual choice — Kente-inspired divider stripe:** Rather than a plain horizontal rule, the `.kente-divider` uses `repeating-linear-gradient` to produce a stripe of alternating green, gold, red, and terracotta bars. This is a CSS-only nod to Kente cloth geometry — it doesn't copy the pattern literally but borrows its structural idea: precise, repeating color bands that carry meaning. It appears between the nav and content on every page.
- **Claude suggestion rejected — rounded pill buttons:** An earlier version of the `.btn` style used `border-radius: 50px` for fully rounded pill-shaped buttons. I rejected this because it felt too playful and modern-startup for a destination with Accra's gravitas. Slightly rounded rectangles (`border-radius: 3px`) are more deliberate and serious, which matches the "deliberate restraint" aesthetic described in planning.md.
- **Style that didn't look right at first — the hero overlay gradient:** The first version used a flat `rgba(0,0,0,0.55)` overlay across the entire hero image, which made the image feel washed out and muddy. I changed it to a `linear-gradient` that's lighter at the top and darker at the bottom, so the image breathes at the top and the headline text at the bottom has enough contrast to be readable — without destroying the photo.

## Milestone 3: Flexbox Layout
- **Flexbox property choice — `flex: 1` on card bodies (`highlight-card-body`, `attraction-card-body`, `food-entry-body`):** Setting `flex: 1` on the text body of each card, combined with `display: flex; flex-direction: column` on the card itself, forces every card in a row to stretch to the same height — matching the tallest card — without any JavaScript or fixed heights. This is the most important Flexbox pattern in the layout because it means cards with more text don't stick out taller than their neighbors.
- **Layout that didn't match the plan — food entry image height:** The original CSS used a fixed `height: 280px` on `.food-entry-img`. When a restaurant entry had more text than 280px worth of height, the card grew but the image stopped, leaving a visible gap at the bottom of the image column. Replaced fixed height with `align-self: stretch` so the image automatically fills whatever height the text column creates — which is what the wireframe actually showed.
- **HTML structure adjustment — `highlight-card` needed `flex-direction: column`:** Adding `flex: 1` to `.highlight-card-body` only works if the parent card is itself a flex column container. The card element needed `display: flex; flex-direction: column` added to its CSS so that the image and body stack vertically and the body can expand downward. Without this structural rule on the parent, `flex: 1` on the child has no flex context to work within.

## Milestone 4: Responsive Design
_Add entries after implementing media queries._

## Stretch Features
_Add entries if you implement any stretch features._
