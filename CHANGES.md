# Changelog

## [v1.0.0] - 2025-07-22

### Added
- Created a `User` model with UUID-based user IDs.
- Added endpoint to **create a user**:  
  `POST /users`
- Added endpoint to **login with user ID**:  
  `POST /users/login`
- Added endpoint to **create a migration** associated with a user:  
  `POST /migrations`
- Added endpoint to **list all migrations**:  
  `GET /migrations`
- Added endpoint to **get a single migration by ID**:  
  `GET /migrations/<id>`
- Added endpoint to **delete a migration by ID**:  
  `DELETE /migrations/<id>`

### Improved
- Added proper UUID validation for user and migration IDs.
- Responses include structured JSON with meaningful messages for success/failure.
- User ID authentication included in migration creation to ensure only registered users can create migrations.

### Testing
- Added `curl` commands for:
  - Creating and logging in users
  - Creating and listing migrations
  - Viewing and deleting specific migrations
- Confirmed all endpoints function correctly with correct HTTP verbs and data.

---

## Upcoming Improvements
- Add token-based authentication for user sessions.
- Connect to a real database (currently using in-memory storage).
- Add support for migration status tracking and error handling.
- Add Swagger/OpenAPI documentation for the API.
