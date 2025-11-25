# React TypeScript Template

A modern React TypeScript template built with Vite, featuring:

- ⚡ **Vite** - Lightning fast build tool
- ⚛️ **React 19** - Latest React features
- 📘 **TypeScript** - Type-safe development
- 🧪 **Vitest** - Fast unit testing with React Testing Library
- 📝 **ESLint** - Code linting for TypeScript and React

## Getting Started

### Prerequisites

- Node.js 18+ 
- npm 9+

### Installation

```bash
npm install
```

### Development

Start the development server:

```bash
npm run dev
```

Open [http://localhost:5173](http://localhost:5173) to view it in the browser.

### Build

Build for production:

```bash
npm run build
```

The build artifacts will be stored in the `dist/` directory.

### Testing

Run tests:

```bash
npm run test      # Watch mode
npm run test:ci   # CI mode (single run)
```

### Linting

Run ESLint:

```bash
npm run lint
```

### Preview

Preview the production build locally:

```bash
npm run preview
```

## Project Structure

```
├── public/             # Static assets
├── src/
│   ├── assets/         # Application assets
│   ├── App.tsx         # Main application component
│   ├── App.test.tsx    # Component tests
│   ├── App.css         # Component styles
│   ├── main.tsx        # Application entry point
│   ├── index.css       # Global styles
│   └── setupTests.ts   # Test setup configuration
├── index.html          # HTML entry point
├── package.json        # Dependencies and scripts
├── tsconfig.json       # TypeScript configuration
├── vite.config.ts      # Vite configuration
└── eslint.config.js    # ESLint configuration
```

## Scripts

| Script | Description |
|--------|-------------|
| `npm run dev` | Start development server |
| `npm run build` | Build for production |
| `npm run preview` | Preview production build |
| `npm run test` | Run tests in watch mode |
| `npm run test:ci` | Run tests once (CI mode) |
| `npm run lint` | Lint code with ESLint |

## Plugins

This template uses [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react) which uses [Babel](https://babeljs.io/) for Fast Refresh.

## Expanding the ESLint Configuration

If you are developing a production application, we recommend updating the configuration to enable type-aware lint rules:

```js
export default defineConfig([
  globalIgnores(['dist']),
  {
    files: ['**/*.{ts,tsx}'],
    extends: [
      tseslint.configs.recommendedTypeChecked,
      // Or for stricter rules:
      // tseslint.configs.strictTypeChecked,
    ],
    languageOptions: {
      parserOptions: {
        project: ['./tsconfig.node.json', './tsconfig.app.json'],
        tsconfigRootDir: import.meta.dirname,
      },
    },
  },
])
```

## License

MIT
