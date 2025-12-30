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

---

## Remaining Work - 3 Phase Plan

### Phase 1: Build Verification & Error Fixes
**Goal:** Ensure the current codebase compiles without errors

1. Run `pnpm build` to check for compilation errors
2. Fix any import errors (e.g., missing Link import)
3. Verify no JSX-in-frontmatter issues remain
4. Confirm build passes

**Known Issues to Check:**
- `case-study-classic.astro` - Link import may be missing
- `saas-pricing.astro` - Uses Link, verify imported
- `dashboard.astro` - Uses Link in multiple places

---

### Phase 2: WireframeCTA Integration (5 pages)
**Goal:** Replace remaining inline CTAs with WireframeCTA component

**Pages to update:**
1. `case-study-classic.astro` (~lines 379-410)
2. `case-study-visual.astro`
3. `job-posting.astro`
4. `saas-pricing.astro` (~lines 261-294)
5. `storytelling.astro`

---

### Phase 3: Cleanup & Documentation
**Goal:** Final verification and documentation updates

1. Run final `pnpm build`
2. Update this doc - mark CTA items complete
3. Mark intentionally skipped items:
   - showcase.astro (complex custom layouts)
   - modular.astro section headers/testimonials/stats (uses ModularCard/GridShowcase)
   - saas-pricing.astro hero (unique pricing layout)
