# Component Breakout Progress

> This document tracks the refactoring of wireframe pages to use reusable components.
> Check off items as they are completed across sessions.

## Components to Create

- [x] **WireframeBreadcrumb** - Back navigation with optional breadcrumb trail
- [x] **WireframeHero** - Hero sections with title, subtitle, CTA buttons
- [x] **WireframeSectionHeader** - Section title + description (centered/left/right)
- [x] **WireframeFeatureCard** - Icon + title + description cards
- [x] **WireframeCTA** - Final call-to-action sections
- [x] **WireframeTestimonial** - Customer quotes/testimonials
- [x] **WireframeStats** - Metric/stat display cards
- [x] **WireframePricingCard** - Individual pricing plan cards
- [x] **WireframeLogoGrid** - Social proof logo display

---

## Pages to Update

### classic.astro (High Priority - Most Patterns)
- [x] Replace hero section with WireframeHero
- [x] Replace section headers with WireframeSectionHeader
- [x] Replace feature cards with WireframeFeatureCard
- [x] Replace logo grid with WireframeLogoGrid
- [x] Replace testimonial with WireframeTestimonial
- [x] Replace pricing cards with WireframePricingCard
- [x] Replace final CTA with WireframeCTA

### showcase.astro
- [ ] Add WireframeBreadcrumb (not needed - no back nav in original)
- [ ] Replace hero with WireframeHero (complex hero, kept as-is)
- [ ] Replace section headers with WireframeSectionHeader
- [ ] Replace testimonials with WireframeTestimonial
- [ ] Replace final CTA with WireframeCTA (complex CTA, kept as-is)

### modular.astro
- [x] Replace hero with WireframeHero
- [ ] Replace section headers with WireframeSectionHeader (uses GridShowcase)
- [ ] Replace testimonials with WireframeTestimonial (uses ModularCard)
- [ ] Replace stats with WireframeStats (uses ModularCard)
- [x] Replace final CTA with WireframeCTA

### case-study-classic.astro
- [x] Replace back nav with WireframeBreadcrumb
- [ ] Replace final CTA with WireframeCTA

### case-study-visual.astro
- [x] Replace back nav with WireframeBreadcrumb
- [ ] Replace final CTA with WireframeCTA

### job-posting.astro
- [x] Replace back nav with WireframeBreadcrumb
- [ ] Replace section headers with WireframeSectionHeader
- [ ] Replace final CTA with WireframeCTA

### saas-pricing.astro
- [x] Replace back nav with WireframeBreadcrumb
- [ ] Replace hero with WireframeHero
- [ ] Replace section headers with WireframeSectionHeader
- [ ] Replace final CTA with WireframeCTA

### checkout.astro
- [x] Replace back nav with WireframeBreadcrumb

### product-listing.astro
- [x] Replace back nav with WireframeBreadcrumb

### dashboard.astro
- [x] Replace back nav with WireframeBreadcrumb

### storytelling.astro
- [ ] Replace final CTA with WireframeCTA

### index.astro (hub)
- [x] No changes needed (already uses components)

---

## Component Usage Summary

| Component | Pages Using It |
|-----------|----------------|
| WireframeBreadcrumb | 7 pages |
| WireframeHero | 6 pages |
| WireframeSectionHeader | 8+ pages |
| WireframeFeatureCard | 5+ pages |
| WireframeCTA | 9 pages |
| WireframeTestimonial | 3 pages |
| WireframeStats | 5 pages |
| WireframePricingCard | 2 pages |
| WireframeLogoGrid | 1+ pages |

---

## Notes

- All components should follow existing wireframe styling patterns
- Use `wireframe-box`, `doodle-border`, `wireframe-heading`, `wireframe-text` classes
- Apply theme colors via CSS custom properties: `var(--color-theme-*)`
- Test with ColorPaletteSelector after each page update
