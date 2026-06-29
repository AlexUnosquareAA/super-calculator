# Super Calculator

## Project Overview
An Angular 19 educational calculator app with basic arithmetic operations (addition, subtraction, multiplication, division) and a dark/light theme toggle. Built for teaching purposes with intentional incomplete exercises for students to implement.

## Tech Stack
- **Framework:** Angular 19 (standalone components)
- **Language:** TypeScript 5.7
- **Testing:** Karma + Jasmine
- **Build tool:** Angular CLI 19.2.27
- **Node.js:** 18.x or 20.x (not compatible with Node 22+)

## How to Run

### Install dependencies
```bash
npm install
```

### Start development server
```bash
npm start
```
App runs at `http://localhost:4200`

### Run tests
```bash
npm test
```

## Project Structure
```
src/app/
├── app.component.ts       — Calculator logic (state + methods)
├── app.component.html     — Template (button grid + display)
├── app.component.css      — Styles (dark mode default, light mode overrides)
├── app.component.spec.ts  — Unit test suite (Karma + Jasmine)
└── app.config.ts          — Angular app configuration
```

## Exercises
Three methods in `app.component.ts` are intentionally left empty for students:

| Exercise | Method | Description |
|---|---|---|
| 1 | `pressToggleSign()` | Flip the sign of the displayed number (5 → -5) |
| 2 | `pressPercent()` | Divide displayed number by 100 (50 → 0.5) |
| 3 | `toggleTheme()` + CSS | Toggle between dark and light mode |

## Coding Conventions
- Standalone Angular components (no NgModules)
- Component state managed via class properties (`display`, `firstOperand`, `operator`, `waitingForSecondOperand`, `isLightMode`)
- Floating-point precision handled with `.toPrecision(10)`
- Tests use `fixture.detectChanges()` after every state change before asserting on the DOM
