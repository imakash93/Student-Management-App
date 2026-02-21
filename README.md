# AngularAssignment

Angular assignment for student onboarding. This is a Student Management App for registering, listing, viewing, and editing student records.

## What This Repository Contains

This folder holds the **built output** of the app only. It does not include Angular source code or build configuration.

- `index.html` – Entry page
- JS bundles: `main.js`, `polyfills.js`, `runtime.js`, `vendor.js`, `styles.js`, `es2015-polyfills.js`
- `README.md`

There is no `src/`, `package.json`, or `angular.json` here. To develop or rebuild the app, you need the full Angular source project.

## How to Run the App

Serve this folder as static files, for example:

```bash
npx serve .
```

Or use any static HTTP server (e.g. `http-server`, or your IDE’s “Open with Live Server”) with the project root as the document root.

**Data:** The app expects these assets (create them if missing):

- `assets/students/students.json` – List of students
- `assets/students/docTypes.json` – Document types

Without them, student and document-type requests may fail or show empty data.

## Application Overview

- **Login** – Entry screen (default route)
- **Welcome** – Post-login landing
- **Register** – New student registration form
- **Students list** – List and filter students
- **View / Edit student** – View or edit a student by ID

**Main routes:** `login`, `welcome`, `register`, `studentslist`, `studentView/:id`, `students/:id`. Default and unknown routes redirect to `login`.

## Tech Stack

- Angular (legacy, fesm5-style build), Webpack
- `HttpClient` for data; no HTTP interceptors
- Angular Material Icons, Roboto font
- No NgRx; state is handled in components and services

## Project Structure (Build Output)

| File / folder   | Role                          |
|-----------------|-------------------------------|
| `index.html`    | Loads the app and script tags |
| `main.js`       | Application and routing code  |
| `polyfills.js`  | Browser compatibility         |
| `vendor.js`     | Third-party libraries         |
| `styles.js`     | Compiled styles               |
| `runtime.js`    | Webpack runtime               |

For development (editing code, running tests, rebuilding), use the full Angular project that contains `src/`, `package.json`, and `angular.json`.
