# Implementing a Multi-Page Application

## Overview:
In this assignment, you will be tasked with implementing a **Multi-Page Application (MPA)** using **Vue.js 3**. Unlike a Single-Page Application (SPA), each page will be loaded separately and rendered on the server. Your project should focus on building individual pages, integrating Vue.js for component-based rendering, and optimizing the user experience through Vue.js concepts such as **components**, **directives**, and **state management**.

---

# Project Requirements:

You are required to build a **Multi-Page Application** that includes the following key features:

## 1. **Project Setup**
- Set up your Vue.js project using **Vue CLI** or **Vite**.
- Each page should be a separate HTML file served from the backend (e.g., with a framework like Express.js or any static site generator).
- Integrate Vue.js on each page to manage UI components and interactions.
- Include at least 3 main pages:
  - **Home Page**
  - **Services Page**
  - **Contact Page**

---

## 2. **Components**
- Create reusable **Vue components** that are used across different pages of your application.
  - Example components: `Header.vue`, `Footer.vue`, `Button.vue`, etc.
- Use **props** and **emits** to manage data flow between components.
  
### Tasks:
1. Implement a **header** and **footer** component that is included on all pages.
2. Create a reusable **button component** for performing actions across multiple pages (e.g., submitting a form, navigating to another page).
3. Build a **modal component** for displaying additional information or prompts on the Services page.

---

## 3. **Vue Directives**
- Utilize Vue’s built-in directives like `v-if`, `v-for`, `v-model`, `v-bind`, and `v-on` across different pages.
- Implement at least one **custom directive**. For example:
  - A directive to highlight a section when it comes into view.
  - A directive that toggles an element's visibility based on a condition.

### Tasks:
1. Use **v-if** and **v-for** to conditionally render components and loop through data across different pages.
2. Implement a **custom directive** to enhance the user experience, such as animating a section or auto-scrolling to a specific part of the page.

---

## 4. **Form Handling and Validation**
- On the **Contact Page**, create a form for user inputs (e.g., name, email, and message).
- Use **v-model** for two-way binding of form inputs.
- Implement form validation to ensure all fields are filled out correctly (e.g., email format validation).
- Provide user feedback after form submission (e.g., success or error messages).

### Tasks:
1. Build a contact form using Vue.js components.
2. Implement **v-model** for form data binding.
3. Include **form validation** and provide feedback after submission.

---

## 5. **State Management (Optional)**
- If your application has global state requirements, manage the state using either **Vuex** or the **Composition API**.
- For example, use Vuex to track user preferences or form data across different pages.

### Tasks:
1. Use Vuex for centralized state management across pages (optional).
2. Alternatively, use the Composition API to handle shared state.

---

## 6. **Project Structure**
- Follow best practices for **organizing your project**. Ensure that your components, assets, and views are structured logically.
  
### Suggested Structure:

```
my-mpa-project/
├── public/
│   ├── index.html (Home page)
│   ├── services.html
│   ├── contact.html
├── src/
│   ├── assets/
│   │   ├── images/
│   │   └── styles/
│   ├── components/
│   │   ├── Header.vue
│   │   ├── Footer.vue
│   │   └── Button.vue
│   ├── views/
│   │   ├── Home.vue
│   │   ├── Services.vue
│   │   └── Contact.vue
│   ├── App.vue
│   └── main.js
├── package.json
└── README.md
```

---

## 7. **Performance Optimization**
- Optimize your MPA by improving the performance of each page. Use Vue.js optimization techniques such as:
  - Using the **v-once** directive to prevent unnecessary re-renders of static content.
  - Implementing **lazy loading** of large components or media on specific pages.

### Tasks:
1. Use **v-once** to prevent re-renders of static sections on your pages.
2. Use **lazy loading** to load heavy media or large components only when needed.

---

## 8. **Styling and Responsiveness**
- Ensure that your application is **fully responsive** and adapts to different screen sizes.
- Use **CSS** or a **pre-processor** (like SCSS) for styling.
- Consider using a **CSS framework** like Bootstrap or Tailwind CSS for faster development (optional).

### Tasks:
1. Ensure that all pages are responsive and mobile-friendly.
2. Implement consistent styling across all pages and components.

---

## 9. **Deployment (Optional)**
- Deploy your application using a platform like **Netlify**, **Vercel**, or **GitHub Pages**.
- Ensure the application is accessible and functional in a production environment.

### Tasks:
1. Deploy your application using the platform of your choice.
2. Share the URL to your live application.

---

# Submission:
- Submit a **GitHub repository** containing your project code.
- Ensure the repository includes a **README** file explaining how to set up and run the project, and a brief description of its features.
- (Optional) Share the **live URL** if the project is deployed.

# Evaluation Criteria:
- **Code Quality**: Clean, structured, and maintainable code.
- **Component Reusability**: Efficient use of Vue components across multiple pages.
- **Directives Usage**: Correct usage of built-in and custom directives.
- **Form Handling**: Proper form data binding, validation, and feedback.
- **Performance Optimization**: Efficient handling of static content and lazy loading of heavy elements.
- **Responsiveness**: The application should be fully responsive across different screen sizes.
