# Wireframe Pages Design Specification

## Overview
This document outlines the design and implementation specifications for 7 new wireframe pages based on 2025 design trends and user experience best practices.

## Design Principles
- **Hand-drawn Aesthetic**: All components use `doodle-border` class for sketchy wireframe appearance
- **Theme Integration**: Use theme classes (`theme-headline`, `theme-paragraph`, etc.) and CSS custom properties
- **Mobile-First**: Responsive design starting from mobile breakpoints
- **Accessibility**: Proper heading hierarchy, semantic HTML, keyboard navigation
- **Component Reusability**: Modular design allowing components to be used across different pages

## Page Specifications

### 1. Job Posting Page (`/wireframes/job-posting`)

**Purpose**: Professional job listing with clear information hierarchy
**Target Users**: Job seekers, HR professionals, recruiting agencies

**Layout Structure**:
```
┌─ Job Header (Company, Title, Location, Salary) ─┐
├─ Quick Stats (Type, Experience, Posted Date) ────┤
├─ Job Description ─────────────────────────────────┤
├─ Requirements & Qualifications ───────────────────┤
├─ Benefits & Perks ────────────────────────────────┤
├─ Application Process ──────────────────────────────┤
├─ Company Info Sidebar ─────────────────────────────┤
└─ Related Jobs ─────────────────────────────────────┘
```

**Key Components**:
- `JobCard.astro` - Main job listing display
- `RequirementsList.astro` - Structured requirements with icons
- `ApplicationFlow.astro` - Step-by-step application process
- `CompanyInfo.astro` - Company details sidebar

### 2. Case Study Classic (`/wireframes/case-study-classic`)

**Purpose**: Traditional problem-solution-results case study format
**Target Users**: UX/UI designers, agencies, consultants

**Layout Structure**:
```
┌─ Project Hero (Title, Client, Timeline) ──────────┐
├─ Problem Statement ────────────────────────────────┤
├─ Research & Discovery ─────────────────────────────┤
├─ Design Process ───────────────────────────────────┤
├─ Solution Overview ────────────────────────────────┤
├─ Results & Metrics ────────────────────────────────┤
├─ Key Learnings ────────────────────────────────────┤
└─ Project Credits ──────────────────────────────────┘
```

**Key Components**:
- `CaseStudyHero.astro` - Project header with metadata
- `ResultsMetrics.astro` - Before/after metrics display
- `ProjectTimeline.astro` - Process timeline visualization
- `ProcessSteps.astro` (existing) - Design methodology steps

### 3. Case Study Visual (`/wireframes/case-study-visual`)

**Purpose**: Image-heavy showcase with visual comparisons
**Target Users**: Design teams, creative agencies, portfolio viewers

**Layout Structure**:
```
┌─ Visual Hero (Large Project Image) ───────────────┐
├─ Project Overview (Split Left/Right) ─────────────┤
├─ Before/After Comparison ──────────────────────────┤
├─ Design Process Gallery ───────────────────────────┤
├─ Interactive Prototypes ───────────────────────────┤
├─ Team & Tools ─────────────────────────────────────┤
└─ More Projects ────────────────────────────────────┘
```

**Key Components**:
- `VisualHero.astro` - Large image-focused header
- `BeforeAfterComparison.astro` - Side-by-side image comparisons
- `GalleryGrid.astro` (existing) - Design process gallery
- `PrototypeShowcase.astro` - Interactive demo placeholders

### 4. E-commerce Checkout (`/wireframes/checkout`)

**Purpose**: Multi-step checkout process with form validation
**Target Users**: E-commerce developers, UX designers, online shoppers

**Layout Structure**:
```
┌─ Progress Indicator (Step 1, 2, 3, 4) ────────────┐
├─ Cart Summary (Items, Quantities, Prices) ────────┤
├─ Shipping Information Form ────────────────────────┤
├─ Payment Methods Selection ────────────────────────┤
├─ Order Review & Terms ─────────────────────────────┤
├─ Security Badges ──────────────────────────────────┤
└─ Checkout Actions ─────────────────────────────────┘
```

**Key Components**:
- `CheckoutProgress.astro` - Multi-step progress indicator
- `CartSummary.astro` - Shopping cart display with editing
- `PaymentMethods.astro` - Payment options with icons
- `OrderSummary.astro` - Final order review
- `SecurityBadges.astro` - Trust indicators

### 5. SaaS Pricing Page (`/wireframes/saas-pricing`)

**Purpose**: Clean pricing comparison with interactive features
**Target Users**: SaaS customers, subscription services, product managers

**Layout Structure**:
```
┌─ Pricing Header & Toggle (Monthly/Yearly) ────────┐
├─ Pricing Tiers Table (Free, Pro, Enterprise) ────┤
├─ Feature Comparison Matrix ────────────────────────┤
├─ Pricing Calculator ───────────────────────────────┤
├─ FAQ Section ──────────────────────────────────────┤
├─ Customer Testimonials ────────────────────────────┤
└─ Contact Sales CTA ────────────────────────────────┘
```

**Key Components**:
- `PricingTable.astro` - Advanced pricing tiers with highlighting
- `BillingToggle.astro` - Monthly/yearly billing switcher
- `FeatureComparison.astro` - Detailed feature matrix
- `PricingCalculator.astro` - Interactive cost calculator

### 6. Product Listing Page (`/wireframes/product-listing`)

**Purpose**: E-commerce product browse with filtering and search
**Target Users**: Online shoppers, e-commerce managers, UX designers

**Layout Structure**:
```
┌─ Search Bar & Breadcrumbs ─────────────────────────┐
├─ Filter Sidebar ┤ Product Grid (3-4 columns) ─────┤
├─ Sort Options   ┤ Product Cards with Images ──────┤
├─ Categories     ┤ Pricing & Reviews ──────────────┤
├─ Price Range    ┤ Quick Actions ──────────────────┤
├─ Brands         ┤ Load More / Pagination ─────────┤
└─ Applied Filters┴─────────────────────────────────┘
```

**Key Components**:
- `ProductGrid.astro` - Responsive product layout
- `FilterSidebar.astro` - Advanced filtering with categories
- `ProductCard.astro` - Individual product display
- `SearchBar.astro` - Enhanced search with suggestions
- `SortControls.astro` - Sorting options dropdown

### 7. Dashboard Page (`/wireframes/dashboard`)

**Purpose**: Analytics dashboard with charts and KPI tracking
**Target Users**: Data analysts, business users, dashboard designers

**Layout Structure**:
```
┌─ Dashboard Header & Navigation ────────────────────┐
├─ KPI Overview Cards (4 metrics) ──────────────────┤
├─ Primary Chart (Revenue/Traffic) ─────────────────┤
├─ Secondary Charts ┤ Recent Activity ──────────────┤
├─ Data Table       ┤ Quick Actions ───────────────┤
├─ Filters          ┤ Notifications ───────────────┤
└─ Export Options ──┴───────────────────────────────┘
```

**Key Components**:
- `MetricCard.astro` - KPI display cards with trends
- `ChartWidget.astro` - Chart/graph placeholders
- `DataTable.astro` - Sortable data tables
- `DashboardSidebar.astro` - Navigation and filters
- `ActivityFeed.astro` - Recent actions list

## Component Design Standards

### Typography
- **Headlines**: `theme-headline` class with `wireframe-heading` for hand-drawn font
- **Body Text**: `theme-paragraph` class with `wireframe-text`
- **Labels**: Small text with `theme-card-text`
- **Links**: `theme-link` class with hover states

### Colors
- **Primary Actions**: `theme-button-primary` with `var(--color-theme-button)`
- **Secondary Actions**: `theme-button-outline` 
- **Backgrounds**: `theme-card-bg`, `theme-section-bg`
- **Borders**: `style="border-color: var(--color-theme-stroke);"`

### Spacing
- **Sections**: `mt-16`, `mb-12` for major sections
- **Components**: `gap-6`, `gap-8` for grids
- **Cards**: `p-6`, `p-8` for internal padding
- **Text**: `mb-4`, `mb-6` for text spacing

### Icons
- **Consistent Library**: Only `bx:` icons (Box Icons)
- **Sizing**: `w-4 h-4`, `w-5 h-5`, `w-6 h-6`
- **Colors**: `style="color: var(--color-theme-button);"`
- **Static Usage**: Always use static `<Icon name="..." />`, never dynamic

### Responsive Design
- **Mobile**: Base styles, single column
- **Tablet**: `md:` prefix, 2-column grids
- **Desktop**: `lg:` prefix, 3-4 column grids
- **Large**: `xl:` prefix, maximum widths

## Implementation Priority

### Phase 1: Core Components (Week 1)
1. E-commerce components (ProductGrid, FilterSidebar, CartSummary)
2. Dashboard components (MetricCard, ChartWidget, DataTable)
3. Case study components (CaseStudyHero, BeforeAfterComparison)
4. Job posting components (JobCard, RequirementsList)

### Phase 2: Advanced Components (Week 2)
1. Pricing components (PricingTable, BillingToggle, Calculator)
2. Checkout components (CheckoutProgress, PaymentMethods)
3. Dashboard sidebar and activity feeds
4. Interactive elements and toggles

### Phase 3: Page Assembly (Week 3)
1. Build all 7 wireframe pages using completed components
2. Test responsive behavior across breakpoints
3. Verify theme integration across all 17 color palettes
4. Update navigation and hub page

### Phase 4: Testing & Optimization (Week 4)
1. Build testing and error resolution
2. Performance optimization
3. Accessibility audit
4. Documentation updates

## Success Metrics
- ✅ All pages build without errors
- ✅ Responsive design works on mobile, tablet, desktop
- ✅ Theme switching works across all 17 palettes
- ✅ Components are reusable across different contexts
- ✅ Hand-drawn wireframe aesthetic is consistent
- ✅ Navigation integration is seamless
- ✅ Page load times are under 2 seconds

## Technical Requirements
- **Astro 5.x** compatibility
- **TypeScript** interfaces for all component props
- **TailwindCSS 4.x** utility classes
- **Theme system** integration with CSS custom properties
- **Mobile-first** responsive design
- **Accessibility** WCAG 2.1 AA compliance
- **Performance** optimized images and minimal JS

This specification serves as the blueprint for creating a comprehensive wireframe page system that showcases modern 2025 design patterns while maintaining consistency with the existing codebase architecture.