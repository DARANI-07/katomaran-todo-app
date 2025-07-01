# TaskFlow - Task Management Application

## Overview

TaskFlow is a full-stack task management application built with a modern React frontend and Express.js backend. The application provides comprehensive task management features including task creation, editing, sharing, and real-time collaboration. It uses PostgreSQL for data persistence and integrates with Replit's authentication system for secure user management.

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript
- **UI Library**: shadcn/ui components built on Radix UI primitives
- **Styling**: Tailwind CSS with CSS variables for theming
- **State Management**: TanStack Query (React Query) for server state
- **Routing**: Wouter for client-side routing
- **Form Handling**: React Hook Form with Zod validation
- **Build Tool**: Vite with ESM modules

### Backend Architecture
- **Framework**: Express.js with TypeScript
- **Authentication**: Replit Auth with OpenID Connect
- **Session Management**: Express sessions with PostgreSQL storage
- **API Design**: RESTful endpoints with proper HTTP status codes
- **Validation**: Zod schemas for request/response validation
- **Error Handling**: Centralized error middleware

## Key Components

### Database Layer
- **ORM**: Drizzle ORM with PostgreSQL dialect
- **Database**: Neon serverless PostgreSQL
- **Connection**: WebSocket-based connection pooling
- **Migrations**: Drizzle Kit for schema management

### Authentication System
- **Provider**: Replit Auth (OpenID Connect)
- **Session Storage**: PostgreSQL-backed sessions
- **Authorization**: Route-level protection with middleware
- **User Management**: Automatic user creation and profile management

### Task Management
- **CRUD Operations**: Full task lifecycle management
- **Filtering & Sorting**: Status, priority, and date-based filtering
- **Pagination**: Server-side pagination for performance
- **Task Sharing**: Email-based task sharing between users
- **Statistics**: Task completion and priority analytics

### UI Components
- **Design System**: Consistent component library with variants
- **Responsive Design**: Mobile-first approach with breakpoint management
- **Accessibility**: ARIA-compliant components
- **Theming**: CSS variables for light/dark mode support

## Data Flow

### User Authentication Flow
1. User visits application
2. Unauthenticated users see landing page
3. Login redirects to Replit Auth
4. Successful auth creates/updates user record
5. Session established with secure cookies

### Task Management Flow
1. Frontend makes authenticated API requests
2. Express middleware validates session
3. Controllers process business logic
4. Storage layer interacts with database
5. Responses formatted and cached by React Query

### Real-time Updates
- React Query automatic refetching
- Optimistic updates for better UX
- Error boundaries for graceful failure handling

## External Dependencies

### Core Dependencies
- **@neondatabase/serverless**: PostgreSQL connection
- **drizzle-orm**: Database ORM and query builder
- **@tanstack/react-query**: Server state management
- **react-hook-form**: Form handling and validation
- **wouter**: Lightweight routing
- **date-fns**: Date manipulation utilities

### UI Dependencies
- **@radix-ui/***: Accessible UI primitives
- **tailwindcss**: Utility-first CSS framework
- **class-variance-authority**: Component variant management
- **lucide-react**: Icon library

### Development Dependencies
- **typescript**: Type safety
- **vite**: Build tool and dev server
- **esbuild**: Production bundling
- **drizzle-kit**: Database migrations

## Deployment Strategy

### Development Environment
- **Dev Server**: Vite dev server with HMR
- **API Server**: tsx for TypeScript execution
- **Database**: Neon development database
- **Environment**: Replit-specific optimizations

### Production Build
- **Frontend**: Vite build to static assets
- **Backend**: esbuild bundle for Node.js
- **Database**: Production PostgreSQL instance
- **Deployment**: Single-command deployment script

### Environment Configuration
- **DATABASE_URL**: PostgreSQL connection string
- **SESSION_SECRET**: Session encryption key
- **REPLIT_DOMAINS**: Allowed domains for auth
- **NODE_ENV**: Environment mode detection

## Changelog

```
Changelog:
- June 30, 2025. Initial setup
- June 30, 2025. Enhanced with advanced features: 
  * Voice control with speech recognition
  * Gamification system with points, levels, and achievements
  * Mood-based task assignment (focused, creative, energetic, calm)
  * Calendar view with monthly summaries
  * Analytics dashboard with charts and insights
  * Animated task completion with confetti
  * Minimal UI mode toggle
  * Comprehensive task management with advanced filtering
  * All features integrated into tabbed interface
- January 1, 2025. Successfully migrated from Replit Agent to standard Replit environment:
  * Organized project structure with proper server/client separation
  * Set up PostgreSQL database with comprehensive schema for all features
  * Implemented Google OAuth authentication with session management
  * Created complete React frontend with shadcn/ui components
  * Added comprehensive task management with CRUD operations
  * Implemented habit tracker with streak counting and visual progress
  * Added analytics dashboard with productivity insights
  * Created calendar view with task scheduling and deadline alerts
  * Integrated voice control for accessibility
  * Added gamification with points, levels, and achievements
  * Implemented mood-based task assignment system
  * Added animated task completion with confetti effects
  * All advanced features fully functional and ready for use
- January 1, 2025. Enhanced with AI voice assistant and comprehensive features:
  * Implemented AI voice assistant with OpenAI integration and intelligent fallback parsing
  * Added email notifications with natural language due dates ("today", "tomorrow", "yesterday")
  * Created automated due date alerts and reminder system
  * Enhanced UI with vibrant color scheme and gradient backgrounds
  * Added gamification system with achievements, points, levels, and progress tracking
  * Implemented colorful priority and mood-based task styling
  * Added animated task completion effects and visual feedback
  * Created comprehensive progress tracking with streaks and weekly goals
  * Fixed speech recognition errors and improved voice command processing
  * Made application visually attractive with animated elements and gradients
```

## User Preferences

```
Preferred communication style: Simple, everyday language.
```