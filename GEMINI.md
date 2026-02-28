# GEMINI.md - Mobile Project Context

This document provides essential context and instructions for AI agents working on the **mobile** project.

## Project Overview

- **Type:** Universal mobile application built with [Expo](https://expo.dev) (React Native).
- **Core Stack:**
  - **Framework:** [Expo](https://expo.dev) v55.0.4
  - **Runtime:** [React Native](https://reactnative.dev) v0.83.2
  - **Language:** [TypeScript](https://www.typescriptlang.org/)
  - **Routing:** [Expo Router](https://docs.expo.dev/router/introduction) (file-based routing)
  - **Styling:** [NativeWind](https://www.nativewind.dev/) (Tailwind CSS for React Native)
  - **Animation:** [React Native Reanimated](https://docs.swmansion.com/react-native-reanimated/)

## Directory Structure

- `src/app/`: File-based routing directory.
  - `_layout.tsx`: Root layout using `Stack` navigator.
  - `index.tsx`: Initial route.
  - `(tabs)/`: Tab-based navigation group.
- `assets/`: Images, icons, and font resources.
- `global.css`: Global Tailwind CSS styles.
- `app.json`: Expo configuration.
- `tailwind.config.js`: NativeWind/Tailwind configuration.

## Building and Running

### Development Commands

- `npm start`: Starts the Expo development server (Metro).
- `npm run ios`: Starts the app on an iOS simulator.
- `npm run android`: Starts the app on an Android emulator.
- `npm run web`: Starts the app in a web browser.
- `npm run lint`: Executes linting checks.

### Setup

1. Install dependencies: `npm install`
2. Start the development server: `npm start`

## Development Conventions

- **Styling:** Use NativeWind's `className` prop for styling components whenever possible. Avoid inline `style` objects unless necessary for dynamic values.
- **Routing:** Follow `expo-router` conventions for creating new screens and layouts in `src/app/`.
- **TypeScript:** Ensure all new files and components are strictly typed.
- **Components:** Prefer functional components with hooks.
- **Global Styles:** Add global CSS or Tailwind utilities to `global.css`.

## Architecture Insights

- The project uses a `src` directory to house application code.
- `expo-router` is configured with `typedRoutes` enabled for type-safe navigation.
- The `reactCompiler` is enabled in `app.json` for performance optimizations.
- NativeWind v4 is used, requiring `@tailwind` directives in `global.css` and import in the root `_layout.tsx`.
