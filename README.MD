# Ophelia E-Business Project

Ophelia is a small e-commerce project with a static frontend and an ASP.NET Core backend API. The project is organized so the UI, API, and database script are easy to find after extracting the ZIP once.

## Project Structure

```text
E-Bussiness/
├── frontend/
│   ├── index.html
│   ├── landing-page.html
│   ├── add-to-cart.html
│   ├── Product Description-page.html
│   ├── Success.html
│   ├── main.css
│   ├── bootstrap.css
│   ├── features.css
│   ├── main.js
│   ├── features.js
│   ├── config.js
│   └── Photos/
├── backend/
│   └── Ophelia.Api/
├── database.sql
├── DEPLOYMENT.md
└── README.md
```

## Requirements

- .NET SDK 10.0 or newer
- SQL Server or SQL Server Express
- A modern browser

## Backend Setup

1. Create the database using `database.sql`, or make sure SQL Server can create `OpheliaDb`.
2. Check the connection string in `backend/Ophelia.Api/appsettings.json`.
3. Run the API:

```powershell
cd backend/Ophelia.Api
dotnet restore
dotnet run
```

By default, the frontend expects the API at `http://localhost:5159/api`. If your backend runs on another URL, update `frontend/config.js`.

## Frontend Setup

Open `frontend/index.html` in a browser. It redirects to the landing page and keeps the frontend files in one clear location.

For a local static server, you can also run this from the project root:

```powershell
cd frontend
python -m http.server 8080
```

Then open `http://localhost:8080`.

## Notes

- Build folders such as `bin/`, `obj/`, `publish/`, and log files are intentionally excluded.
- Frontend files live only in `frontend/`.
- Backend source lives only in `backend/Ophelia.Api/`.
