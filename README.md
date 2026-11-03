# Social Habit Tracker: Frontend

A web app where friends build habits together. Users track daily habits (reading, exercise, coding…), keep their streaks alive, see their squad's check-ins live, react to them and nudge friends who are slipping. Friends can also join challenges with optional money pledges (test mode only).

This repo is the **React + TypeScript frontend**. The API lives in [habit-tracker-backend](https://github.com/iamsamikshya-git/habit-tracker-backend).

> **Status:** 🚧 Sprint 0 (planning & design). Project setup starts in Sprint 1 (11 Nov 2026). Sections marked *(planned)* will be confirmed once the setup PR is merged.

AMPW Capstone Project · 28 Oct 2026 to 4 Jan 2027 · Student: Samikshya Adhikari · Supervisor: Prayusha Giri

## Features

- [ ] Sign up / log in with email + password
- [ ] Sign in with Google
- [ ] Create habits with flexible schedules; one-tap check-ins; streaks
- [ ] Private squads: live check-ins, reactions, nudges
- [ ] Challenges with optional pledges (eSewa / Stripe test mode)
- [ ] Points, levels & badges
- [ ] Public communities & leaderboards *(stretch)*
- [ ] Auto check-ins from GitHub / Strava *(stretch)*

## Tech stack

| Area | Tool |
|---|---|
| Framework | [React](https://react.dev) + [TypeScript](https://www.typescriptlang.org) |
| Build tool | [Vite](https://vitejs.dev) |
| Routing | React Router |
| Forms & validation | React Hook Form + Zod *(planned)* |
| HTTP | Axios *(planned)* |
| Google sign-in | `@react-oauth/google` *(planned)* |
| Icons | Lucide |
| Testing | [Vitest](https://vitest.dev) + React Testing Library |
| Linting / formatting | ESLint + Prettier |
| Docs | TSDoc comments |
| Design | Google Stitch, Figma |

## Prerequisites

- [Node.js](https://nodejs.org) **20 or newer** (check with `node -v`)
- npm (comes with Node)
- The [backend](https://github.com/iamsamikshya-git/habit-tracker-backend) running locally for API calls

## Getting started *(planned)*

```bash
# 1. Clone the repo
git clone https://github.com/iamsamikshya-git/habit-tracker-frontend.git
cd habit-tracker-frontend

# 2. Install dependencies
npm install

# 3. Create your environment file
cp .env.example .env        # Windows PowerShell: Copy-Item .env.example .env
#    then fill in the values (see below)

# 4. Start the dev server
npm run dev
```

The app runs at **http://localhost:5173**.

## Environment variables

Create a `.env` file in the project root. Never commit `.env`; only commit `.env.example`.

| Variable | Description | Example |
|---|---|---|
| `VITE_API_BASE_URL` | URL of the Django backend API | `http://localhost:8000/api` |
| `VITE_GOOGLE_CLIENT_ID` | OAuth Client ID from Google Cloud Console (must match the backend) | `1234-abc.apps.googleusercontent.com` |

> Variables must start with `VITE_` to be available in the browser. Don't put secrets here: everything in a Vite env file is visible to users.

## Scripts *(planned)*

| Command | What it does |
|---|---|
| `npm run dev` | Start the development server |
| `npm run build` | Type-check and build for production into `dist/` |
| `npm run preview` | Preview the production build |
| `npm run test` | Run Vitest tests once |
| `npm run test:watch` | Run tests in watch mode |
| `npm run coverage` | Run tests with a coverage report |
| `npm run lint` | Check code with ESLint |
| `npm run format` | Format code with Prettier |

## Testing

Every **form** and every **API call** has a Vitest test (project guideline).

```bash
npm run test
```

Tests live next to the code they test, e.g. `LoginForm.tsx` → `LoginForm.test.tsx`.

## Project structure *(planned)*

```
src/
├── api/          # Axios client + one file per API area (auth.ts, habits.ts…)
├── components/   # Reusable UI (Button, TextField, …)
├── features/     # Feature folders (auth, habits, squads, challenges…)
├── hooks/        # Custom hooks (useAuth…)
├── pages/        # Route pages (LoginPage, SignupPage, DashboardPage…)
├── routes/       # Router + protected routes
├── styles/       # Design tokens & global CSS
├── utils/        # Helpers
└── main.tsx
```

## Accessibility

We target **WCAG 2.1 AA**: colour contrast ≥ 4.5:1, full keyboard navigation, visible focus states, labelled form fields, alt text and clear error messages.

## Contributing / Git workflow

- Never commit directly to `main`.
- One issue → one branch → one pull request.
- Branch names: `<name>/<type>/<short-description>`, e.g. `samikshya/feat/login-page`
  (types: `feat`, `fix`, `docs`, `test`, `chore`, `refactor`, `design`)
- Commit messages: `feat: add login form validation`
- PR description must link the issue: `Closes #12`
- Tasks are tracked on the GitHub Projects board (Backlog → In Progress → Review → Done).

## Related

- Backend repo: https://github.com/iamsamikshya-git/habit-tracker-backend
- Design (Figma): *link coming soon*
- Project board: *link coming soon*
