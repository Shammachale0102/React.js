# React.js

# React Introduction:

What is React?
React is a front-end JavaScript library.

React was developed by the Facebook Software Engineer Jordan Walke.

React is also known as React.js or ReactJS.

React is a tool for building UI components.


 ## How does React Work?



React creates a VIRTUAL DOM in memory.

Instead of manipulating the browser's DOM directly, React creates a virtual DOM in memory, where it does all the necessary manipulating, before making the changes in the browser DOM.

React only changes what needs to be changed!

## React ES6

What is ES6?
ES6 stands for ECMAScript 6.

ECMAScript was created to standardize JavaScript, and ES6 is the 6th version of ECMAScript, it was published in 2015, and is also known as ECMAScript 2015.

## React Render HTML

React's goal is in many ways to render HTML in a web page.

React renders HTML to the web page by using a function called createRoot() and its method render().
### The createRoot Function
The createRoot() function takes one argument, an HTML element.

The purpose of the function is to define the HTML element where a React component should be displayed.

### The render Method
The render() method is then called to define the React component that should be rendered.

But render where?

There is another folder in the root directory of your React project, named "public". In this folder, there is an index.html file.

You'll notice a single <div> in the body of this file. This is where our React application will be rendered.

 ## React JSX

  ### What is JSX?
 
JSX stands for JavaScript XML.

JSX allows us to write HTML in React.

JSX makes it easier to write and add HTML in React.

 ### Coding JSX
JSX allows us to write HTML elements in JavaScript and place them in the DOM without any createElement()  and/or appendChild() methods.

JSX converts HTML tags into react elements.

You are not required to use JSX, but JSX makes it easier to write React applications.

 ## React Components
Components are like functions that return HTML elements.

### React Components
Components are independent and reusable bits of code. They serve the same purpose as JavaScript functions, but work in isolation and return HTML.

Components come in two types, Class components and Function components, in this tutorial we will concentrate on Function components.

In older React code bases, you may find Class components primarily used. It is now suggested to use Function components along with Hooks, which were added in React 16.8. There is an optional section on Class components for your reference.

 ### Create Your First Component
When creating a React component, the component's name MUST start with an upper case letter.

 ### Class Component
A class component must include the extends React.Component statement. This statement creates an inheritance to React.Component, and gives your component access to React.Component's functions.

The component also requires a render() method, this method returns HTML.

## React Class Components
Before React 16.8, Class components were the only way to track state and lifecycle on a React component. Function components were considered "state-less".

With the addition of Hooks, Function components are now almost equivalent to Class components. The differences are so minor that you will probably never need to use a Class component in React.

Even though Function components are preferred, there are no current plans on removing Class components from React.

## React Props
Props are arguments passed into React components.

Props are passed to components via HTML attributes.

props stands for properties.

### React Props
React Props are like function arguments in JavaScript and attributes in HTML.

To send props into a component, use the same syntax as HTML attributes:

 ## React Events

 Just like HTML DOM events, React can perform actions based on user events.

React has the same events as HTML: click, change, mouseover etc.

 ### Adding Events
React events are written in camelCase syntax:

onClick instead of onclick.

React event handlers are written inside curly braces:

onClick={shoot}  instead of onclick="shoot()".

 ## React Conditional Rendering

 In React, you can conditionally render components.

There are several ways to do this.

if Statement
We can use the if JavaScript operator to decide which component to render.

## React Lists

In React, you will render lists with some type of loop.

The JavaScript map() array method is generally the preferred method.

If you need a refresher on the map() method, check out the ES6 section.

 ## React Forms

 Just like in HTML, React uses forms to allow users to interact with the web page.

### Handling Forms
Handling forms is about how you handle the data when it changes value or gets submitted.

In HTML, form data is usually handled by the DOM.

In React, form data is usually handled by the components.

When the data is handled by the components, all the data is stored in the component state.

You can control changes by adding event handlers in the onChange attribute.

We can use the useState Hook to keep track of each inputs value and provide a "single source of truth" for the entire application.

### Submitting Forms
You can control the submit action by adding an event handler in the onSubmit attribute for the <form>:

### Multiple Input Fields
You can control the values of more than one input field by adding a name attribute to each element.

We will initialize our state with an empty object.

To access the fields in the event handler use the event.target.name and event.target.value syntax.

To update the state, use square brackets [bracket notation] around the property name.

 ## React Router
 Create React App doesn't include page routing.

React Router is the most popular solution.

Add React Router
To add React Router in your application, run this in the terminal from the root directory of the application:

npm i -D react-router-dom

### Folder Structure
To create an application with multiple page routes, let's first start with the file structure.

Within the src folder, we'll create a folder named pages with several files:
src\pages\:

Layout.js
Home.js
Blogs.js
Contact.js
NoPage.js

Each file will contain a very basic React component.

#### Basic Usage
Now we will use our Router in our index.js file.

#### Example Explained
We wrap our content first with <BrowserRouter>.

Then we define our <Routes>. An application can have multiple <Routes>. Our basic example only uses one.

<Route>s can be nested. The first <Route> has a path of / and renders the Layout component.

The nested <Route>s inherit and add to the parent route. So the blogs path is combined with the parent and becomes /blogs.

The Home component route does not have a path but has an index attribute. That specifies this route as the default route for the parent route, which is /.

Setting the path to * will act as a catch-all for any undefined URLs. This is great for a 404 error page.

#### Pages / Components
The Layout component has <Outlet> and <Link> elements.

The <Outlet> renders the current route selected.

<Link> is used to set the URL and keep track of browsing history.

Anytime we link to an internal path, we will use <Link> instead of <a href="">.

The "layout route" is a shared component that inserts common content on all pages, such as a navigation menu.

## React Memo

Using memo will cause React to skip rendering a component if its props have not changed.

This can improve performance.

## Styling React Using CSS
There are many ways to style React with CSS, this tutorial will take a closer look at three common ways:

Inline styling
CSS stylesheets
CSS Modules

### Inline Styling
To style an element with the inline style attribute, the value must be a JavaScript object:

### camelCased Property Names
Since the inline CSS is written in a JavaScript object, properties with hyphen separators, like background-color, must be written with camel case syntax:

### JavaScript Object
You can also create an object with styling information, and refer to it in the style attribute:

### CSS Stylesheet
You can write your CSS styling in a separate file, just save the file with the .css file extension, and import it in your application.

### CSS Modules
Another way of adding styles to your application is to use CSS Modules.

CSS Modules are convenient for components that are placed in separate files.




