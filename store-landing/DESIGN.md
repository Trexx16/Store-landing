# NovaStore Landing Page — Design Notes

## Colour palette
Both versions share one palette: primary blue #2563eb (darker #1d4ed8 on hover), amber accent #f59e0b for highlights, off-white background #f8fafc, white cards, slate text #1e293b, muted text #64748b, navy footer #0f172a. Stored as CSS variables in :root so the theme can be re-skinned from one place.

## Typography
A single Google Font, Poppins (300-700), is used throughout. It gives a friendly, modern feel suited to e-commerce, and one family keeps load times and visual noise low. Headings are bold with tight line-height; body copy uses 1.6.

## Layout approach
Mobile-first: base styles target small screens, then media queries at 600px and 992px enhance. Flexbox handles header, nav, hero, about and footer; CSS Grid drives products (1 column mobile, 2 tablet, 4 desktop). Images use max-width: 100% and aspect-ratio crops to avoid sideways scroll.

## Breakpoints
- Under 600px: hamburger nav, single-column grid.
- 600-991px: two-column grid, hero becomes a row.
- 992px and up: horizontal nav, four-column grid, wider spacing.

## Why Bootstrap in version 2
Bootstrap 5.3 demonstrates a component-driven workflow: its grid (col-12 col-sm-6 col-lg-3), navbar with navbar-expand-lg toggler, cards, badges and modal remove boilerplate and guarantee responsive, accessible behaviour. A small style.css overrides defaults (custom variables, gradient hero, card hover lift, footer) so the page still feels like branded NovaStore rather than a stock template.
