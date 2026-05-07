# Deployment Notes

## Backend

1. Update `backend/Ophelia.Api/appsettings.json` with the production SQL Server connection string.
2. Restore and publish the API:

```powershell
cd backend/Ophelia.Api
dotnet restore
dotnet publish -c Release
```

3. Deploy the publish output to your hosting provider.

## Frontend

1. Update `frontend/config.js` so `apiBaseUrl` points to the deployed API URL.
2. Upload the contents of `frontend/` to any static hosting service.

Keep generated folders such as `bin/`, `obj/`, `publish/`, and log files out of the final ZIP and source control.
