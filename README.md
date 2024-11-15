# Angular 17 JWT Authentication

A complete authentication system built with Angular 17 that implements JWT (JSON Web Token) authentication with role-based authorization.

## Features

- User registration and login
- JWT authentication
- Role-based access control (Admin, Moderator, User)
- Protected routes
- HTTP interceptor for handling auth tokens
- Session storage management
- Responsive UI with Bootstrap

## Prerequisites

- Node.js (v16 or higher)
- Angular CLI (v17.3.0 or higher)
- A compatible backend server running on `http://localhost:8080`

## Installation

1. Clone the repository
2. Install dependencies:

bash:
npm install
npm install bootstrap (not sure if this is needed)

## Run the backend server

1. Clone this repository: https://github.com/janpc01/mean-authentication-authorization
2. Run backend server from backend directory: node server.js

## Development Server

Run the development server:

bash:
ng serve --port 8081

Navigate to `http://localhost:8081/`. The application will automatically reload if you change any of the source files.

## Project Structure

- `src/app/_services/` - Authentication and user services
- `src/app/components/` - Feature components (login, register, profile, etc.)
- `src/_helpers/` - HTTP interceptor for handling auth tokens
- `src/app/board-*` - Role-specific components

## Key Components

### Authentication Service
The auth service handles all authentication-related operations:

typescript:src/app/services/auth.service.ts
startLine: 18
endLine: 35

### Storage Service
Manages user session data:

typescript:src/app/services/storage.service.ts
startLine: 12
endLine: 35

## Available Routes

- `/home` - Home page
- `/login` - Login page
- `/register` - Registration page
- `/profile` - User profile
- `/user` - User board (authenticated users only)
- `/mod` - Moderator board (moderators only)
- `/admin` - Admin board (administrators only)

## Security Features

- HTTP-only cookies for token storage
- Cross-Origin Resource Sharing (CORS) support
- Protected routes with role-based guards
- Session management
- Secure password handling

## Building for Production

Build the project for production:

bash:
ng build


The build artifacts will be stored in the `dist/` directory.

## Running Tests

Execute unit tests:

bash:
ng test
