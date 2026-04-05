# Architecture

## Style
- Modular monolith (Nx workspace)

## Backend
- NestJS (layered architecture)
  - Controller → Service → Repository

## Frontend
- Angular (standalone + signals)
- Feature-based structure

## Data Flow
Client → API → Service → DB

## Rules
- No business logic in controllers
- DTO validation required