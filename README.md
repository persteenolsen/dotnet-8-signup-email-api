# dotnet-8-signup-verification-api

.NET 8.0.203 - Boilerplate API with Email Sign Up, Verification, Authentication & Forgot Password

# Functionality of the Web App

- JWT authentication with refresh tokens
- Email sign up and verification
- Forgot password and reset password functionality
- Role based authorization with two roles "User" and "Admin"
- CRUD Account management routes with role based access control
- Swagger API documentation with routes

# Tech used for creating the Web App

- A .NET 8.0.203 Web API
- An Angular 14 Web Client for the Frontend
- Entity Framework
- SQLite as a local DB
- Swagger for documentation
- A traditional Webhotel for hosting

# Updated EF Core tool to the latest version
dotnet tool update --global dotnet-ef

# Create the Initial Migration for SQLite DB ( should be ok for any DB )
dotnet ef migrations add InitialCreate --context DataContext --output-dir Migrations/SqlServerMigrations