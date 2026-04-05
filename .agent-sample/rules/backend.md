# Backend Rules

- Use service layer for all business logic
- Controllers must be thin
- Use DTO + validation (Zod)
- No direct DB access outside repository layer

## API Design

- RESTful
- Consistent error format
- Use async/await only