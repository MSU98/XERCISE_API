# XERCISE_API
Mobile application
This is the backend API for XERCISE application. This program provides frontend application with endpoints, services, dbcontext and supports Microsoft Entra ID authentication. You can use official XERCISE frontend for full functionality or build your own.

## Content

- Installation
- Prerequisites
- Technologies Used
- Roadmap

## Installation

<!-- How to install this application, including version-specific dependencies and the reasons for using older versions -->

In order to run the program with a local database:

1. Create a file called appsettings.local.json
2. Paste the following code inside of the appsettings.local.json file.

```json
{
  "Logging": {
    "LogLevel": {
      "Default": "Information",
      "Microsoft.AspNetCore": "Warning"
    }
  },
  "ConnectionStrings": {
    "DefaultConnection": "<Replace this with your own dbconnectionstring>"
  },
  "EntraId": {
    "Instance": "https://login.microsoftonline.com/",
    "TenantId": "",
    "ClientId": "",
    "Audience": "api://",
    "Authority": "https://login.microsoftonline.com/"
  }
}
```

Then run the application using your IDE or CLI:

```
dotnet run
```

### Dependency Notes

This project uses ASP.NET Core and requires a configured local or remote SQL Server database connection.

It also integrates with Microsoft Entra ID for authentication. The backend includes support for validation, authentication, database migrations, testing, and API documentation.

---

<!-- Packages and tools required to run the application -->

### Prerequisites

Before running this project, make sure you have the following installed and available:

- .NET 8
- A SQL Server instance (local or cloud)
- A configured Microsoft Entra ID (formely Azure AD) tenant

### Technologies Used

This project makes use of the following key libraries and tools:

- FluentValidation v11.11.0
- Microsoft.AspNetCore.Authentication.JwtBearer v8.0.0
- Microsoft.EntityFrameworkCore v9.0.4
- Microsoft.EntityFrameworkCore.Design v9.0.4
- Microsoft.EntityFrameworkCore.SqlServer v9.0.4
- Microsoft.EntityFrameworkCore.Tools v9.0.4
- Microsoft.Identity.Web v3.8.4
- Microsoft.NET.Test.Sdk v17.13.0
- Swashbuckle.AspNetCore v8.1.0
- xUnit v2.9.3
- xUnit.extensibility.core v2.9.3

## Roadmap

- ✅ Test project
- ✅ Services for workout, user, categories, intensities
- ✅ Validation
- ✅ DB Context with seeddata
- ✅ Minimal API endpoints for workout, user, categories, intensities
- ⬜ Service/endpoints for getting workout data
