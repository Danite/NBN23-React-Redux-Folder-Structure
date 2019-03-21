# NBN23 Folder structure for React + Redux projects

*The best aproach to structuring React + Redux projects*


This folder structure is based on `grouping by feature` structure,
keeping your code maintainable as your application scales.

## Table of Contents

  1. [Folder Structure](#folder-structure)
  1. [Modules](#modules)
  1. [Containers](#containers)
  1. [Components](#components)
  1. [Common](#common)
  1. [Utils](#common)
  1. [src/reducers.js](#src/reducers.js)
  1. [src/index.js](#src/index.js)
  1. [Assets](#assets)
  1. [Storybook](#storybook)

## Folder Structure

  ```
  src/
  ├── app/
  │   ├── Home/
  │   │   ├── Components/
  │   │   │   ├── HomeButton.jsx
  │   │   │   └── index.js
  │   │   ├── Containers/
  │   │   │   ├── NavBar/
  │   │   │   │   ├── NavBar.jsx
  │   │   │   │   ├── NavBar.actions.js
  │   │   │   │   ├── constants.js
  │   │   │   │   ├── NavBar.reducer.js
  │   │   │   │   ├── NavBar.saga.js
  │   │   │   │   └── NavBar.spec.js
  │   │   │   ├── Footer/
  │   │   │   └── index.js
  │   │   ├── Home.jsx
  │   ├── Following/
  │   ├── Common/
  │   └── App.jsx
  ├── utils/
  ├── reducers.js
  ├── index.js
  assets/
  storybook/
  ├── stories/
  │   ├── Button/
  │   └── Cards/
  package.json
  ```

## Modules

  - The module directory contain the routes or views of your application.
  - Each route or view will have one directory.

  ```
  src/
  ├── app/
  │   ├── Home/
  │   ├── Following/
  │   ├── Common/
  │   └── App.jsx
  ```

## Containers
  
  Containers directory contain `Stateful Components` that provide data and behavior to
  `Stateless Components` or other container components.

  Containers:

  - Are concerned with how things work.
  - Call Redux actions and provide these as callbacks to the `Stateless Components`.
  - Are stateful, as they tend to serve as data sources.
  - Are usually generated using higher order components such as connect() from React Redux.

  ```
  Containers/
  ├── NavBar/
  │   ├── NavBar.jsx
  │   ├── NavBar.actions.js
  │   ├── constants.js
  │   ├── NavBar.reducer.js
  │   ├── NavBar.saga.js
  │   └── NavBar.spec.js
  ```

## Components or `Stateless Components`

  Components directory contain `Stateless Components` that receive data and callbacks exclusively via props
  from the parent.

  Stateless Components:

  - Are concerned with how things look.
  - Don't specify how the data is loaded or mutated.
  - Rarely have their own state (when they do, it's UI state rather than data).
  - Are written as functional components unless they need state, lifecycle hooks,
    or performance optimizations.

  ```
  Home/
  ├── Components/
  │   ├── HomeButton.jsx
  │   └── index.js
  ```

## Common

  - Common directory contain components that are shared throughout your app,
    such as buttons, modals, navbars...

## Utils

  - Utils directory contain useful functions, services and constants that are shared throughout your app.

## src/reducers.js

  - Used to import all the reducers from all the modules and combine them into a root reducer using `combineReducers()`.

## src/index.js

  - Used to create the Redux store using `createStore()` and connect the app to it using the `<Provider>` wrapping the component.
  - All middleware needs to be imported and applied here.

## Assets

  - Assets directory used to store non-source code items.
  - Images, video, or configuration.

## Storybook

  - Storybook directory contain UI components.
  - Easier and better development of UI components.
  - Easier testing.

  ```
  storybook/
  ├── stories/
  │   ├── Button/
  │   └── Cards/
  ```

**[⬆ back to top](#table-of-contents)**