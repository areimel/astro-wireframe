# Approved Icons Whitelist

This document serves as the definitive whitelist of approved icons for use in this project. **ONLY USE ICONS FROM THIS LIST** to prevent build failures and ensure consistency.

## Icon Libraries Available

This project uses three icon libraries via astro-icon:
- **bx (Box Icons)** - Primary icon library (most comprehensive)
- **uil (Unicons)** - Secondary icons for specific use cases
- **simple-icons** - Brand and technology logos only

## ✅ APPROVED ICONS

### Box Icons (bx:) - PRIMARY LIBRARY

#### Navigation & UI
- `bx:bx-home` - Home icon
- `bx:bx-menu` - Hamburger menu
- `bx:bx-x` - Close/cancel icon
- `bx:bx-chevron-down` - Dropdown arrow
- `bx:bx-chevron-up` - Up arrow
- `bx:bx-chevron-left` - Left arrow
- `bx:bx-chevron-right` - Right arrow
- `bx:bx-arrow-back` - Back arrow
- `bx:bx-link-external` - External link
- `bx:bx-show` - View/eye icon
- `bx:bx-search` - Search icon
- `bx:bx-filter` - Filter icon

#### Actions & Controls
- `bx:bx-check` - Checkmark
- `bx:bx-check-circle` - Checkmark in circle
- `bx:bx-plus` - Plus/add icon
- `bx:bx-star` - Outline star
- `bx:bxs-star` - Filled star
- `bx:bx-heart` - Heart icon
- `bx:bx-rocket` - Launch/rocket icon
- `bx:bx-customize` - Customization
- `bx:bx-scan` - QR/barcode scanner
- `bx:bx-qr-scan` - QR code scanner

#### Content & Media
- `bx:bx-image` - Image/photo icon
- `bx:bx-photo-album` - Photo album
- `bx:bx-camera` - Camera icon
- `bx:bx-video` - Video icon
- `bx:bx-file-blank` - Document/file
- `bx:bx-book-reader` - Reading/book icon
- `bx:bx-palette` - Color palette

#### Communication
- `bx:bx-envelope` - Email/message
- `bx:bx-chat` - Chat/messaging
- `bx:bx-phone` - Phone icon
- `bx:bx-microphone` - Voice/audio input
- `bx:bx-volume-full` - Audio/sound

#### Business & Finance
- `bx:bx-briefcase` - Business/work
- `bx:bx-buildings` - Company/office buildings
- `bx:bx-dollar` - Currency/pricing
- `bx:bx-dollar-circle` - Money in circle
- `bx:bx-credit-card` - Payment/card
- `bx:bx-bar-chart` - Analytics/charts
- `bx:bx-target-lock` - Targeting/goals

#### Technical & Development
- `bx:bx-code` - Code/development
- `bx:bx-layout` - Layout/design
- `bx:bx-columns` - Split columns
- `bx:bx-grid` - Grid layout
- `bx:bx-grid-alt` - Alternative grid
- `bx:bx-carousel` - Carousel/slider
- `bx:bx-devices` - Multiple devices
- `bx:bx-mobile-alt` - Mobile device
- `bx:bx-font-size` - Typography/text size
- `bx:bx-data` - Data/database
- `bx:bx-cloud` - Cloud services

#### User & Profile
- `bx:bx-user` - User profile
- `bx:bxs-user` - Filled user icon
- `bx:bx-pointer` - Cursor/pointer

#### Security & Privacy
- `bx:bx-check-shield` - Security verification (NOT bx:bx-shield-check)
- `bx:bx-shield` - Protection/security

#### Accessibility
- `bx:bxs-keyboard` - Keyboard input
- `bx:bx-pause-circle` - Pause/control

#### Utility & Tools
- `bx:bx-history` - History/recent
- `bx:bx-calendar` - Date/calendar
- `bx:bx-time` - Time/clock
- `bx:bx-category` - Categories/organization
- `bx:bx-trending-up` - Trending/popular
- `bx:bx-brain` - AI/intelligence
- `bx:bx-brush` - Design/creative
- `bx:bx-map` - Location/mapping

#### Info & Help
- `bx:bx-info-circle` - Information
- `bx:bx-lightbulb` - Ideas/tips

#### Solid Variants (bxs:)
- `bx:bxs-briefcase` - Solid business icon
- `bx:bxs-window-alt` - Solid window
- `bx:bxs-data` - Solid data icon
- `bx:bxs-bot` - AI/bot icon
- `bx:bxs-file-find` - File search
- `bx:bxs-cloud-download` - Download from cloud
- `bx:bxs-bolt` - Lightning/power
- `bx:bxs-bolt-circle` - Lightning in circle
- `bx:bxs-wrench` - Tools/settings
- `bx:bxs-devices` - Multiple devices (solid)

#### Brand Icons (bxl:)
- `bx:bxl-github` - GitHub
- `bx:bxl-twitter` - Twitter/X
- `bx:bxl-facebook` - Facebook
- `bx:bxl-linkedin` - LinkedIn

### Unicons (uil:) - SECONDARY LIBRARY

#### Contact & Location
- `uil:map-marker` - Location pin
- `uil:envelope` - Email message
- `uil:phone` - Phone contact

#### Navigation
- `uil:arrow-right` - Right arrow

#### Time & Calendar
- `uil:calendar-alt` - Calendar alternative
- `uil:clock` - Time/clock

#### User & Settings
- `uil:setting` - Settings/preferences
- `uil:user` - User profile

#### Security
- `uil:shield-check` - Security verification

#### Data & Analytics
- `uil:chart-line` - Line chart
- `uil:cloud` - Cloud services

### Simple Icons - BRAND LOGOS ONLY

#### Frontend Technologies
- `simple-icons:react` - React framework
- `simple-icons:svelte` - Svelte framework
- `simple-icons:astro` - Astro framework
- `simple-icons:tailwindcss` - Tailwind CSS
- `simple-icons:alpinedotjs` - Alpine.js

#### Development Tools
- `simple-icons:javascript` - JavaScript
- `simple-icons:typescript` - TypeScript
- `simple-icons:figma` - Figma design tool
- `simple-icons:github` - GitHub platform
- `simple-icons:vercel` - Vercel hosting

#### Social Platforms
- `simple-icons:twitter` - Twitter/X
- `simple-icons:linkedin` - LinkedIn

## ❌ FORBIDDEN ICONS

**NEVER USE THESE ICONS** - they do not exist and will cause build failures:

- `bx:bx-shield-check` ❌ (Use `bx:bx-check-shield` instead)
- Any icon not listed in the approved sections above

## Icon Usage Rules

### 1. **Validation Before Use**
Before using ANY icon in code:
1. Check this approved list first
2. Only use icons from the approved sections
3. If you need a new icon, add it to this list first

### 2. **Preferred Icon Order**
When choosing icons, prefer in this order:
1. **bx:** icons (primary library - most comprehensive)
2. **uil:** icons (secondary - for specific use cases not covered by bx)
3. **simple-icons:** (brand logos only)

### 3. **Naming Conventions**
- Regular icons: `bx:bx-[name]`
- Solid variants: `bx:bxs-[name]`
- Brand icons: `bx:bxl-[name]` or `simple-icons:[name]`
- Unicons: `uil:[name]`

### 4. **Common Patterns**
- Use `bx:bx-check` for confirmations
- Use `bx:bx-x` for close/cancel actions
- Use `bx:bx-search` for search functionality
- Use `bx:bx-menu` for navigation toggles
- Use `bx:bx-check-shield` (NOT bx:bx-shield-check) for security

## Adding New Icons

If you need an icon not on this list:

1. **Search the Box Icons library first** at [boxicons.com](https://boxicons.com)
2. **Verify the exact icon name** in the Box Icons documentation
3. **Test the icon works** in a small component first
4. **Add it to this whitelist** with proper categorization
5. **Document the use case** for the icon

## Maintenance

This list should be updated whenever:
- New icons are added to the project
- Icons are found to be broken or non-existent
- New icon libraries are added to the project
- Existing icons are deprecated

**Last Updated:** 2025-08-17