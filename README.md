# React Training
- React training at Eurofins, Bengaluru
- Nov 9, 2022

## Preview
We shall build a few of the features in this app. Please revisit this very page as the app will not show up when you refresh the browser.  
https://vw-angular.s3.ap-south-1.amazonaws.com/index.html

## Backend
The backend for the app is here  
https://workshops-server.herokuapp.com/

## Summary
- Before beginning React
    - UI library for building frontend apps
    - Free and open-source
    - Handles DOM manipulations efficiently
    - Generally used to build Single Page Applications (SPAs)
	- The Single Page Application (SPA) architecture
        - App includes a single web page (HTML page). The content changes based on the route.
        - All HTML, CSS, JS assets are fetched on first page load
        - Only data is fetched on need basis.
        - Advantages
            - Page navigation is faster
            - Less load on the server
        - Disadvantages
            - First page load is slow
	- Role of Webpack in SPA
        - Babel transpilation
            - ES2015+ features can be used without issues
            - Supports JSX
        - Bundling
            - Must for SPA. Reduces page load time.
        - Hot reloading
            - Faster development

- Introduction to components
	- Component-based architecture for front-end apps
        - A component is a small part of the UI. Example: A button, a dialog box
        - Features
            - Declarative
            - Reusable
            - Composable
	- Scaffolding a React application using boilerplate code (create-react-app)
    ```
    npx create-react-app project-name
    ```
	- Understanding the Project Structure and build process
    - Start the server
	```
    npm start
    ```

- JSX
    - Easy way to create "React element" (UI definition)
	- A HTML like-syntax (but is actually a non-standard extension to JavaScript) and hence succint
	- Features
        - Conditional expressions and hiding and showing elements conditionally
	    - Rendering an array of React elements
	        - Setting a key for efficient DOM re-rendering
	    - Styling React elements

- React Bootstrap
    - UI library that offers useful UI components
    - Create good-looking and functional UI with less effort

- Component Basics
	- Defining Components
	    - Function syntax
        - Class syntax
    - Which syntax to use?
        - We prefer function syntax in modern React
            - as capable as class components
            - simpler to set up use
            - most importantly, it is easy to share functionality between different components ("custom hooks")
	- Props
        - Taking input from outside the component using props
        - Used to customize an instance of a component
    - Composing components
        - JSX makes it easy to put together components to form larger components. This way we build the UI incrementally.

- State
	- Data the component maintains
    - Data that changes with time and affects the UI
        - Example: Page number in a list of search results, the results for the selected 	page etc. These change as the user interacts.
	– Managing state in function components
        - The useState hook
        - equivalent in class components - setState() method

- Hooks
    - A set of methods in React available only to function components
    - They provide capabilities to function components, which previously (before v16.8) only class components had.
    - They throw an error if used within a class component, or outside of a function component (i.e not during the rendering of a function)
    - They were introduced to simplify implementing components that share common functionality.

- Side-effects - Logic in a component apart from generating and returning the UI
    - Handling asynchronous operations during the lifetime of a component like fetching and displaying data from the backend
    - Managing side-effects
        - Function components: The useEffect hook
        - Class components: lifecycle methods (componentDidMount, componentDidUpdate etc.)

- Basics of event handling
    - A separate handler - receives event object as argument
    - Online handler - to pass custom arguments

- Parent-child upstream/downstream communication
    - Shared state is maintained in the common ancestor
    - State and callback functions are passed as required to children
    - Communication from child to parent component using callback function passed as prop

- Working with forms and validating inputs
    - Using react-hook-form for handling forms and validations

- Routing
    - Handle navigation between "pages" - changes UI according to the "address" (path)
	- React Router
        - Popular router library
        - v6
	- Using React router
        - BrowserRouter
            - Refreshes child (usually App) when path changes ("address")
        - Routes, Route
            - Used for conditionally rendering components based on path
        – Link
            - Render links that does not cause browser to reload pages
        - NavLink
            - Same as Link but highlights link if it matches page path ("address")
	    - Handling dynamic path params
            - Parts of the path used to match a component can be dynamic
                - /path/to/:dynamic/:part/in/the/route
            - useParams() helps extract the dynamic parts from within the matched component

- Deployment
	- Configuration management in a create-react-app application
	- Creating a production build
    ```
    npm run build
    ```
	- Deployment on Netlify

## Further exploration

## JavaScript
- [General reference](javascript.info)
- [You Don't Know JS, Book Series by Kyle Simpson](https://rileygelwicks.gitbooks.io/you-dont-know-js/)
- [The Event Loop and Asynchronous Operations](https://www.youtube.com/watch?v=8aGhZQkoFbQ)
- [Promises - good article explaining its workings](https://medium.com/javascript-scene/master-the-javascript-interview-what-is-a-promise-27fc71e77261)
- [Functions including how the function context ("this") works](https://www.youtube.com/watch?v=D61O7f4C2HA&t=279s)

### A learning roadmap for React
- [Reactiflux - Curated list of references created by experts](https://www.reactiflux.com/learning/)
- [This is a very extensive roadmap for further exploration. Too vast, but comprehensive - can be quite intimidating](https://github.com/adam-golab/react-developer-roadmap)

### Courses on React
- [List of courses on React](https://reactjs.org/community/courses.html)

### Libraries
- [React](https://reactjs.org/)
- [React - Community resources and Support - includes references to tools](https://reactjs.org/community/support.html)
- [Create React app](https://facebook.github.io/create-react-app/)
- [React router](https://reacttraining.com/react-router/web/guides/quick-start)
- [Redux](https://redux.js.org/)
- [React Redux](http://react-redux.js.org)
- [Redux Thunk](https://github.com/reduxjs/redux-thunk)
- [Redux Saga Introduction](https://redux-saga.js.org/docs/introduction/BeginnerTutorial.html)
- [Redux Thunk](https://github.com/reduxjs/redux-thunk)
- [Quick introduction to Mobx](https://mobx.js.org/getting-started.html)
- [Mobx](https://mobx.js.org/)
- [Redux vs Mobx](https://www.youtube.com/watch?v=76FRrbY18Bs)
- [Immutable JS](https://immutable-js.github.io/immutable-js/)
- [Webpack - Step-by-step guide](https://webpack.js.org/guides)
- [Resources on Webpack](https://github.com/webpack-contrib/awesome-webpack)
- [Jest](https://jestjs.io/en/)
- [Enzyme](https://airbnb.io/enzyme/)
- [List of CSS in JS libraries for React](https://github.com/FormidableLabs/radium/tree/905227c122b1775775cf8d82c508cce4179cff08/docs/comparison)
- [Axios Cheat Sheet](https://kapeli.com/cheat_sheets/Axios.docset/Contents/Resources/Documents/index)

### Redux
- [Dan Abramov's article on Presentational + Container components](https://medium.com/@dan_abramov/smart-and-dumb-components-7ca2f9a7c7d0)
- [Dan Abramov's free course on Redux (on Egghead) - Part 1](https://egghead.io/courses/getting-started-with-redux)
- [Dan Abramov's free course on Redux (on Egghead) - Part 2](https://egghead.io/courses/building-react-applications-with-idiomatic-redux)
- [Redux vs Context + useReducer](https://medium.com/javascript-scene/do-react-hooks-replace-redux-210bab340672)
