       Setting Up the Router
The first component we'll explore is BrowserRouter, which is a context provider allowing all the features of our React-Router to be available to its children. To make our code more semantic, we'll rename BrowserRouter as Router.
We want all of our application to have the router features, so we'll wrap the App component in index.js with the <Router> component.
index.js

    Components versus Pages
A common convention is to create two folders, components and pages. Any component that is used as a piece of UI goes in the components folder, any component meant to act as a "page" of the website goes in pages.
To accomplish this for our example project, we:
Create a components and pages folder.
Create a Main.js, Currencies.js, and Price.js file in the pages folder.
Create the component boilerplate in each component.
Main.js



         Creating Our Routes
 import the Route & Routes component into App. This will allow us define which of our components should render depending on the URL. We'll also import our pages for our routes.
App.js




The Currencies Component
In this component we will be doing the following:
Creating an array of the currencies our app can find prices for.
Looping over that array to generate a link for each one to the Price route.
Placing the currency symbol in the :symbol part of the URL.
Currencies.js


The Price Component
Store the API key and currency symbol in different variables.
Use the useEffect hook to make an API call.
Interpolate the apikey and symbol in the fetch URL.
Save the resulting data in state and render it.
Include a loaded and loading function for rendering the data if exists.
Price.js