# React + TypeScript + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react/README.md) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

## Expanding the ESLint configuration

If you are developing a production application, we recommend updating the configuration to enable type aware lint rules:

- Configure the top-level `parserOptions` property like this:

```js
   parserOptions: {
    ecmaVersion: 'latest',
    sourceType: 'module',
    project: ['./tsconfig.json', './tsconfig.node.json'],
    tsconfigRootDir: __dirname,
   },
```

- Replace `plugin:@typescript-eslint/recommended` to `plugin:@typescript-eslint/recommended-type-checked` or `plugin:@typescript-eslint/strict-type-checked`
- Optionally add `plugin:@typescript-eslint/stylistic-type-checked`
- Install [eslint-plugin-react](https://github.com/jsx-eslint/eslint-plugin-react) and add `plugin:react/recommended` & `plugin:react/jsx-runtime` to the `extends` list

Stucture
```
src/
├── assets/
│   ├── images/
│   └── styles/
├── containers/
│   ├── containter/
│   │   ├── Header.tsx
│   │   ├── Header.css
│   │   └── index.tsx
├── components/
│   ├── Header/
│   │   ├── Header.tsx
│   │   ├── Header.css
│   │   └── index.tsx
│   ├── Footer/
│   │   ├── Footer.tsx
│   │   ├── Footer.css
│   │   └── index.tsx
│   └── ...
├── modules/
│   ├── Home/
|   |   ├── action/
|   |   |   ├── index.ts  
|   |   ├── sagas/
|   |   |   ├── index.ts  
|   |   ├── reducer/
|   |   |   ├── index.ts
|   |   ├── selector/
|   |   |   ├── index.ts  
│   │   ├── Home.tsx
│   │   ├── Home.css
│   │   └── index.tsx
│   ├── About/
│   │   ├── About.tsx
│   │   ├── About.css
│   │   └── index.tsx
│   ├── Contact/
│   │   ├── Contact.tsx
│   │   ├── Contact.css
│   │   └── index.tsx
│   └── ...
├── services/
├── utils/
├── App.tsx
├── index.tsx
├── routes.tsx
├── store.ts
├── ...
```
CSS Methodology: BEM (Block Element Modifier)
What is BEM?
BEM (Block Element Modifier) is a naming convention for classes in HTML and CSS. It helps create reusable and maintainable styles by providing a clear structure and naming conventions.


Why BEM in Our Project
Explain why you've chosen to use BEM in this project. For example, mention its benefits for maintainability, readability, and scalability.

BEM Naming Convention
In this project, we adhere to the BEM naming convention to ensure consistency and clarity in our CSS code. Here's a quick overview of how BEM naming works:

Block: The main, standalone component that encapsulates an element. This corresponds to a React component in our project.
Element: A part of a block that has no meaning on its own. Elements are typically nested within blocks.
Modifier: A class that modifies the block or element, adding variations in appearance or behavior.
Example of BEM Naming
Here's an example of how we use BEM in our project:

```html
<div class="block">
    <div class="block__element"></div>
    <div class="block__element--modifier"></div>
</div>
```
block is the main component.
block__element is an element inside the block.
block__element--modifier is an element with a modifier applied.