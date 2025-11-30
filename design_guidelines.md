# Design Guidelines: Bhavesh Ahire - Freelance Portfolio

## Design Approach
**Modern Glassmorphism Portfolio** - Drawing inspiration from contemporary developer portfolios like Brittany Chiang's and minimalist design systems. Focus on depth through glassmorphism, subtle shadows, and layered elements that create visual interest without overwhelming content.

## Core Design Elements

### Typography
- **Hero Heading**: Bold, large display font (3.5rem desktop, 2.5rem mobile) - use "Inter" or "Poppins" weight 700
- **Section Headings**: Semi-bold (2rem desktop, 1.5rem mobile) - weight 600
- **Body Text**: Regular weight 400, 1rem base size
- **Tagline/Subheadings**: Medium weight 500, 1.125rem
- Line height: 1.6 for body, 1.2 for headings

### Layout System
**Tailwind spacing primitives**: Use units of 4, 6, 8, 12, 16, 20, 24 (e.g., p-8, mb-12, gap-6)
- Section padding: py-20 desktop, py-12 mobile
- Container max-width: max-w-6xl mx-auto px-6
- Component spacing: mb-16 between major sections
- Grid gaps: gap-8 for project cards, gap-6 for skill items

### Color Application
- **Primary Accent**: #9381FF - CTAs, headings, hover states
- **Secondary Accent**: #B8B8FF - secondary buttons, borders, icons
- **Background Base**: #F8F7FF - main background
- **Warm Accent 1**: #FFEEDD - glassmorphism overlays, cards
- **Warm Accent 2**: #FFD8BE - hover effects, subtle highlights
- Glassmorphism: rgba(255, 238, 221, 0.15) with backdrop-blur-lg

## Component Library

### Hero Section
- Full viewport height (min-h-screen) with centered content
- Large background gradient from #F8F7FF to #B8B8FF (subtle, top to bottom)
- Name display: Extra large, gradient text (#9381FF to #B8B8FF)
- Tagline: Medium size below name with fade-in delay
- CTA Buttons: Primary (#9381FF bg, white text) + Secondary (outlined #B8B8FF border, purple text) side by side
- Floating geometric shapes in background (circles/squares with glassmorphism)

### About Me Section
- Two-column layout (desktop): Left - profile image placeholder with glassmorphic border, Right - bio text
- Single column (mobile) with image above text
- Bio in card with subtle glassmorphism effect (backdrop-blur-md, bg-white/10)
- Highlight badges: Small pills with icons showing "Hardworking", "Problem Solving", "Creative"

### Skills Section
- Grid layout: 4 columns desktop, 2 columns mobile
- Each skill card: Icon (use Heroicons via CDN), skill name, glassmorphic background
- Hover: Lift effect (translate-y-1) with shadow increase
- Icons colored with primary/secondary accents

### Projects Section
- Grid: 2 columns desktop, 1 column mobile
- Project cards with glassmorphism: Image placeholder at top, content below
- Each card includes: Project name (heading), brief description (2 lines), tech tags (small pills), "View Project" button
- Hover: Scale (1.02) with enhanced shadow

### Services Section
- 4 columns desktop, 2 columns tablet, 1 column mobile
- Service cards with large icons, service name, brief description
- Glassmorphic cards with hover lift effect
- Icons: Use Heroicons - Code, DevicePhone, Sparkles, ChartBar

### Testimonials Section
- Horizontal scroll cards (3 visible desktop, 1 mobile)
- Each testimonial: Quote text, author name, role
- Glassmorphic cards with quotation mark icon
- Cards have soft shadows and rounded corners (rounded-2xl)

### Contact Form
- Centered form (max-w-2xl)
- Input fields with glassmorphic styling: backdrop-blur-sm, border-2 border-purple/20
- Focus states: border-purple (#9381FF), outline-none
- Submit button: Full width, primary color, with loading state consideration
- Form validation feedback: Red border for errors, green check for valid

### Footer
- Dark glassmorphic section (bg-purple-900/20 with backdrop-blur)
- Social icons row (centered): LinkedIn, GitHub, Email, Twitter placeholders
- Copyright text centered below icons
- Hover on social icons: Scale and color shift to primary

## Animations
- **Page Load**: Hero content fades in sequentially (name → tagline → buttons) with 0.2s delays
- **Scroll Animations**: Sections fade-up as they enter viewport (use Intersection Observer)
- **Hover Effects**: Smooth transitions (0.3s ease) on all interactive elements
- **Button Hovers**: Slight scale (1.05) with shadow enhancement
- No excessive motion - keep subtle and professional

## Images
**Hero Section**: Large abstract gradient background (geometric patterns or subtle wave shapes) - decorative, not photograph
**About Section**: Professional headshot or avatar placeholder (circular, 300x300px)
**Project Cards**: Project thumbnail images (16:9 aspect ratio, 600x338px) showing app/web interfaces
All images should have proper alt text and lazy loading

## Responsive Breakpoints
- Mobile: < 768px (single column, stacked layout)
- Tablet: 768px - 1024px (2 columns where applicable)
- Desktop: > 1024px (full multi-column layouts)

## Accessibility
- All buttons and links have clear focus states (ring-2 ring-purple)
- Form labels properly associated with inputs
- Semantic HTML (header, main, section, footer)
- Sufficient color contrast ratios (WCAG AA minimum)