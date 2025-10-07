# Prashiskshan Design Guidelines

## Design Approach: Hybrid System

**Primary Framework**: Material Design 3 principles for dashboard/utility areas with custom landing page aesthetics
**Rationale**: Government education platform requiring professional trustworthiness (utility-focused) while maintaining engaging landing experience. The multi-role dashboard system demands consistency and familiarity, making Material Design 3 ideal for its component maturity and accessibility standards.

**Landing Page Inspiration**: Draw from modern SaaS platforms like Notion (clean professionalism) and government portals like Digital India (trust and credibility) - feature-rich hero section with NEP 2020 compliance messaging, statistics cards, and clear role-based CTAs.

---

## Core Design Elements

### A. Color Palette

**Light Mode:**
- Primary: `210 85% 45%` (Professional blue - government trust)
- Primary Variant: `210 90% 35%` (Darker blue for emphasis)
- Secondary: `150 60% 40%` (Educational green - growth/learning)
- Success: `142 71% 45%` (Status indicators)
- Warning: `38 92% 50%` (Alerts)
- Error: `0 84% 60%` (Critical actions)
- Background: `210 20% 98%` (Soft neutral)
- Surface: `0 0% 100%` (Cards/panels)
- Text Primary: `220 15% 15%`
- Text Secondary: `220 10% 45%`

**Dark Mode:**
- Primary: `210 80% 60%` (Brighter for contrast)
- Primary Variant: `210 85% 50%`
- Secondary: `150 55% 50%`
- Success: `142 65% 55%`
- Warning: `38 85% 55%`
- Error: `0 75% 65%`
- Background: `220 15% 10%` (Deep blue-black)
- Surface: `220 12% 15%` (Elevated cards)
- Text Primary: `210 15% 95%`
- Text Secondary: `210 10% 70%`

### B. Typography

**Font Stack**: 
- Primary: 'Inter' via Google Fonts (body, UI elements)
- Secondary: 'Poppins' (headings, hero text)
- Monospace: 'JetBrains Mono' (data tables, code)

**Scale**:
- Hero: text-5xl/6xl (landing only)
- H1: text-3xl/4xl font-bold
- H2: text-2xl/3xl font-semibold
- H3: text-xl/2xl font-medium
- Body: text-base leading-relaxed
- Small: text-sm
- Caption: text-xs text-secondary

### C. Layout System

**Spacing Primitives**: Use Tailwind units: **2, 4, 6, 8, 12, 16**
- Component padding: p-4 to p-6
- Section spacing: py-8 to py-16
- Card gaps: gap-4 to gap-6
- Container: max-w-7xl mx-auto px-4

**Grid Systems**:
- Dashboard: 12-column grid (grid-cols-12)
- Cards: 1/2/3/4 column responsive (grid-cols-1 md:grid-cols-2 lg:grid-cols-3)
- Admin analytics: 2-column split (lg:grid-cols-2)

### D. Component Library

**Navigation:**
- Top navbar: Sticky header with logo, role indicator, notifications bell, profile dropdown
- Sidebar (Dashboard): 240px fixed width, collapsible on mobile, icon + text items, active state with primary color left border
- Mobile: Bottom navigation bar for key dashboard actions

**Cards:**
- Elevated cards: shadow-md with rounded-lg borders
- Interactive cards: hover:shadow-lg transition
- Dashboard stat cards: Icon (top-left) + metric (large text) + label (small text) + trend indicator
- Internship cards: Company logo + title + location + stipend + tags + action buttons

**Forms:**
- Input fields: Outlined style with focus ring (ring-2 ring-primary)
- Labels: text-sm font-medium mb-2
- Validation: Inline error messages in error color below field
- File upload: Drag-drop zone with border-dashed styling

**Data Display:**
- Tables: Striped rows, sticky headers, hover:bg-surface-variant
- Charts: Chart.js with primary/secondary color scheme, rounded bars, smooth animations
- Status badges: Pill-shaped (rounded-full) with color-coded backgrounds (success/warning/error)
- Progress bars: Rounded with gradient fills showing completion

**Buttons:**
- Primary: bg-primary text-white rounded-lg px-6 py-3
- Secondary: border-2 border-primary text-primary (outline)
- Icon buttons: Circular (rounded-full) p-2
- Floating Action Button (FAB): Fixed bottom-right for quick actions
- Buttons on images: backdrop-blur-md bg-white/10 border border-white/20

**Modals & Overlays:**
- Modal: Centered with backdrop blur, max-w-2xl, shadow-2xl
- Drawer: Slide from right for detailed views
- Toast notifications: Top-right corner, auto-dismiss, with icons

**Dashboard-Specific:**
- Analytics cards: Chart + KPI metric + comparison text
- Activity feed: Timeline design with left border indicator
- Logbook entries: Expandable accordion with date headers
- Application tracking: Stepper component showing status progression

### E. Animations

**Minimal & Purposeful:**
- Page transitions: Fade-in only (duration-200)
- Card hover: Scale 1.02 + shadow lift (duration-150)
- Button interactions: Built-in states (no custom)
- Chart animations: Chart.js defaults (subtle entrance)
- Loading states: Skeleton screens (pulse animation)

**Explicitly Avoid**: Parallax, scroll-triggered animations, complex keyframes

---

## Landing Page Specifications

**Layout Structure:**
1. **Hero Section** (90vh): 
   - Left: Headline "Empowering India's Future Through NEP 2020-Compliant Internships" + subtitle + 4 role-based CTA buttons (Student/Company/Faculty/Admin) in 2x2 grid
   - Right: Large hero image showing diverse students in professional settings
   - Background: Subtle gradient (primary to secondary, 15% opacity)

2. **NEP 2020 Compliance Section** (auto height):
   - 4-column grid (lg:grid-cols-4): Compliance features with icons, percentages, descriptions

3. **Platform Statistics** (auto height):
   - 3-column grid: "25+ Students", "15+ Companies", "20+ Internships" with animated counters

4. **Role Features** (auto height):
   - Tabbed interface or separate sections for each role showing key features as cards (3-column grid)

5. **Testimonials** (auto height):
   - 2-column grid with student/company testimonials, photos, designations

6. **CTA Section** (60vh):
   - Centered: "Ready to Get Started?" + secondary hero image + primary CTA button

7. **Footer**: 
   - 4-column: About, Quick Links, Contact, Social Media + Newsletter signup

**Multi-Column Strategy**: Use 3-4 columns on desktop, 2 on tablet, 1 on mobile throughout landing page

---

## Images

**Required Images:**
1. **Hero Image** (Landing): Professional photo of diverse Indian students/interns in tech/lab environment - placement: right 50% of hero section (object-cover h-full)
2. **CTA Section Image**: Handshake or collaboration visual - placement: background with overlay
3. **Role Icons**: Custom illustrations for Student/Company/Faculty/Admin - placement: in role feature cards
4. **Company Logos**: 15+ placeholder company logos - placement: in internship cards and company directory
5. **User Avatars**: Profile photos for sample users - placement: testimonials, dashboards, activity feeds

---

## Dashboard Design Standards

- **Consistency**: All dashboards follow same header (breadcrumb + actions) + sidebar + main content structure
- **White Space**: Generous padding between sections (py-8), no cramped layouts
- **Hierarchy**: Clear visual separation using cards, dividers, and section headers
- **Responsiveness**: Sidebar collapses to hamburger <768px, cards stack to single column
- **Accessibility**: ARIA labels, keyboard navigation (Tab/Enter), focus indicators, WCAG AA contrast ratios

This design system ensures Prashiskshan presents as a trustworthy, professional government platform while maintaining modern UX standards across all user roles.