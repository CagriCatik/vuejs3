# Vue.js 3 Directives

Vue.js directives are special tokens in the markup that tell the library to do something with a DOM element. While Vue provides several built-in directives like `v-if`, `v-for`, and `v-bind`, it also allows developers to create custom directives, making Vue incredibly flexible for handling DOM manipulation and advanced UI behaviors.

In this tutorial, we’ll explore the most common directives and dive into building custom ones for real-world applications.

## What Are Vue Directives?

Directives are essentially special attributes in Vue.js that extend HTML’s functionality by binding data to the DOM in declarative ways. They are prefixed with `v-` to indicate Vue-specific functionality.

Here are some of the most common Vue directives:

- `v-bind`: Dynamically bind one or more attributes to an element.
- `v-model`: Two-way data binding for form inputs.
- `v-if`, `v-else`, `v-else-if`: Conditionally render elements.
- `v-show`: Show or hide an element based on the bound condition.
- `v-for`: Render elements based on data iteratively.
- `v-on`: Attach event listeners to DOM elements.
- `v-slot`: Expose slot properties and content.
- `v-pre`, `v-cloak`, `v-once`: These are advanced and provide specific rendering behaviors for performance.

## Common Built-In Vue Directives

### 1. `v-bind`: Binding Attributes Dynamically

The `v-bind` directive is used to dynamically bind an attribute to an element. It can be used with almost any HTML attribute.

```vue
<template>
  <img v-bind:src="imageUrl" alt="Dynamic Image" />
  <!-- Short syntax: -->
  <img :src="imageUrl" alt="Short Syntax" />
</template>

<script>
export default {
  data() {
    return {
      imageUrl: "https://example.com/my-image.jpg",
    };
  },
};
</script>
```

In this example, `v-bind:src` binds the image URL dynamically from the `data` object.

### 2. `v-model`: Two-Way Data Binding

The `v-model` directive simplifies two-way data binding, especially for forms.

```vue
<template>
  <input v-model="username" placeholder="Enter your username" />
  <p>Your username: {{ username }}</p>
</template>

<script>
export default {
  data() {
    return {
      username: "",
    };
  },
};
</script>
```

This makes the input field reactive, updating the value in the DOM and in the Vue instance’s data simultaneously.

### 3. `v-if`, `v-else`, `v-else-if`: Conditional Rendering

These directives conditionally render elements based on the evaluation of an expression.

```vue
<template>
  <p v-if="isLoggedIn">Welcome back!</p>
  <p v-else-if="hasAccount">Please log in</p>
  <p v-else>Create an account</p>
</template>

<script>
export default {
  data() {
    return {
      isLoggedIn: false,
      hasAccount: true,
    };
  },
};
</script>
```

In this example, Vue dynamically renders the appropriate message based on the `isLoggedIn` and `hasAccount` conditions.

### 4. `v-for`: List Rendering

The `v-for` directive is used to loop over data and render elements for each item in the array or object.

```vue
<template>
  <ul>
    <li v-for="(item, index) in items" :key="index">{{ item.name }}</li>
  </ul>
</template>

<script>
export default {
  data() {
    return {
      items: [
        { name: "Item 1" },
        { name: "Item 2" },
        { name: "Item 3" },
      ],
    };
  },
};
</script>
```

This efficiently renders a list of items from the `items` array.

### 5. `v-on`: Event Handling

The `v-on` directive is used to listen to DOM events.

```vue
<template>
  <button v-on:click="handleClick">Click me</button>
  <!-- Short syntax: -->
  <button @click="handleClick">Click me</button>
</template>

<script>
export default {
  methods: {
    handleClick() {
      alert("Button clicked!");
    },
  },
};
</script>
```

Here, the `v-on:click` directive attaches a click event listener to the button.

## Creating Custom Directives

Vue.js allows you to create custom directives that can encapsulate specific behavior. For example, let’s create a custom directive that automatically focuses an input element when it is rendered.

### Example: Custom Focus Directive

```vue
<template>
  <input v-focus placeholder="Focus on render" />
</template>

<script>
export default {
  directives: {
    focus: {
      mounted(el) {
        el.focus();
      },
    },
  },
};
</script>
```

In this example, the `v-focus` directive is applied to the input field, and it will focus automatically when the element is inserted into the DOM. The `mounted` hook of the directive gives access to the element, allowing us to call `el.focus()`.

### Directive Lifecycle Hooks

Just like Vue components, directives have lifecycle hooks:
- `beforeMount`: Called before the element is inserted into the DOM.
- `mounted`: Called when the directive’s element is inserted into the DOM.
- `beforeUpdate`: Called before the element’s data is updated.
- `updated`: Called after the data has been updated.
- `beforeUnmount`: Called before the directive is unbound from the element.
- `unmounted`: Called when the directive is removed from the DOM.

## Best Practices for Directives

1. **Use Built-In Directives When Possible**: Vue’s built-in directives cover most common cases, so prefer using them over custom directives unless necessary.
2. **Scope Custom Directives**: Ensure custom directives are scoped to prevent side effects.
3. **Avoid Overusing Directives**: Directives are powerful, but using them excessively can make the template hard to read. Prefer using methods or computed properties for complex logic.
4. **Naming**: Custom directives should have clear, descriptive names to indicate their purpose.
  
## Real-World Example: Input AutoFocus with Directive

```vue
<template>
  <div>
    <h1>Registration Form</h1>
    <input v-focus type="text" placeholder="Your Name" />
  </div>
</template>

<script>
export default {
  directives: {
    focus: {
      mounted(el) {
        el.focus();
      },
    },
  },
};
</script>
```

This simple directive can greatly enhance user experience by automatically focusing the input field when a form is rendered.

---

## Summary

Vue.js directives provide powerful ways to control and interact with the DOM. Built-in directives like `v-bind`, `v-for`, and `v-model` are essential for daily development, while custom directives can be used to encapsulate specific functionality in your applications. Understanding and mastering Vue directives is crucial for building clean, efficient, and maintainable code.

In the next tutorial, we will dive deeper into the **Vue Composition API** to further enhance your Vue.js applications. Stay tuned!
