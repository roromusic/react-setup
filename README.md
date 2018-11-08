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

---

## 3. Parcel

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
