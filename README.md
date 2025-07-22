[v1.0.0] - 2025-07-22
Added
Created a User model with UUID-based user IDs.

Endpoint to create a user:
POST /users

Endpoint to login with user ID:
POST /users/login

Endpoint to create a migration associated with a user:
POST /migrations

Endpoint to list all migrations:
GET /migrations

Endpoint to get a single migration by ID:
GET /migrations/<MIGRATION_ID>

Endpoint to delete a migration by ID:
DELETE /migrations/<MIGRATION_ID>

Improved
Proper UUID validation for user and migration IDs.

Responses now return structured JSON with meaningful success/failure messages.

User ID authentication added during migration creation to ensure only registered users can initiate migrations.

Testing
Verified the following cURL commands:

Creating a user

Logging in with user ID

Creating a migration

Listing all migrations

Viewing a specific migration

Deleting a specific migration

Confirmed all endpoints function correctly using proper HTTP verbs and payloads.

Upcoming Improvements
Add token-based authentication for secure user sessions.

Connect the app to a persistent database (currently uses in-memory storage).

Implement support for migration status tracking and detailed error handling.

Add Swagger/OpenAPI documentation for easier API exploration.

