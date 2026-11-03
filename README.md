# MealMate

MealMate is a responsive recipe browser built with React and Vite. Discover recipes from [TheMealDB](https://www.themealdb.com/), keep track of favorites, and turn recipe ingredients into a practical shopping list.

## What you can do

- Discover featured recipes and browse by category.
- Search for recipes by name or ingredient.
- Open recipe details, including ingredients and cooking instructions.
- Rate recipes and save personal notes.
- Bookmark recipes and revisit recently viewed meals.
- Add ingredients to a shopping list, track purchased items, undo individual removals, and copy the list.
- Ask the built-in recipe assistant to search, suggest ideas from current results, or answer questions about an open recipe.
- Choose a light or dark theme; your theme and personal recipe data persist in your browser.

## Get started

You’ll need Node.js and npm installed.

```sh
git clone https://github.com/ashvaniix/MealMate.git
cd MealMate
npm install
npm run dev
```

Open the local URL printed by Vite in your terminal.

## Configuration

MealMate uses TheMealDB API. By default, it uses the public development key `1`, so no configuration is needed to get started.

To use another API key, copy `.env.example` to `.env.local` and set the key:

```env
VITE_MEALDB_KEY=your_api_key
```

Restart the Vite development server after changing environment variables. Do not commit `.env.local`.

## Development commands

| Command | Description |
| --- | --- |
| `npm run dev` | Start the Vite development server |
| `npm run build` | Create a production build in `dist/` |
| `npm run preview` | Preview the production build locally |
| `npm run lint` | Run Oxlint |
| `npm test` | Run the Vitest test suite |
| `npm run package:source` | Create `MealMate-source.zip` |

The source archive excludes `node_modules`, `dist`, `.git`, `.env.local`, and the archive itself.

## Data and privacy

Recipe searches and details are retrieved from TheMealDB. Bookmarks, ratings, notes, shopping list items, search history, and theme preference are stored in the browser’s `localStorage`; MealMate does not require an account or app backend. Clearing this site’s browser data removes the locally saved information.

## Project structure

```text
src/
  app/          Application shell, providers, and error boundary
  components/   UI grouped by feature (search, recipes, shopping, and more)
  context/      Shared application contexts
  data/         TheMealDB client and recipe/search helpers
  hooks/        State, browser storage, and application behavior
```

## Tech stack

- React 19
- Vite
- Tailwind CSS 4
- Vitest and Testing Library
- TheMealDB API
