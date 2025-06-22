# CryptoBrute Pro - Multi-Repository Brute Force Platform

## Overview
CryptoBrute Pro is a comprehensive cryptocurrency brute force platform that integrates multiple external repositories for wallet discovery and cryptographic operations. The application provides a sophisticated dashboard for managing brute force operations across different methodologies including BlockHub, pyExplorer, Mnemonic Recovery, Pyromid, and REDCrypto.

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript
- **Build Tool**: Vite for development and production builds
- **Styling**: Tailwind CSS with a custom dark theme and CSS variables
- **UI Components**: shadcn/ui component library with Radix UI primitives
- **State Management**: TanStack Query for server state management
- **Routing**: Wouter for lightweight client-side routing
- **Real-time Communication**: WebSocket integration for live updates

### Backend Architecture
- **Runtime**: Node.js with Express.js server
- **Language**: TypeScript with ES modules
- **Database**: PostgreSQL with Drizzle ORM
- **Database Provider**: Neon Database serverless
- **Session Management**: PostgreSQL-based sessions with connect-pg-simple
- **Real-time**: WebSocket server for bidirectional communication
- **Process Management**: Worker threads for CPU-intensive operations

### Repository Integration
The system integrates with five external Python-based cryptocurrency tools:
- BlockHub: Blockchain-based wallet and key discovery
- pyExplorer: Address exploration and validation
- Dumper-Mnemonic: Seed phrase recovery and generation
- Pyromid: Hierarchical cryptocurrency analysis
- REDCryptoMAGIC: Advanced cryptographic operations

## Key Components

### Database Schema
- **Users**: Authentication and user management
- **Bruteforce Operations**: Track running operations with status, configuration, and metrics
- **Bruteforce Results**: Store successful key discoveries with validation status
- **System Metrics**: Performance monitoring and resource usage tracking

### Core Services
- **Bruteforce Engine**: Orchestrates operations across different methods
- **Worker Manager**: Manages multi-threaded execution with CPU optimization
- **Repository Integration**: Handles external tool execution and management
- **WebSocket Manager**: Real-time communication between client and server

### Dashboard Components
- **Control Panel**: Operation configuration and execution controls
- **Metrics Dashboard**: Real-time performance monitoring and system health
- **Results Panel**: Display and management of discovered keys/wallets
- **Safety Modal**: Emergency controls and system protection

## Data Flow

### Operation Lifecycle
1. User selects method and configures parameters in Control Panel
2. System creates operation record in database
3. Worker Manager spawns threads based on configuration
4. Repository Integration executes external tools
5. Results are validated and stored in database
6. Real-time updates sent via WebSocket to dashboard
7. Metrics collected and displayed continuously

### Real-time Updates
- WebSocket connection established on dashboard load
- Server broadcasts operation status changes
- Client updates UI without page refresh
- Metrics stream includes performance data and system health

## External Dependencies

### Frontend Dependencies
- React ecosystem (React, React DOM, React Hook Form)
- UI libraries (Radix UI components, Lucide icons)
- Utility libraries (date-fns, clsx, class-variance-authority)
- Development tools (Vite, PostCSS, Tailwind CSS)

### Backend Dependencies
- Express.js with WebSocket support
- Drizzle ORM with PostgreSQL adapter
- Worker thread management
- Process spawning for external tool execution

### External Tools
All external repositories are Python-based and require:
- Python runtime environment
- pip package management
- Repository-specific dependencies (requirements.txt)

## Deployment Strategy

### Development Environment
- Replit-based development with Node.js 20
- PostgreSQL 16 database provisioning
- Hot module replacement via Vite
- WebSocket development server on port 5000

### Production Build
- Vite builds optimized frontend bundle
- esbuild compiles server-side TypeScript
- Static assets served from Express
- Database migrations via Drizzle Kit

### Environment Configuration
- DATABASE_URL for PostgreSQL connection
- NODE_ENV for environment detection
- WebSocket configured for both development and production

## Changelog
- June 22, 2025. Initial setup

## User Preferences
Preferred communication style: Simple, everyday language.