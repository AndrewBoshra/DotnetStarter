# .NET Starter

An opinionated starting point for .NET 9 APIs — the scaffolding I'd otherwise rewrite at the start of every project.

## Stack

.NET 9 · Carter · MediatR · FluentValidation · EF Core 9 · MySQL · JWT bearer auth · Swagger

## What's included

- Vertical-slice layout — features own their endpoints, handlers, validators and DTOs
- MediatR pipeline with validation as a behaviour, so handlers stay free of guard clauses
- JWT authentication wired up, with an `Auth` feature as the worked example
- Centralised exception handling and consistent error responses
- EF Core configured with an initial auth migration
- Swagger in development

## Using it

```bash
dotnet restore
dotnet ef database update
dotnet run
```

Update the connection string and JWT settings in `appsettings.Development.json`, then add features under `Src/Features/` following the `Auth` slice.
