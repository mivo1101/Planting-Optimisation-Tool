# Planting Optimisation Tool – Frontend

This folder contains the frontend for the Planting Optimisation Tool.  
It is a multi-page Vite + TypeScript application that provides:

- A **Home** page (Landing page)
- A **Recommendation** page
- A **Sapling Calculator** page
- A **Species** page

---

## Tech Stack

- **Build tool:** Vite 7 (multi-page setup)
- **Language:** TypeScript (no framework, vanilla TS)
- **Styling:** CSS (global styles in `src/style.css` and page‑specific CSS)
- **Testing / tooling:**
  - Vitest
  - ESLint, Stylelint
  - Prettier

---

## App Structure (High Level)

Key files:

- `index.html` – Home page
- `recommendations.html` – Recommendation page (To be updated)
- `calculator.html` – Sapling Calculator page (To be updated)
- `species.html` – Species page

Main TypeScript entry points:

- `src/home.ts` – Home page logic (navigation)
- `src/recommendations.ts` – Species recommendation logic (To be updated)
- `src/calculator.ts` – Sapling Calculator (To be updated)
- `src/species.ts` – Searching species information based on keywords

Vite is configured in `vite.config.ts` to treat these HTML files as separate entry points.

---

## How to Run the Frontend

From the project root:

```bash
cd Planting-Optimisation-Tool-master/frontend
npm install
npm run dev
```

---

## Useful NPM Scripts

From the `frontend` directory:

- `npm run dev` – start the Vite dev server
- `npm run build` – build the production bundle into `build/dist`
- `npm run test` / `npm run test:coverage` – run unit tests with Vitest
- `npm run lint:scripts` – lint TypeScript files with ESLint
- `npm run lint:styles` – lint CSS/SCSS with Stylelint
- `npm run format` – format scripts and styles with Prettier + Stylelint

---

## Contentful SDK for CMS of Species Information

This project uses [Contentful](https://www.contentful.com/) as a headless CMS to store and retrieve **Species Information**, including fields:

- Name
- Scientific Name
- Description
- Keywords
- Image

This enables easy keyword searching and displays the relevant species information cards in the Species page.

## Configuration

1.  Copy `.env.example` to a new file named `.env`.
    ```bash
    cp .env.example .env
    ```
2.  Fill in the `VITE_SPACE_ID` and `VITE_ACCESS_TOKEN` values in the `.env` file.
    _(Please ask the project lead or check the secure handover notes for these credentials)_.
