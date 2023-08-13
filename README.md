# [Install Tailwind-CSS in VueJS3](https://tailwindcss.com)

**_*After Creating Your `Vue` Project*_**

## Install Using NPM

Install `tailwindcss` and its peer dependencies, then generate your `tailwind.config.js` and `postcss.config.js` files.

```bash
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p
```

---

## Configure your template paths

Add the paths to all of your template files in your `tailwind.config.js` file.

```js
/** @type {import('tailwindcss').Config} */
export default {
  content: ["./index.html", "./src/**/*.{vue,js,ts,jsx,tsx}"],
  theme: {
    extend: {},
  },
  plugins: [],
};
```

---

## Add the Tailwind directives to your CSS

Add the `@tailwind` directives for each of `Tailwind’s` layers to your `./src/style.css` file.

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

---

## Import style.css File in main.js File

```js
import { createApp } from "vue";
import App from "./App.vue";

/* Import tailwind style.css File */
import "./style.css";

createApp(App).mount("#app");
```

---

## Start your build process

Run your build process with `npm run dev`.

```bash
npm run dev
```

## Start using Tailwind in your project

Start using `Tailwind’s` utility classes to style your content.

```html
<template>
  <!-- Use Tailwind CSS -->
  <h1 class="text-3xl font-bold underline">Hello world!</h1>
</template>
```

[Browse Flowbite Site](https://tailwindcss.com/docs/guides/vite#vue)
