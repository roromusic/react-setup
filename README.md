# React Setup

## Introduction
A document outlining my recommended React setup and tooling

---

## Table of Contents

1. **[Prettier](#1-prettier)**
2. **[ESLint](#2-eslint)**
3. **[Parcel](#3-parcel)**
4. **[Reach Router](#4-reach-router)**
5. **[Babel](#5-babel)**
6. **[Jest](#6-jest)**
7. **[Emotion](#7-emotion)**
8. **[React Loadable](#8-react-loadable)**


---

## 1. Prettier

### Method 1: VSCode Extension
Add the prettier extension and add a `.prettierrc` file and put `{}` for the default configuration. 

In your workspace settings in VSCode you want the following settings:
```
"prettier.requireConfig": true,
"editor.formatOnSave": true
```
This setting says to only run prettier when you have a prettierrc file, and to format automatically when you save a file. 

### Method 2: Add Prettier CLI Script
`npm install -D prettier`

Add something like the following to your scripts object:
`"format": "prettier --write \"src/**/*.{js,jsx,css,json}\""`

To run prettier, run `npm run format`

---

## 2. ESLint

We want ESLint to handle style because Prettier is handling formatting. 
Install ESLint and config files/plugins:
`npm i -D eslint eslint-config-prettier eslint-plugin-prettier`

We also want ESLint to process JSX and React files, add linting rules around import/export, tell us best accessibility practices, 
Install:
`npm i -D babel-eslint eslint-plugin-import eslint-plugin-jsx-a11y eslint-plugin-react`

Add a `.eslintrc.json` file and add:
```
{
  "extends": [
    "eslint:recommended",
    "plugin:import/errors",
    "plugin:react/recommended",
    "plugin:jsx-a11y/recommended",
    "prettier",
    "prettier/react"
  ],
  "plugins": ["react", "import", "jsx-a11y"],
  "parserOptions": {
    "ecmaVersion": 2018,
    "sourceType": "module",
    "ecmaFeatures": {
      "jsx": true
    }
  },
  "env": {
    "es6": true,
    "browser": true,
    "node": true
  }
}
```

You can install the VSCode plugin to automatically check for you

### Add ESLint CLI Script
You can make it so that your build fails if it doesn't pass ESLint.

`"lint": "eslint **/*.{js,jsx} --quiet"`

---

## 3. Parcel
Parcel is fantastic because it is zero-config. Just tell it your index.html file and it does the rest. 

`npm install -D parcel-bundler`

In your npm scripts:
```
"dev": "parcel src/index.html"
```

..and that's it!
Out of the box, it can handle TypeScript, SASS, JSX, etc, and handles minification, gzip, and code splitting out of the box, and does the React transformations for you (via babel).

Running `npm run dev` will not only bundle your file, but will serve the build and comes with hot module replacement out of the box. 
It's also cool to note that Parcel will install packages for you. If you type `import React from 'react'`, it will automatically add it to your package.json file. 

---

## 4. Reach Router

---

## 5. Babel

---

## 6. Jest

---

## 7. Emotion

---

## 8. React Loadable
