# ARDA Astro Website Template - Project Context for Qwen Code

## Project Overview

This is the **ARDA Astro Website Template**, a modern, feature-rich website template built by the Advanced Research & Development Agency (ARDA) using **Astro 5** and **TailwindCSS 4**. It's designed for SAAS platforms, startups, marketing websites, landing pages, and blogs.

The project implements a unique **hand-drawn wireframe theme** using DoodleCSS, providing a sketchy, doodle-like aesthetic throughout the site. It also features a sophisticated **multi-palette color system** for dynamic theme switching.

## Key Technologies

- **Astro 5.x**: Static site generator with component islands architecture.
- **TailwindCSS 4.x**: Utility-first CSS framework, configured via the Vite plugin.
- **TypeScript**: Type safety throughout the project.
- **Content Collections**: Structured content management using Zod schemas for blog posts, case studies, products, and team members.
- **MDX**: Markdown with JSX support.
- **Astro Icon**: Icon system integrating Box Icons (bx), Unicons (uil), and Simple Icons.
- **DoodleCSS**: Provides the hand-drawn wireframe aesthetic.

## Project Structure

```
arda-astro-template/
├── public/                     # Static assets
│   ├── images/                # Image assets organized by section
│   └── hero-1.svg            # Hero illustration
├── src/
│   ├── components/            # Reusable Astro components
│   │   ├── navbar/           # Navigation with dropdown support
│   │   ├── ui/               # Base UI components (buttons, links, icons)
│   │   ├── styleguide/       # Design system components
│   │   ├── wireframes/       # Wireframe-specific components
│   │   └── PopupComponents/  # Modal system components
│   ├── content/              # Content Collections
│   │   ├── config.ts         # Collection schemas (Zod validation)
│   │   ├── blog/            # Blog posts (.md files)
│   │   ├── case-studies/    # Case study content
│   │   ├── products/        # Product showcases
│   │   └── team/           # Team member profiles
│   ├── data/               # JSON configuration files
│   │   ├── color-palettes.json  # Multi-theme color system
│   │   ├── navigation.json     # Site navigation structure
│   │   └── links.json         # External links
│   ├── layouts/            # Page layouts
│   │   ├── Layout.astro    # Base layout with SEO
│   │   └── BlogLayout.astro # Blog post layout
│   ├── pages/              # File-based routing
│   │   ├── styleguide/     # Design system documentation
│   │   ├── wireframes/     # Wireframe pages section
│   │   ├── blog/           # Blog section + [slug] pages
│   │   ├── case-studies/   # Case studies + [slug] pages  
│   │   ├── products/       # Products + [slug] pages
│   │   └── *.astro         # Static pages
│   ├── assets/            # Component-specific images
│   └── styles/           # Global CSS styles
├── CLAUDE.md             # AI development instructions for consistency
└── package.json
```

## Building and Running

This project uses **pnpm** as the package manager.

### Development

1.  **Install Dependencies**:
    ```bash
    pnpm install
    ```
2.  **Start Development Server**:
    ```bash
    pnpm dev
    ```
    The site will be available at `http://localhost:4321`.

### Production

1.  **Build for Production**:
    ```bash
    pnpm build
    ```
2.  **Preview Production Build**:
    ```bash
    pnpm preview
    ```

## Development Conventions

### Design System & Theme Integration

- **Multi-Palette Color System**: The project uses a sophisticated theme system defined in `src/data/color-palettes.json`. There are 9 distinct color palettes ranging from light to dark modes.
- **Theme Classes**: Use predefined theme classes like `theme-headline`, `theme-paragraph`, `theme-button-primary`, `theme-card-bg`, etc., for consistent styling across themes. *Avoid hard-coded colors.*
- **CSS Custom Properties**: For dynamic elements like borders or accents that need to respond to theme changes, use CSS custom properties (e.g., `style="border-color: var(--color-theme-stroke);"`, `style="color: var(--color-theme-button);"`)
- **Color Palette Selector**: A component (`ColorPaletteSelector.astro`) allows real-time switching between themes, with persistence via localStorage.

### Styleguide

- A comprehensive design system documentation is available at `/styleguide`. Always reference this for component examples, color usage, typography, buttons, cards, icons, and spacing.
- This ensures consistency and provides copy-paste ready examples.

### Component Development

- **Path Aliases**: Use `@/*` for `src/*` and `~/*` for the project root.
- **UI Components**: Reusable base components are in `src/components/ui/` (e.g., `Button.astro`). Always check for existing components before creating new ones.
- **Wireframe Components**: Components specific to the wireframe aesthetic are in `src/components/wireframes/` (e.g., `ProcessSteps.astro`, `GalleryGrid.astro`).
- **Icons**: Use the `astro-icon` system. Prefer `bx:` (Box Icons) icons. *Always check `project_docs/approved-icons.md` before using any icon* to avoid build failures. Use static icon components (`<Icon name="bx:name" />`) and never use them dynamically in `.map()` calls.
- **Modal System**: A reusable modal system is available in `src/components/PopupComponents/`, using a data-attribute system (`data-modal-open`, `data-modal-close`) for interaction.

### Wireframe System

- The project features a dedicated section for wireframe landing page layouts at `/wireframes`.
- A `WIREFRAME_DESIGN_PLAN.md` outlines the design and implementation for new wireframe pages.
- Reusable wireframe components are located in `src/components/wireframes/`.
- The aesthetic uses `doodle-border` class and theme classes for consistency.

### AI Development Guidelines (CLAUDE.md)

This project has a specific `CLAUDE.md` file that provides guidance for AI assistants (like Claude Code) working with the codebase. It covers:
- Development commands
- Project architecture details
- Component development guidelines (emphasizing styleguide reference and theme integration)
- Icon system rules (especially the approved icons whitelist)
- Modal system usage
- Wireframe system workflow
- Color system instructions

It is highly recommended to review `CLAUDE.md` for any development work to maintain consistency and avoid common pitfalls.

## Important Files

- `README.md`: Main project documentation.
- `package.json`: Project dependencies and scripts.
- `astro.config.mjs`: Astro configuration.
- `tsconfig.json`: TypeScript configuration.
- `src/data/navigation.json`: Site navigation structure.
- `src/data/color-palettes.json`: Theme definitions.
- `src/layouts/Layout.astro`: Base page layout.
- `CLAUDE.md`: AI development instructions.
- `WIREFRAME_DESIGN_PLAN.md`: Specifications for wireframe pages.
- `project_docs/approved-icons.md`: Whitelist of approved icons.