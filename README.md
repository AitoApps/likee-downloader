# Create Nuxt 3 project
```bash
npx nuxi init likee-downloader
```

# Add Tailwind CSS 3
```bash
npm install --save-dev @nuxtjs/tailwindcss@5.0.0-4
```


# add this module to the buildModules section in nuxt.config.js
```bash
import { defineNuxtConfig } from 'nuxt3';

// https://v3.nuxtjs.org/docs/directory-structure/nuxt.config
export default defineNuxtConfig({
  buildModules: ['@nuxtjs/tailwindcss'],
});
```

# Create the Tailwind configuration file
```bash
npx tailwindcss init
```


# Add a basic CSS file at ./assets/css/tailwind.css
```bash
@tailwind base;
@tailwind components;
@tailwind utilities;

.theme-light {
  --background: #f8f8f8;
  --text: #313131;
}

.theme-dark {
  --background: #313131;
  --text: #f8f8f8;
}
```

# Define these colors in our tailwind.conf.js
```bash
module.exports = {
  content: [
    `components/**/*.{vue,js,ts}`,
    `layouts/**/*.vue`,
    `pages/**/*.vue`,
    `app.vue`,
    `plugins/**/*.{js,ts}`,
    `nuxt.config.{js,ts}`,
  ],
  theme: {
    extend: {
      colors: {
        themeBackground: 'var(--background)',
        themeText: 'var(--text)',
      },
    },
  },
  plugins: [],
};
```


