# BulkUserUpdate3CX

A simple .NET console tool to **enable or disable two-factor authentication (2FA) for multiple 3CX users at once**.  
The list of users and configuration settings are managed via `appsettings.json`.

---

## Features
- Bulk update **2FA (Require2FA)** flag for selected 3CX users.
- Reads configuration (server, credentials, users) from `appsettings.json`.
- Authenticates against 3CX API using OAuth2 client credentials.
- Updates users via the `xapi/v1/Users` endpoint.

---

## Configuration

Create or edit the `appsettings.json` in the project root. **UsersToChange** is ID equal to fkidextenstion from database.

```json
{
  "3CXSettings": {
    "FQDN_3CX": "https://your-3cx-server",
    "ApiClientID_3CX": "your-client-id",
    "ApiToken_3CX": "your-client-secret",
    "Enable2FA3CX": true,
    "UsersToChange": "101,102,103"
  }
}
