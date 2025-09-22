# Overview

This is a full-stack web application for CSV data management and visualization. The system allows users to upload CSV files, parse and store the data in a PostgreSQL database, and provides an intuitive interface for viewing, searching, filtering, and managing the uploaded data. Built with a modern tech stack including React, Express, and Drizzle ORM, the application focuses on product data analysis with features like sorting, pagination, and column selection.

# User Preferences

Preferred communication style: Simple, everyday language.

# System Architecture

## Frontend Architecture
- **Framework**: React with TypeScript using Vite as the build tool
- **UI Library**: Shadcn/ui components built on Radix UI primitives with Tailwind CSS styling
- **State Management**: TanStack Query for server state management and caching
- **Routing**: Wouter for client-side routing (lightweight React Router alternative)
- **Styling**: Tailwind CSS with custom CSS variables for theming support
- **Component Structure**: Modular component architecture with reusable UI components, pages, and business logic components

## Backend Architecture
- **Server**: Express.js with TypeScript running in Node.js
- **API Design**: RESTful API endpoints for CSV upload and data retrieval
- **File Processing**: Multer for handling file uploads with CSV parsing using csv-parser library
- **Database Layer**: Drizzle ORM with PostgreSQL for type-safe database operations
- **Development**: Hot reload with Vite middleware integration for seamless development experience

## Database Schema
- **Users Table**: Basic user management with id, username, and password fields
- **CSV Uploads Table**: Tracks uploaded files with metadata (filename, original name, upload timestamp, record count)
- **CSV Records Table**: Stores parsed CSV data with structured fields for product information (URLs, prices, ratings, locations) plus raw data column for flexibility
- **Relationships**: Cascading deletes from uploads to records for data integrity

## Data Processing Pipeline
- **Upload Flow**: File upload → CSV parsing → database storage → client notification
- **Validation**: Zod schemas for runtime type validation on both client and server
- **Error Handling**: Comprehensive error handling with user-friendly toast notifications
- **Performance**: Pagination and search capabilities for handling large datasets efficiently

## Development Toolchain
- **Build System**: Vite with TypeScript compilation and ESM module support
- **Database Management**: Drizzle Kit for migrations and schema management
- **Code Quality**: TypeScript strict mode with comprehensive type checking
- **Development Server**: Express server with Vite middleware for hot reload during development

# External Dependencies

## Database
- **Neon Database**: Serverless PostgreSQL database with connection pooling
- **Connection**: Uses @neondatabase/serverless with WebSocket support for optimal performance

## UI Framework
- **Radix UI**: Headless UI components for accessibility and behavior
- **Shadcn/ui**: Pre-built component system with consistent design patterns
- **Tailwind CSS**: Utility-first CSS framework with custom design system

## Development Tools
- **Replit Integration**: Custom Vite plugins for Replit development environment
- **Hot Reload**: Vite development server with Express middleware integration
- **Error Handling**: Runtime error overlay for development debugging

## File Processing
- **Multer**: Express middleware for handling multipart/form-data file uploads
- **CSV Parser**: Stream-based CSV parsing for memory-efficient data processing

## State Management
- **TanStack Query**: Server state management with caching, background updates, and optimistic updates
- **React Hook Form**: Form state management with validation integration

## Build and Deployment
- **ESBuild**: Fast JavaScript bundler for production builds
- **Vite**: Development server and build tool with optimized asset handling
- **Node.js**: Server runtime with ES modules support