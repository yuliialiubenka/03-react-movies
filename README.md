# Movie Search

Homework #2 of the React course: a movie search app powered by the
[TMDB](https://www.themoviedb.org/) API. Enter a keyword to find movies, click a poster to see
details in a modal window.

## Tech stack

Vite, React 19, TypeScript, axios, React Hot Toast, CSS Modules, modern-normalize, ESLint, Prettier.
Deployed to Vercel.

## Getting started

Requires Node.js 24 (LTS).

1. Install dependencies: `npm install`.
2. Copy `.env.example` to `.env` and put your TMDB **API Read Access Token** there:

    ```
    VITE_TMDB_TOKEN=your_tmdb_api_read_access_token
    ```

    `.env` is in `.gitignore` and must never be committed.

3. Start the dev server: `npm run dev` and open [http://localhost:5173](http://localhost:5173).

On Vercel, add `VITE_TMDB_TOKEN` in **Project Settings → Environment Variables** and redeploy.

## Scripts

| Command                | What it does                                 |
| ---------------------- | -------------------------------------------- |
| `npm run dev`          | Start the dev server                         |
| `npm run build`        | Check types and build the production version |
| `npm run preview`      | Serve the built `dist/` locally              |
| `npm run lint`         | Check code with ESLint                       |
| `npm run format`       | Format all files with Prettier               |
| `npm run format:check` | Check formatting without changing files      |

## Project structure

```
src/
    main.tsx
    index.css
    types/
        movie.ts                Movie interface
    services/
        movieService.ts         fetchMovies: TMDB search request via axios
    components/
        App/                    state: movies, loading, error, selected movie
        SearchBar/              header with the search form (Form Actions)
        MovieGrid/              list of movie cards
        Loader/                 loading message
        ErrorMessage/           request error message
        MovieModal/             movie details in a portal modal
```

Each component folder has a `.tsx` file and a `.module.css` file with the same name.
