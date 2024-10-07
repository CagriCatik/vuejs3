# Installation

Getting started with Vue.js 3 is simple and straightforward. Whether you’re building a small project or a large-scale application, Vue provides flexible ways to set up your environment. You can use either the **Vue CLI**, **Vite**, or include Vue directly via a CDN for quick prototypes.

In this section, we’ll cover multiple ways to install and set up Vue.js 3 depending on your project requirements.

---

## 1. Installing Vue.js via CDN (For Prototyping)

If you want to quickly prototype a Vue.js application without setting up a full development environment, you can include Vue.js via a CDN. This is the fastest way to get started with Vue without any tooling or build step.

### Example Setup Using Vue.js via CDN

You can create a basic HTML file and link to Vue.js directly through a CDN.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Vue.js 3 App</title>
  <script src="https://unpkg.com/vue@next"></script>
</head>
<body>
  <div id="app">
    {{ message }}
  </div>

  <script>
    const { createApp } = Vue;
    createApp({
      data() {
        return {
          message: 'Hello, Vue 3!'
        };
      }
    }).mount('#app');
  </script>
</body>
</html>
```

### Advantages of CDN Setup:
- **Quick Setup**: No need for a build tool, ideal for simple experiments and prototypes.
- **No Build Tools**: You can directly include Vue.js in a script tag and start building right away.

### Disadvantages:
- **No Build Optimization**: For production, this is not ideal because it doesn’t include advanced optimizations (minification, code splitting, etc.).
- **Limited Scalability**: This approach is not suitable for large, complex applications.

---

## 2. Installing Vue.js with Vue CLI (For Full-Scale Projects)

**Vue CLI** is a full-featured project scaffolding tool, offering built-in tools like Vue Router, Vuex, Babel, and more, to create and manage Vue.js applications. It’s a great option for developers building larger, production-ready applications.

### Prerequisites

Before installing Vue CLI, you need to have **Node.js** installed on your machine. You can download it from [Node.js official site](https://nodejs.org/).

### Step 1: Install Vue CLI

Install Vue CLI globally using npm or yarn:

```bash
npm install -g @vue/cli
# OR
yarn global add @vue/cli
```

You can verify the installation by running:

```bash
vue --version
```

This command should display the version of Vue CLI you have installed.

### Step 2: Create a New Vue.js Project

Once Vue CLI is installed, you can create a new project with the following command:

```bash
vue create my-vue-app
```

You’ll be prompted to either use the default setup or manually select features. You can choose the options depending on your needs (e.g., Vue Router, Vuex, TypeScript, etc.).

```bash
? Please pick a preset:
  Default ([Vue 3] babel, eslint)
❯ Manually select features
```

Vue CLI will then scaffold the project, set up necessary configurations, and install dependencies.

### Step 3: Run the Development Server

After the setup is complete, navigate into the project directory and run the development server:

```bash
cd my-vue-app
npm run serve
```

The local development server will start, and you can access your application at `http://localhost:8080`.

### Step 4: Build for Production

When you’re ready to deploy your project, use the following command to generate optimized production assets:

```bash
npm run build
```

This will create a `dist/` directory with minified and optimized files for production.

### Advantages of Vue CLI:
- **Feature-Rich**: Supports advanced configurations, Vue Router, Vuex, TypeScript, linting, testing, and more.
- **Plugins and GUI**: Easily add or remove features with Vue CLI’s plugin-based architecture, or use the GUI tool for visual management.
- **Great for Larger Projects**: Provides a well-structured environment for building large-scale applications.

---

## 3. Installing Vue.js with Vite (For Modern Development)

**Vite** is a modern build tool that offers faster startup times and more efficient hot module replacement (HMR) during development. It's a great choice for Vue.js 3 projects due to its speed and simplicity.

### Step 1: Create a New Vite Project

You can set up a new Vite project for Vue.js 3 by running the following command:

```bash
npm create vite@latest my-vue-app
```

You’ll be prompted to select a framework. Choose **Vue** or **Vue with TypeScript**, depending on your preference:

```bash
? Select a framework:
  vanilla
  vue
  vue-ts
  react
  preact
  lit
  svelte
  others
```

### Step 2: Install Dependencies

After generating the project structure, navigate to your project directory and install the necessary dependencies:

```bash
cd my-vue-app
npm install
```

### Step 3: Run the Development Server

Start the development server with:

```bash
npm run dev
```

Vite’s dev server runs on `http://localhost:5173` by default, with hot module replacement (HMR) providing instant feedback during development.

### Step 4: Build for Production

To build your Vite project for production, run:

```bash
npm run build
```

This will generate the optimized production files in the `dist/` folder using Rollup under the hood.

### Advantages of Vite:
- **Faster Builds**: Vite offers lightning-fast development builds and HMR compared to traditional bundlers.
- **Simplicity**: Vite is simpler to set up, with fewer configurations needed for most use cases.
- **Efficient for Modern Development**: Ideal for modern, smaller to medium-sized projects or for developers prioritizing fast build times.

---

## 4. Installing Vue.js with a Package Manager

If you’re building a project without using Vue CLI or Vite, you can manually add Vue.js to your existing project using a package manager like npm or yarn.

### Step 1: Initialize a Project

If you don’t already have a project, initialize one with npm:

```bash
mkdir my-vue-project
cd my-vue-project
npm init -y
```

### Step 2: Install Vue

Install Vue.js via npm or yarn:

```bash
npm install vue@next
# OR
yarn add vue@next
```

### Step 3: Set Up Vue in Your Project

You can now use Vue in your project by importing it into your JavaScript file and initializing it.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Vue Setup</title>
</head>
<body>
  <div id="app">{{ message }}</div>

  <script type="module">
    import { createApp } from 'vue';

    createApp({
      data() {
        return {
          message: 'Hello, Vue.js 3!'
        };
      }
    }).mount('#app');
  </script>
</body>
</html>
```

---

## Conclusion

Vue.js offers multiple ways to set up and start building your application depending on your project needs:

- **For Prototyping**: Using Vue.js via CDN is the quickest way to get started.
- **For Full-Scale Applications**: Vue CLI provides a robust and feature-rich environment for building large and complex applications.
- **For Modern Development**: Vite offers blazing-fast development and build times for modern projects, making it a popular choice for Vue 3 apps.
- **For Custom Setups**: You can manually install and configure Vue.js in any existing project using npm or yarn.

Each method has its own strengths, so choose the one that fits your development workflow and project needs.

In the next chapter, we’ll dive into **Vue.js 3 Composition API** and learn how it revolutionizes component development in Vue 3.