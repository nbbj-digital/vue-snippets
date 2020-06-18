<img src="https://cdn.auth0.com/blog/vuejs/vue-logo.png" alt="Vue.js" width="100"/>

# Vue Snippets

A collection of useful Vue.js snippets and patterns.

## Usage

Fork, download, or clone this repository and run locally to interact with the examples and read the code in parallel.
The snippets are best understood through local execution using [Vue Devtools](https://chrome.google.com/webstore/detail/vuejs-devtools/nhdogjmejiglipccpnnnanhbledajbpd?hl=en).
Running this application locally while browsing the components using the Vue Devtools extension will allow you to see
how the code snippets enact the changes in the DOM that are described below. Without Vue Devtools, you won't be able
to see how data is manipulated.

### Current Snippets

1. [CSS/SASS By Props](/src/components/CssByProps.vue)

- This example shows how we can influence the style of the component by passing props which directly edit the CSS/SASS
of the component itself.
- Example: You're creating a button component, and you want other developers on your project to be able to use it. However,
they are working on different pages in the application, and they need to be able to control the button's text color
and font styling.

2. [Custom V-Model](/src/components/CustomVModel.vue)

- How to create a custom component which naturally interfaces with the `v-model` paradigm of Vue.js, and allows us 
to pass information up to parent components from a child.
- Example: You're creating a text input component, and want to get data out of it so that the parent component which
is displaying the text input can do a computation using the input text.

3. [Manipulating Props](/src/components/ManipulatingProps.vue)
- How to manipulate data in a child component which is passed down from the parent component.
- Example: You're creating a component which has to display the most current data in the global store (Vuex), but your
component also has to change that data and (both) re-render the correct data, and save it in the global store.

3. [Deeply Nested Reactivity](/src/components/NestedReactivity.vue)
- How to properly and reactively update properties and objects in arrays 
- Example: You're fetching data with unknown or varying properties and need to update an existing object with that data,
or you need to reassign an object in an array with updated data.

## Development

### Added/Updated Configurations to Vue CLI Starter

1. [AirBnB Style Guide](https://github.com/airbnb/javascript)
2. [Prettier Style Guide](https://prettier.io/)
3. [Jest (Unit Testing)](https://jestjs.io/)
4. [ESLint (Style Enforcing)](https://eslint.org/)

### Commands

The following commands are used to develop the project:

1. `npm run build` - Build the package distribution bundle.
2. `npm run serve` - Start a development server with live-reloading on changes. (Used for previewing individual components.)
3. `npm run lint` - Lint code using ESLint and Vue, AirBnB, and Prettier configs.
4. `npm run test:unit` - Run unit tests for the individual components in the package.
