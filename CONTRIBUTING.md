# Contributing to wolfXspotify-API

**Project:** wolfXspotify-API  
**Maintainer:** Silent Wolf · WOLF TECH  
**Live API:** [https://spotify.xwolf.space](https://spotify.xwolf.space)

Thank you for your interest in contributing! All contributions are welcome and appreciated.

---

## Getting Started

### Prerequisites
- Node.js 18 or higher
- npm 8 or higher
- Git

### Local Setup

```bash
git clone https://github.com/WOLFTECH-254/wolfXspotify-API.git
cd wolfXspotify-API
npm install
cp .env.example .env
npm run dev
```

The server will start on `http://localhost:5000` by default.

---

## How to Contribute

### Reporting Bugs

1. Check the [existing issues](https://github.com/WOLFTECH-254/wolfXspotify-API/issues) to avoid duplicates
2. Open a new issue with a clear title and description
3. Include steps to reproduce, expected vs actual behaviour, and your Node.js version

### Suggesting Features

Open a GitHub issue with the label `enhancement`. Describe the use case clearly.

### Submitting a Pull Request

1. Fork the repository
2. Create a new branch: `git checkout -b feat/your-feature-name`
3. Make your changes
4. Test thoroughly — hit the affected endpoints manually
5. Commit with a clear message: `git commit -m "feat: add /api/artist/:id/albums endpoint"`
6. Push to your fork: `git push origin feat/your-feature-name`
7. Open a Pull Request against `main`

---

## Code Style

- Use plain Node.js / Express — no TypeScript, no transpilation
- Follow the existing response format: always use `respond()` and `respondError()` from `src/response.js`
- All routes must include the `provider: "WOLF TECH"` and `creator: "Silent Wolf"` envelope via the response helpers
- Keep route files in `src/routes/`, one file per resource
- Add new routes to `src/index.js` and document them in `README.md`

---

## Environment Variables

See `.env.example` for the full list. The only required variable is `PORT` (defaults to `5000`). `GITHUB_TOKEN` and `GITHUB_REPO` are optional and only needed for GitHub token persistence.

---

## Scripts

| Command | Description |
|---------|-------------|
| `npm start` | Start the production server |
| `npm run dev` | Start with hot-reload (node --watch) |
| `npm run refresh` | Manually trigger a token refresh + GitHub commit |

---

## Contact

- **GitHub:** [@WOLFTECH-254](https://github.com/WOLFTECH-254)
- **Maintainer:** Silent Wolf · WOLF TECH
- **Location:** Kenya 🇰🇪

---

© 2026 WOLF TECH · Silent Wolf — All rights reserved.
