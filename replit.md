# Bhavesh Ahire - Freelance Portfolio

## Overview

This is a modern portfolio website for Bhavesh Ahire, a freelance developer and student specializing in web development, mobile apps, and UI/UX design. The site showcases skills, projects, services, and provides contact functionality. Built with a glassmorphism design approach, the portfolio emphasizes visual depth and modern aesthetics while maintaining optimal performance and user experience.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture

**Framework & Build System**
- **React 18** with TypeScript for type-safe component development
- **Vite** as the build tool and development server, providing fast HMR and optimized production builds
- **Wouter** for lightweight client-side routing (instead of React Router)

**UI Component System**
- **shadcn/ui** component library built on Radix UI primitives
- **Tailwind CSS** for utility-first styling with custom design tokens
- Custom glassmorphism effects and animations throughout
- Responsive design with mobile-first approach

**State Management & Data Fetching**
- **TanStack Query (React Query)** for server state management and caching
- Local component state with React hooks
- No global state management library (keeping it simple)

**Design System**
- Custom color palette defined in CSS variables (primary: #9381FF, secondary: #B8B8FF, warm accents)
- Typography using Inter and Poppins fonts
- Consistent spacing system based on Tailwind's spacing scale
- Elevation effects using custom CSS classes (hover-elevate, active-elevate-2)

**Key Features**
- Intersection Observer API for scroll-triggered animations
- Typewriter effect for hero section
- 3D tilt effects on project cards
- Form validation for contact section
- Theme toggle (light/dark mode) with localStorage persistence
- Mobile-responsive navigation with hamburger menu

### Backend Architecture

**Server Framework**
- **Express.js** with TypeScript running on Node.js
- Middleware for JSON parsing, URL encoding, and request logging
- Custom logging system that tracks API requests with duration and response data

**Development Setup**
- **Vite middleware mode** for development with HMR
- Separate build processes for client (Vite) and server (esbuild)
- SSR-ready architecture (though currently serving SPA)

**Storage Layer**
- In-memory storage implementation (`MemStorage` class)
- Interface-based design (`IStorage`) allowing easy swapping to persistent storage
- Basic user CRUD operations defined (currently minimal usage)

**API Design**
- RESTful endpoints prefixed with `/api`
- All routes registered through centralized `registerRoutes` function
- Error handling with proper HTTP status codes

### Database Schema

**ORM & Migration**
- **Drizzle ORM** configured for PostgreSQL (via `@neondatabase/serverless`)
- Schema-first approach with type generation
- Zod validation schemas generated from database schema

**Current Schema**
- `users` table with UUID primary keys
  - `id`: Auto-generated UUID
  - `username`: Unique text field
  - `password`: Text field for authentication

**Note**: The database configuration expects a `DATABASE_URL` environment variable. The application is set up for PostgreSQL but may not be actively using it yet. The in-memory storage suggests the database integration is prepared but not yet implemented for core features.

## External Dependencies

### UI Libraries
- **Radix UI** - Comprehensive set of unstyled, accessible UI primitives (accordion, dialog, dropdown, popover, etc.)
- **Lucide React** - Icon library (implied by imports like `Mail`, `Github`, `ChevronDown`)
- **Tailwind CSS** - Utility-first CSS framework with custom configuration
- **class-variance-authority** - Utility for managing component variants
- **clsx** & **tailwind-merge** - Class name merging utilities

### Forms & Validation
- **React Hook Form** - Form state management
- **@hookform/resolvers** - Validation resolvers for React Hook Form
- **Zod** - Schema validation library
- **drizzle-zod** - Integration between Drizzle ORM and Zod

### Data Fetching
- **TanStack Query** - Async state management and data fetching

### Carousel & Animations
- **embla-carousel-react** - Carousel/slider component
- **cmdk** - Command menu component

### Database & Backend
- **Drizzle ORM** - TypeScript ORM for SQL databases
- **@neondatabase/serverless** - Neon database driver for serverless environments
- **PostgreSQL** - Relational database (via Neon)
- **connect-pg-simple** - PostgreSQL session store for Express

### Development Tools
- **Replit plugins** - Development tools for Replit environment (cartographer, dev-banner, runtime-error-modal)
- **tsx** - TypeScript execution for development
- **esbuild** - JavaScript bundler for production builds

### Fonts
- **Google Fonts** - Inter and Poppins font families loaded via CDN

### Asset Management
- Custom asset directory (`attached_assets`) for generated images including:
  - Profile images (AI-generated professional portrait)
  - Hero backgrounds
  - Project screenshots (Campus Sphere, ironSpeech, Vimero, Placement Dashboard)

## Recent Changes (November 2025)

### Enhanced Creative Features
- **Hero Section**: Typewriter animation with rotating taglines, floating particle effects, mouse-following gradient blob, animated scroll indicator
- **About Section**: Animated profile image with glow effects, staggered badge animations, Rocket icon badge (replaces emoji per design guidelines)
- **Stats Section**: New animated counter cards (15+ projects, 20+ clients, 3+ years experience, 8 certifications) with scroll-triggered animations
- **Skills Section**: Animated progress bars with percentages, grid layout with hover effects
- **Projects Section**: 3D tilt effect on cards with glare overlay, category filter tabs (All, Web, Mobile, Design), staggered reveal animations
- **Navigation**: Mobile hamburger menu with animated icon and slide-out panel
- **Scroll Progress**: Fixed progress bar at page top with gradient coloring
- **CSS Animations**: Float, gradient, blink, bounce-slow keyframes with smooth scroll behavior

### Design Guidelines Compliance
- All emojis replaced with Lucide icons
- No `text-primary` class used for standard text
- Semantic color tokens used throughout