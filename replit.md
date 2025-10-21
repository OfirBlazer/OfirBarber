# Ofir Barber - Luxury Barbershop Website

## Overview

A luxury barbershop website for "Ofir Barber" located in Petah Tikva, Israel. The application is a modern, single-page website built with React and Express, featuring a premium dark-themed design with gold accents. The site showcases barbershop services, pricing, contact information, and includes WhatsApp integration for customer engagement. The design emphasizes a high-end, immersive experience with Hebrew (RTL) language support.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture

**Framework & Build System**
- React 18 with TypeScript for type-safe component development
- Vite as the build tool and development server for fast HMR and optimized production builds
- Single-page application (SPA) using Wouter for client-side routing

**UI Component System**
- Shadcn/ui component library with Radix UI primitives for accessible, customizable components
- Tailwind CSS for utility-first styling with custom theme configuration
- Design system based on luxury aesthetics: dark mode with gold color palette, serif fonts (Playfair Display) for headings, and sans-serif (Rubik) for body text
- RTL (right-to-left) layout support for Hebrew language

**State Management & Data Fetching**
- TanStack Query (React Query) for server state management
- Custom query client configuration with specific refetch and caching strategies
- Form handling with React Hook Form and Zod for validation

**Animation & Interactions**
- Custom scroll-based animations using Intersection Observer API (useScrollAnimation hook)
- Embla Carousel for potential image galleries
- CSS transitions and Tailwind animation utilities

### Backend Architecture

**Server Framework**
- Express.js with TypeScript for API routes and server logic
- Development and production build separation using tsx and esbuild
- Middleware for JSON parsing, URL encoding, and request/response logging

**Development Tools**
- Vite middleware integration for HMR in development mode
- Custom error overlay and dev banner for Replit environment
- Request duration logging for API endpoints

### Design System

**Color Palette**
- Primary: Gold tones (HSL: 43 71% 52%, with light and dark variants)
- Background: Pure black (0 0% 0%) with elevated surfaces at 6% and 10% lightness
- Accent: WhatsApp green (142 70% 49%) for CTA buttons
- Text hierarchy: White primary, 70% gray secondary, 50% gray muted

**Typography Scale**
- Display/Headings: Playfair Display (serif) for luxury feel
- Body/UI: Rubik (sans-serif) for readability and Hebrew support
- Scale ranges from 14px (small text) to 72px (hero headlines)

**Component Patterns**
- Section-based layout with decorative gold gradient borders
- Card components with glassmorphic effects (backdrop-blur, gradient backgrounds)
- Hover and active state elevations using custom CSS utilities
- Consistent spacing using Tailwind's 4px-based scale

### External Dependencies

**UI & Styling**
- Radix UI primitives for 20+ accessible component patterns (dialogs, dropdowns, tooltips, etc.)
- Tailwind CSS with custom configuration for theme, colors, and animations
- Google Fonts (Playfair Display, Rubik) loaded via CDN
- lucide-react for consistent iconography

**Data Layer**
- Drizzle ORM configured for PostgreSQL database
- @neondatabase/serverless for database connection
- Drizzle-Zod for schema validation integration
- PostgreSQL session storage using connect-pg-simple

**Development Tools**
- Replit-specific plugins: runtime error modal, cartographer, dev banner
- TypeScript for type safety across the stack
- PostCSS with Autoprefixer for CSS processing

**Utilities**
- date-fns for date manipulation
- clsx and tailwind-merge for conditional class name handling
- class-variance-authority for component variant management
- nanoid for unique ID generation

**Communication**
- WhatsApp integration via URL scheme for customer contact
- Phone number: 0522545548 with pre-filled message templates

### Database Schema

**Users Table** (PostgreSQL via Drizzle ORM)
- Primary structure defined but currently using in-memory storage (MemStorage class)
- Schema includes: id (UUID), username (unique), password fields
- Zod validation schemas for insert operations
- Placeholder for future database integration

### Routing & Navigation

**Client-Side Routes**
- `/` - Home page (single-page design with sections: Hero, Services, Pricing, About, Contact)
- Catch-all 404 handler for undefined routes
- Smooth scroll navigation to section anchors (hero, services, pricing, about, contact)

**API Routes**
- `/api/*` prefix reserved for backend endpoints
- Currently minimal server routes; storage interface prepared for future CRUD operations

### Build & Deployment

**Scripts**
- `dev`: Development server with tsx runtime
- `build`: Production build (Vite + esbuild for server bundling)
- `start`: Production server execution
- `db:push`: Drizzle migration push to database

**Build Configuration**
- Client builds to `dist/public`
- Server bundles to `dist` as ESM module
- Path aliases: `@/` for client source, `@shared/` for shared code, `@assets/` for assets