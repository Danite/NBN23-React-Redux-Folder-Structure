# NBN23 Folder structure for React + Redux projects

*The best aproach to structuring React + Redux projects*


This folder structure is based on `grouped by feature`,
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

  The module contain the routes o views of your application.

  ```
  src/
  ├── app/
  │   ├── Home/
  │   ├── Following/
  │   ├── Components/
  │   └── App.jsx
  ```

## Containers

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

  Components directory contain components that recieve props from the parent.

  ```
  Home/
  ├── Components/
  │   ├── HomeButton.jsx
  │   └── index.js
  ```

## Common

  Common directory contain components that are shared throughout your app,
  such as buttons, modals, navbars...

## Utils

  Utils directory contain useful functions, services, constants.

## src/reducers.js

  Used to import all the reducers from all the modules and combine them into a root reducer using `combineReducers()`.

## src/index.js

  Used to create the Redux store using `createStore()` and connect the app to it using the `<Provider>` wrapping the component.
  All middleware needs to be imported and applied here.

## Storybook

 Storybook directory
  ```
  storybook/
  ├── stories/
  │   ├── Button/
  │   └── Cards/
  ```

**[⬆ back to top](#table-of-contents)**