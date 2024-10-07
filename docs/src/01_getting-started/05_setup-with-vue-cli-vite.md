# Setup with Vue CLI and Vite

When starting a Vue.js project, two primary tools are widely used for setting up your development environment: **Vue CLI** and **Vite**. Both offer fast, modern development workflows, but they differ in their underlying architecture and the way they handle project builds.

In this section, we will explore how to set up a Vue.js 3 project using both **Vue CLI** and **Vite**, highlighting the pros and cons of each, and guiding you through a practical setup process.

## What is Vue CLI?

**Vue CLI** (Command-Line Interface) is the official standard tooling for Vue.js. It offers a project scaffolding tool, complete with built-in features like development server, hot module replacement (HMR), and build optimization. Vue CLI is robust and highly configurable, making it great for enterprise-level applications.

### Key Features of Vue CLI:
1. **Project Templates**: Pre-configured project templates for quickly setting up a Vue project.
2. **Graphical User Interface (GUI)**: Provides a GUI for managing projects and configurations if you prefer not to use the command line.
3. **Built-in Vue Router and Vuex**: When generating a project, you can select Vue Router and Vuex to be automatically installed.
4. **Plugins Ecosystem**: The plugin-based architecture allows you to extend your project with tools like Babel, TypeScript, ESLint, and PWA support.
5. **Webpack-based**: Uses Webpack under the hood for bundling and building your project.

### Installing Vue CLI

First, you need to install the Vue CLI globally via npm (Node Package Manager):

```bash
npm install -g @vue/cli
```

After installation, you can create a new Vue project using the following command:

```bash
vue create my-vue-project
```

### Creating a Project with Vue CLI

Once you run the `vue create` command, Vue CLI will guide you through the project setup process. You’ll have two options:

1. **Default**: Pre-configured with Vue 3, Babel, and ESLint.
2. **Manually Select Features**: Allows you to customize your project with options like Vue Router, Vuex, TypeScript, Linter/Formatter, Unit Testing, E2E Testing, and more.

Example of a manual setup:

```bash
? Please pick a preset:
  Default ([Vue 3] babel, eslint)
❯ Manually select features
```

After choosing the features you need, Vue CLI will scaffold the project for you, and you’ll have a fully working Vue.js setup.

### Running the Project

Once your project is created, navigate into the project directory and start the development server:

```bash
cd my-vue-project
npm run serve
```

Vue CLI will spin up a local development server with hot module replacement (HMR) enabled. You can now access your application at `http://localhost:8080`.

### Pros and Cons of Vue CLI

**Pros**:
- **Mature and Feature-Rich**: Vue CLI is battle-tested and offers an extensive ecosystem of plugins and configuration options.
- **GUI Tool**: For developers who prefer a visual interface, Vue CLI offers a GUI to manage projects and configure plugins easily.
- **Great for Large Projects**: It is well-suited for large-scale applications that require more complex configurations (e.g., Vue Router, Vuex, TypeScript, etc.).

**Cons**:
- **Slower Builds**: Since Vue CLI is based on Webpack, build times can be slower compared to newer bundlers like Vite.
- **Overhead for Small Projects**: For small or simple projects, the extra features and configurations of Vue CLI can feel overwhelming.

---

## What is Vite?

**Vite** is a modern build tool developed by the creator of Vue.js, Evan You. It leverages native ES modules and modern browser APIs to provide incredibly fast development builds and a more efficient production build process. While it was initially created for Vue.js, Vite now supports multiple frontend frameworks.

### Key Features of Vite:
1. **Lightning-Fast Hot Module Replacement (HMR)**: Vite uses native ES modules, allowing near-instant updates during development.
2. **On-Demand Compilation**: Instead of bundling the entire app upfront, Vite compiles and serves modules on-demand, reducing load times during development.
3. **Optimized Production Builds**: Vite uses Rollup for bundling production builds, which results in smaller bundle sizes and faster performance.
4. **Framework-Agnostic**: Although Vite is the recommended tool for Vue.js 3, it also supports frameworks like React, Preact, Svelte, and more.
5. **Minimal Configuration**: Vite is opinionated and provides sensible defaults, reducing the need for extensive configuration files.

### Installing Vite

You can easily set up a Vue.js project using Vite by using npm or yarn. Here’s how:

```bash
npm init vite@latest my-vue-project
```

After this, you’ll be prompted to select a framework. Choose **Vue**:

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

Next, navigate to the project directory and install the dependencies:

```bash
cd my-vue-project
npm install
```

### Creating a Project with Vite

Vite uses a much simpler project setup compared to Vue CLI. By default, Vite includes only the essential dependencies required for a Vue 3 project. Additional tools like Vue Router or Vuex can be added later as needed.

### Running the Project

Once your project is created, you can run the development server with:

```bash
npm run dev
```

Vite will start a development server at `http://localhost:5173` with blazing-fast HMR. You’ll immediately notice the speed difference during development, especially with larger projects.

### Pros and Cons of Vite

**Pros**:
- **Super Fast**: Thanks to its on-demand compilation and native ES modules, Vite offers incredibly fast startup times and HMR during development.
- **Simplicity**: Vite’s minimal configuration and sensible defaults make it very easy to get started with.
- **Efficient Builds**: Vite uses Rollup for production builds, which generates highly optimized bundles.
- **Future-Proof**: Vite is built on modern technologies and is more aligned with the future of the web, such as ES modules and faster build systems.

**Cons**:
- **Less Mature**: Vite is a newer tool compared to Vue CLI and might have fewer plugins and community support, especially for niche use cases.
- **Not as Customizable**: While Vite’s simplicity is an advantage, it also means there’s less out-of-the-box customization compared to Vue CLI, particularly for complex, enterprise-level configurations.
- **Lacks Built-in Plugin Ecosystem**: Vite doesn't come with a plugin architecture as extensive as Vue CLI’s, so if you need heavy customization, you may have to do more manual configuration.

---

## Vue CLI vs Vite: Which One to Choose?

### When to Choose Vue CLI:
- **Enterprise Applications**: For large-scale or enterprise applications where you need more advanced configuration options, Vue CLI is more mature and feature-rich.
- **Legacy Projects**: If you have a legacy codebase built on Webpack or need to maintain compatibility with older configurations and tools, Vue CLI is the better choice.
- **More Plugins and Integrations**: If your project requires extensive use of plugins (e.g., TypeScript, Vuex, Vue Router, PWA support), Vue CLI’s plugin ecosystem is more comprehensive.

### When to Choose Vite:
- **Speed and Performance**: If development speed is your priority, especially for small to medium-sized applications, Vite’s fast build times and HMR make it an excellent choice.
- **Modern Projects**: If you’re starting a new project and want to leverage modern web technologies (like native ES modules), Vite’s minimal setup and fast development environment will help you get up and running quickly.
- **Smaller, Simpler Projects**: For smaller applications or simpler projects that don’t need heavy configurations, Vite’s simplicity and speed will boost your development process.

---

## Conclusion

Both **Vue CLI** and **Vite** offer powerful ways to set up and manage Vue.js 3 projects, but each has its strengths and trade-offs. **Vue CLI** is robust, feature-rich, and better suited for large projects requiring advanced configuration, while **Vite** offers lightning-fast development times and a modern, minimal setup ideal for small to medium-sized projects.

For most new projects, **Vite** is the recommended choice due to its performance and modern architecture. However, **Vue CLI** remains a solid choice for more complex applications that require extensive plugin support and configurability.
