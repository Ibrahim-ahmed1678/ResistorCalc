# Replit.md

## Overview

This is a full-stack Resistor Color Code Calculator web application built with React, Express, and PostgreSQL. The application provides an interactive tool for electronics enthusiasts to calculate resistor values from color bands and perform reverse lookups to find color combinations for desired resistance values.

## System Architecture

The project follows a monorepo structure with a clear separation between client-side and server-side code:

- **Frontend**: React with TypeScript, using Vite as the build tool
- **Backend**: Express.js server with TypeScript
- **Database**: PostgreSQL with Drizzle ORM
- **UI Framework**: Shadcn/ui components with Tailwind CSS
- **State Management**: TanStack Query for server state management
- **Routing**: Wouter for client-side routing

## Key Components

### Frontend Architecture
- **React Application**: Located in `/client` directory
- **Component Library**: Shadcn/ui components for consistent UI design
- **Styling**: Tailwind CSS with custom CSS variables for theming
- **Build Tool**: Vite with hot module replacement for development
- **Type Safety**: Full TypeScript implementation

### Backend Architecture
- **Express Server**: RESTful API with middleware for logging and error handling
- **Database Layer**: Drizzle ORM for type-safe database operations
- **Storage Interface**: Abstracted storage layer with in-memory implementation for development
- **Development Setup**: Vite integration for seamless development experience

### Database Schema
- **Users Table**: Basic user management with username/password authentication
- **Schema Definition**: Centralized in `shared/schema.ts` for type sharing between client and server
- **Migration Support**: Drizzle migrations configured for PostgreSQL

### UI Components
- **Resistor Calculator**: Interactive color band selection and real-time calculation
- **Color Palette**: Dynamic color selection based on band type (digit, multiplier, tolerance)
- **Resistor Visualization**: Visual representation of resistor with clickable color bands
- **Results Display**: Formatted resistance values with tolerance ranges
- **Reverse Lookup**: Input resistance value to find color combinations
- **Reference Charts**: Educational color code reference tables

## Data Flow

1. **User Interaction**: User selects resistor band count and clicks on bands to activate selection
2. **Color Selection**: User chooses colors from the dynamic palette based on band type
3. **Real-time Calculation**: Application calculates resistance value using resistor color code formulas
4. **Results Display**: Shows formatted resistance value, tolerance, min/max ranges, and E-series classification
5. **Reverse Lookup**: User can input desired resistance to find matching color combinations

## External Dependencies

### Frontend Dependencies
- **React Ecosystem**: React 18 with TypeScript support
- **UI Components**: Radix UI primitives with Shadcn/ui wrapper components
- **State Management**: TanStack Query for server state and caching
- **Styling**: Tailwind CSS with PostCSS processing
- **Utilities**: Class-variance-authority for component variants, clsx for conditional classes

### Backend Dependencies
- **Database**: Neon serverless PostgreSQL with Drizzle ORM
- **Server**: Express.js with TypeScript execution via tsx
- **Session Management**: Connect-pg-simple for PostgreSQL session storage
- **Build Tools**: ESBuild for production bundling

### Development Tools
- **Replit Integration**: Custom plugins for development environment
- **Error Handling**: Runtime error overlay for better debugging
- **Hot Reload**: Vite HMR for instant development feedback

## Deployment Strategy

### Development Environment
- **Command**: `npm run dev` - Starts development server with hot reload
- **Database**: Uses DATABASE_URL environment variable for PostgreSQL connection
- **Port Configuration**: Server runs on port 5000 with external port 80

### Production Build
- **Build Process**: `npm run build` - Compiles both client and server code
- **Client Build**: Vite builds React app to `dist/public`
- **Server Build**: ESBuild bundles server code to `dist/index.js`
- **Start Command**: `npm run start` - Runs production server

### Database Management
- **Schema Push**: `npm run db:push` - Pushes schema changes to database
- **Migrations**: Configured in `drizzle.config.ts` for PostgreSQL
- **Environment**: Requires DATABASE_URL environment variable

## Changelog

Changelog:
- June 26, 2025. Initial setup

## User Preferences

Preferred communication style: Simple, everyday language.