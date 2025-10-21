# Design Guidelines: Ofir Barber - Luxury Barbershop Website

## Design Approach
**Reference-Based Approach**: Drawing inspiration from premium service industry leaders like high-end salons and luxury hospitality websites (e.g., premium hotel booking experiences, upscale salon chains). The design will emphasize sophistication, trust-building, and emotional connection while maintaining the existing luxury barber aesthetic.

**Core Principle**: Create an immersive, premium experience that conveys craftsmanship, tradition, and modern luxury.

---

## Color Palette

### Primary Colors (Dark Mode)
- **Background Base**: 0 0% 0% (pure black)
- **Background Elevated**: 0 0% 6% (dark gray)
- **Background Card**: 0 0% 10% (medium dark)

### Accent Colors
- **Primary Gold**: 43 71% 52% (rich gold - main brand color)
- **Gold Light**: 48 84% 80% (light gold for highlights)
- **Gold Dark**: 43 68% 38% (deep gold for depth)
- **Text Primary**: 0 0% 100% (white)
- **Text Secondary**: 0 0% 70% (light gray)
- **Text Muted**: 0 0% 50% (medium gray)

### Success/Action
- **WhatsApp Green**: 142 70% 49% (for WhatsApp CTA)

---

## Typography

### Font Families
- **Display/Headings**: 'Playfair Display' - serif font for luxury feel
- **Body/UI**: 'Rubik' - clean, modern Hebrew-friendly sans-serif

### Type Scale
- **Hero Headline**: 72px/900 weight (desktop), 48px (mobile)
- **Section Titles**: 56px/800 weight (desktop), 36px (mobile)
- **Card Titles**: 28px/700 weight
- **Body Large**: 20-22px/400 weight
- **Body Regular**: 16-18px/400 weight
- **Small/Caption**: 14px/300 weight

---

## Layout System

### Spacing Primitives
Use Tailwind spacing units: **4, 8, 12, 16, 20, 24, 32, 40** for consistent rhythm
- Component padding: p-8, p-12
- Section spacing: py-20, py-32
- Card spacing: p-8, p-12
- Grid gaps: gap-8, gap-12

### Container Widths
- Max content width: 1400px
- Standard sections: max-w-7xl
- Text content: max-w-4xl

---

## Component Library

### Navigation
- Fixed header with blur backdrop (backdrop-blur-xl)
- Semi-transparent background: rgba(0,0,0,0.85)
- Gold bottom border with low opacity
- Smooth shrink animation on scroll
- Gold gradient logo text
- Nav links with animated gold underline on hover

### Hero Section
- Full viewport height (100vh)
- Background: High-quality barbershop image (professional barber at work, luxury interior, or grooming tools)
- Dark overlay gradient (radial from center)
- Subtle geometric pattern overlay
- Floating "special offer" badge with gold gradient
- Large centered headline with gold gradient text
- Descriptive subheading
- Primary CTA button with shine animation

### Service Cards
- 3-4 column grid (responsive to 1 column on mobile)
- Dark gradient background with gold border on hover
- Large emoji/icon at top (64px)
- Service name in Playfair Display
- Short description
- Hover: lift animation (translateY -15px) with glow shadow

### Pricing Table
- Clean rows with alternating subtle backgrounds
- Service name | Price format
- Gold accent for featured services
- Contained in rounded card with gold border

### Gallery Section
- Masonry or grid layout showcasing work
- 3-4 columns on desktop, 2 on tablet, 1 on mobile
- Hover: zoom effect with overlay
- Before/after slider option for transformations

### WhatsApp Contact Integration
**Floating Action Button**: 
- Fixed position bottom-right corner
- Large circular button (64px diameter)
- WhatsApp green background with pulse animation
- WhatsApp icon in white
- Visible shadow for depth
- Mobile: slightly larger for thumb accessibility

**Contact Section**:
- Simple centered card
- Business hours display
- Address with map icon
- Large WhatsApp button: "צור קשר בוואטסאפ" with phone number
- Click opens WhatsApp with pre-filled message

### Footer
- Dark background (slightly lighter than body)
- Business info: name, address, hours
- Social media links (if applicable)
- Gold decorative divider at top
- Copyright notice

---

## Images

### Required Images
1. **Hero Background**: Professional barbershop interior or barber at work - warm lighting, premium atmosphere (full-width, high resolution)
2. **Gallery**: 8-12 before/after photos or finished haircut/styling work - consistent lighting and framing
3. **Service Icons**: Use emoji or Font Awesome icons for services (✂️, 💈, 🧔, etc.)

### Image Treatment
- Slight desaturation for sophistication
- Dark overlay on hero to ensure text readability
- Subtle zoom on hover for gallery items
- Lazy loading for performance

---

## Animations & Interactions

**Principle**: Minimal, purposeful animations - no distractions

### Approved Animations
- Fade-in on scroll for sections (opacity + translateY)
- Hover lift on cards (translateY -10px to -15px)
- Gold glow shadow on hover
- Smooth 0.3-0.4s transitions
- Hero background subtle zoom (scale 1.1 to 1.15)
- Floating animation for special offer badge
- Icon gentle float on service cards
- WhatsApp FAB pulse effect

### Avoid
- Excessive parallax effects
- Distracting continuous animations
- Long transition durations

---

## Responsive Behavior

### Breakpoints
- Mobile: < 768px
- Tablet: 768px - 1024px  
- Desktop: > 1024px

### Key Adaptations
- Navigation: Hamburger menu on mobile
- Grid: 1 column on mobile, 2-3 on tablet, 3-4 on desktop
- Typography: Reduce sizes by 30-40% on mobile
- Hero: Reduce height to 80vh on mobile
- Padding: Reduce section padding to py-12 on mobile
- WhatsApp FAB: Larger on mobile for easier tapping

---

## RTL Considerations
- All layouts flow right-to-left
- Gradients flow right-to-left
- Animations respect RTL direction
- Icons and decorative elements mirror appropriately

---

## Accessibility
- High contrast gold on black meets WCAG standards
- Focus states with gold outline
- Keyboard navigation support
- Touch targets minimum 44px on mobile
- Alt text for all images
- Semantic HTML structure