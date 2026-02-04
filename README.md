## SecureMyAir Operator Dashboard

### Description

SecureMyAir Operator is a React-based web dashboard for operators of the SecureMyAir platform.  
It provides an interface to:
- **Monitor and manage customers**
- **View and manage machines/devices**
- **Access operator tools** such as password reset and other utilities

The UI is built with **React 18** and **MUI (Material UI)**.

### Prerequisites

- **Node.js** (LTS version recommended, e.g. 18+)
- **npm** (comes with Node)

You can verify your versions with:

```bash
node -v
npm -v
```

### Environment variables

Create a `.env` file in the project root (copy from `.env.example` so you don’t commit secrets):

```bash
cp .env.example .env
```

Edit `.env` and set values as needed. Only variables starting with `REACT_APP_` are exposed to the app.

| Variable | Description |
|----------|-------------|
| `REACT_APP_API_URL` | Backend API base URL (e.g. `http://localhost:8000`). No trailing slash. |

The `.env` file is listed in `.gitignore` and should not be committed.

### Install dependencies

From the project root (`operator` folder), run:

```bash
npm install
```

This will install all dependencies listed in `package.json`.

### Run the app in development

```bash
npm start
```

- The app will start in **development mode**.
- Open `http://localhost:3000` in your browser.
- The page will reload automatically when you edit source files.

### Build for production

```bash
npm run build
```

This creates an optimized production build in the `build` folder, ready to be deployed to your hosting environment.

### Run tests (optional)

```bash
npm test
```

This launches the test runner in watch mode (if you add tests to the project).

### Project structure (high level)

- `src/App.js` – main app composition and routing.
- `src/pages/` – main pages like `DashboardPage.jsx` and `LoginPage.jsx`.
- `src/components/` – reusable UI components (e.g. `Customers.jsx`, `Machines.jsx`, `Layout.jsx`, reset password components).
- `src/context/` – React context providers for clients, machines, and protected routes.
- `public/` – static assets and HTML template.

You can customize behavior and UI by editing the files under `src/`.

