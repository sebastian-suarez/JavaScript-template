# JavaScript Template

A minimal Node.js starter that uses ECMAScript modules, path aliases, linting, and formatting so you can begin new experiments quickly without rebuilding the same setup.

## Features

- Node.js ESM configuration with `"type": "module"` for modern import/export syntax.
- Path aliasing via `package.json#imports` so files inside `src` can import using `#root/...`.
- Preconfigured formatting with Prettier and linting with XO, plus a placeholder AVA test command.
- Simple example module (`greet.js`) and entry point (`src/index.js`) to verify the tooling.

## Getting Started

### Prerequisites

- Node.js `>=18`
- npm (bundled with Node.js)

### Installation

```bash
npm install
```

## Available Scripts

- `npm start` – Runs the example application (`node src`) and prints a greeting.
- `npm test` – Executes the lint and test pipeline (`xo && ava`).
- `npx xo` – Lints the project using XO (already invoked by `npm test`).
- `npx prettier --write .` – Formats the codebase using Prettier.

## Project Structure

```
src/
  index.js          # Entry point that imports using the #root alias
  modules/
    greet.js        # Sample module demonstrating modular structure
```

### Import Alias

The alias defined in `package.json` lets you write imports such as:

```js
import greet from "#root/modules/greet.js";
```

Adjust the mapping in `package.json#imports` if you reorganize the `src` directory.

## Development Workflow

1. Implement changes in `src/`.
2. Run `npm start` to verify runtime behavior.
3. Run `npm test` (or `npx xo`) to catch lint issues; add AVA tests as your project grows.
4. Use Prettier for consistent formatting before committing.

## License

This project is released under the [MIT License](LICENSE).
