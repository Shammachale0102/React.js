# React.js
## React Tutorial
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

## Styling React Using Sass

### What is Sass
Sass is a CSS pre-processor.

Sass files are executed on the server and sends CSS to the browser.

#### Can I use Sass?
If you use the create-react-app in your project, you can easily install and use Sass in your React projects.

Install Sass by running this command in your terminal:

npm i sass
Now you are ready to include Sass files in your project!

#### Create a Sass file
Create a Sass file the same way as you create CSS files, but Sass files have the file extension .scss

# React Hooks

Hooks were added to React in version 16.8.

Hooks allow function components to have access to state and other React features. Because of this, class components are generally no longer needed.

Although Hooks generally replace class components, there are no plans to remove classes from React.

### What is a Hook?
Hooks allow us to "hook" into React features such as state and lifecycle methods.

### Hook Rules
There are 3 rules for hooks:

Hooks can only be called inside React function components.
Hooks can only be called at the top level of a component.

### Custom Hooks
If you have stateful logic that needs to be reused in several components, you can build your own custom Hooks.


Hooks cannot be conditional

### React useState Hook
The React useState Hook allows us to track state in a function component.

State generally refers to data or properties that need to be tracking in an application.

#### Import useState
To use the useState Hook, we first need to import it into our component.

#### Initialize useState
We initialize our state by calling useState in our function component.

useState accepts an initial state and returns two values:

The current state.
A function that updates the state.

#### Update State
To update our state, we use our state updater function.

#### What Can State Hold
The useState Hook can be used to keep track of strings, numbers, booleans, arrays, objects, and any combination of these!

We could create multiple state Hooks to track individual values.

#### Updating Objects and Arrays in State
When state is updated, the entire state gets overwritten.

What if we only want to update the color of our car?

If we only called setCar({color: "blue"}), this would remove the brand, model, and year from our state.

We can use the JavaScript spread operator to help us.

## React useEffect Hooks

The useEffect Hook allows you to perform side effects in your components.

Some examples of side effects are: fetching data, directly updating the DOM, and timers.

useEffect accepts two arguments. The second argument is optional.

useEffect(<function>, <dependency>)

#### Effect Cleanup
Some effects require cleanup to reduce memory leaks.

Timeouts, subscriptions, event listeners, and other effects that are no longer needed should be disposed.

We do this by including a return function at the end of the useEffect Hook.

## React useContext Hook

React Context
React Context is a way to manage state globally.

It can be used together with the useState Hook to share state between deeply nested components more easily than with useState alone.

### The Problem
State should be held by the highest parent component in the stack that requires access to the state.

To illustrate, we have many nested components. The component at the top and bottom of the stack need access to the state.

To do this without Context, we will need to pass the state as "props" through each nested component. This is called "prop drilling".

##React useRef Hook

The useRef Hook allows you to persist values between renders.

It can be used to store a mutable value that does not cause a re-render when updated.

It can be used to access a DOM element directly.

#### Does Not Cause Re-renders
If we tried to count how many times our application renders using the useState Hook, we would be caught in an infinite loop since this Hook itself causes a re-render.

To avoid this, we can use the useRef Hook.
### Accessing DOM Elements
The useRef Hook is often used to access DOM elements directly.

First, we create a ref using the useRef Hook: const inputElement = useRef();.

Then, we attach the ref to a DOM element using the ref attribute in JSX: <input type="text" ref={inputElement} />.

Finally, we can access the DOM element using the current property: inputElement.current.

#### Tracking State Changes
The useRef Hook can also be used to keep track of previous state values.

This is because we are able to persist useRef values between renders.

## React useReducer Hook

The useReducer Hook is similar to the useState Hook.

It allows for custom state logic.

If you find yourself keeping track of multiple pieces of state that rely on complex logic, useReducer may be useful.

### Syntax
The useReducer Hook accepts three arguments.

useReducer(reducer, initialState, init)
The reducer function contains your custom state logic and the initialStatecan be a simple value, but generally will contain an object. The init argument is optional and is used to initialize the state.

The useReducer Hook returns the current stateand a dispatchmethod.

## React useCallback Hook
The useCallback Hook is used to memoize a callback function.

Memoizing a function means caching the result of a function so that it does not need to be recalculated.

The useCallback function only re-executes when one of its dependencies changes value.

This allows us to isolate resource intensive functions so that they will not automatically run on every render.

### Syntax
The useCallback Hook accepts two arguments.

useCallback(callback, dependencies)
callback: The function that you want to memoize.

dependencies: An array of dependencies for the callback function. The memoized callback will only change if one of these dependencies has changed.
Try running the example above and click the buttons.

You will notice that all three components (Parent, Button 1 and Button 2) re-render each time you click the buttons.

This can be avoided by using the useCallback hook.

By using the useCallback hook, we can memoize the functions and only recreate them when their dependencies change.

When clicking Button 1, only Parent and Button 1 should re-render, and when clicking Button 2, only Parent and Button 2 should re-render:

## React useMemo Hook

The React useMemo Hook returns a memoized value.

Think of memoization as caching a value so that it does not need to be recalculated.

The useMemo Hook only runs when one of its dependencies update.

This can improve performance.

The useMemo and useCallback Hooks are similar:

useMemo returns a memoized value.

useCallback returns a memoized function.

#### Without useMemo

The useMemo Hook can be used to keep expensive, resource intensive functions from needlessly running.

In this example, we have an expensive function that runs on every render.

When changing the count or adding a todo, you will notice a delay in execution.

### Use useMemo
To fix this performance issue, we can use the useMemo Hook to memoize the expensiveCalculation function. This will cause the function to only run when needed.

We can wrap the expensive function call with useMemo.

The useMemoHook accepts a second parameter to declare dependencies. The expensive function will only run when its dependencies have changed.

## React Custom Hooks
You can make your own Hooks!

When you have components that can be used by multiple components, we can extract that component into a custom Hook.

Custom Hooks start with "use". Example: useFetch.

### Build a Hook
First, let us make an example without a custom Hook.

In the following code, we are fetching data from a URL and displaying it.

We will use the JSONPlaceholder service to fetch some fake data.

To learn more about fetching data, check out the JavaScript Fetch API section.

### Example Explained
We have created a new file called useFetch.js containing a function called useFetch which contains all of the logic needed to fetch our data.

We removed the hard-coded URL and replaced it with a url variable that can be passed to the custom Hook.

Lastly, we are returning our data from our Hook.

In main.jsx, we are importing our useFetch Hook and utilizing it like any other Hook. This is where we pass in the URL to fetch data from.

## React Online Compiler
### React.js Compiler (Editor)
Create your own website and React.js applications with a Node.js environment in W3Schools Spaces.

W3Schools Spaces is a website-building tool that enables you to create and share your own website, as well as develop and host your React.js applications within a Node.js environment.

You have full control over the website's appearance and functionality by editing the code directly in your web browser.

W3Schools Spaces is user-friendly and requires no setup, making it easy to use.

Get started with React.js by selecting the Node.js environment in Spaces.

The code editor is packed with features to help you achieve more:

Templates: Start from scratch or use a template
Cloud-based: no installations required. You only need your browser
Terminal & Log: debug and troubleshoot your code easily
File Navigator: switch between files inside the code editor
And much more!

###Learn Faster
Practice is key to mastering coding, and the best way to put your React.js knowledge into practice is by getting practical with code.

Use W3Schools Spaces to build, test and deploy code.

The code editor lets you write and practice different types of computer languages. It includes React.js, but you can use it for other languages too.
#### Share Your Website With The World
Host and publish your websites in no time with W3School Spaces.

W3Schools subdomain and SSL certificate are included for free with W3School Spaces. An SSL certificate makes your website safe and secure. It also helps people trust your website and makes it easier to find it online.

Want a custom domain for your website?

You can buy a domain or transfer an existing one and connect it to your space.

###Easy Package Management
Get an overview of your packages and easily add or delete frameworks and libraries. Then, with just one click, you can make changes to your packages without manual installation.

## React Syllabus

