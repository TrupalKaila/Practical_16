# Practical-16

This repository contains a simple ASP.NET Core Web API project created as part of Practical 16. It demonstrates the default Web API folder structure, environment-based configuration, routing, dependency injection, and built-in logging with a basic **Hello World** endpoint.

## Project Highlights

- **ASP.NET Core Web API** targeting **.NET 8**.
- **Swagger/OpenAPI** enabled in Development for interactive API exploration.
- **Hello World** endpoint that logs a message using the built-in logger.

## Project Structure

```
Practical_16/
├── Controllers/
│   └── HomeController.cs
├── Program.cs
├── Practical_16.csproj
├── appsettings.json
└── Properties/
```

## Getting Started

### Prerequisites

- [.NET 8 SDK](https://dotnet.microsoft.com/download)

### Run the API

From the repository root:

```bash
dotnet restore
dotnet run --project Practical_16/Practical_16.csproj
```

By default, the API listens on HTTPS and HTTP ports configured by ASP.NET Core.

### Swagger UI (Development Only)

When running in Development, Swagger UI is available at:

```
https://localhost:<port>/swagger
```

## API Endpoint

| Method | Route           | Description                              |
|--------|------------------|------------------------------------------|
| GET    | `/api/home`      | Returns `"Hello World"` and logs a message |

Example request:

```bash
curl https://localhost:<port>/api/home
```

## Logging

The `HomeController` uses ASP.NET Core's built-in `ILogger` to log when the Hello World endpoint is executed.

## Notes

- Environment-specific configuration can be added via `appsettings.Development.json`, `appsettings.Production.json`, etc.
- You can explore request pipeline components in `Program.cs`.
