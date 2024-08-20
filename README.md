# dotnet-8-signup-verification-api

.NET 8.0.203 - Boilerplate API with Email Sign Up, Verification, Authentication & Forgot Password

# Last updated

- 20-08-2024

The Web API was made without the ASP.NET Core Identity using custom JWT middleware

# Functionality of the Web App

- JWT authentication with refresh tokens
- Refresh token rotation
- Revoked token reuse detection
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
- VS Code

# Updated EF Core tool to the latest version

dotnet tool update --global dotnet-ef

# Development

Create the Initial Migration for SQLite DB - should work for any DB

set ASPNETCORE_ENVIRONMENT=Development

dotnet ef migrations add InitialCreate --context DataContext --output-dir Migrations/SqliteMigrations

# Create the local SQLite DB

dotnet run

# Production

Create a self contained build for production at the remote server / traditionel web hotel

dotnet publish webapi.csproj --configuration Release --runtime win-x86 --self-contained

Upload the build to remote server ( without SQLite DB )

At my remote servers the web.config needs to be without the folowing:

hostingModel="inprocess"

# Create the remote SQLite DB

Now you can create the remote SQLite DB at the remote server by type the url:

remote-host.com/swagger

