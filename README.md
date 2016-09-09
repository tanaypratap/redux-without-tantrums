<img src="https://github.com/tanaypratap/redux-without-tantrums/blob/master/img-for-readme/redux.jpg" width="150" align="right">

Redux.. without tantrums
====================

Redux is a replacement to flux architecture. I find it very easy to learn and understand if you take out the bells and whistles of Babel, ES6, Webpack etc. I completely agree that we need to learn these tools but if you are unfamiliar with the ecosystem which comes with React + Redux this small tutorial is for you. 

The major concepts of redux can be learned from the [website](http://redux.js.org/) or from the [egghead videos from the creator himself](https://egghead.io/courses/getting-started-with-redux)


> This tutorial tries to breakdown each concept into individual branch
> and explain it to in plain javascript
> within one simple index.html file. 

### Create the empty app
##### branch: [master](https://github.com/tanaypratap/redux-without-tantrums/tree/master)
The basic app. Creates the skeleton of the app with importing libraries from CDN.
A basic TODO app (Yes! Another TODO app) to add items, remove items when clicked on the item. 

### Add Action
##### branch: [2_add_action](https://github.com/tanaypratap/redux-without-tantrums/tree/2_add_action)
Adds the first action. Action tells the store what to do and with what data to do that. This is the interface from app to store.

>Actions are payloads of information that send data from your application to your store. They are the only source of information for the store. You send them to the store using store.dispatch().

### Add Reducer
##### branch: [3_add_reducer](https://github.com/tanaypratap/redux-without-tantrums/tree/3_add_reducer)
Adds a reducer function. A reducer is a pure javascript function which changes the state based on the action and returns the new state.
>Actions describe the fact that something happened, but don't specify how the application's state changes in response. This is the job of a reducer.
Explanation to addition is in code comments.

### Create store
##### branch: [4_create_store](https://github.com/tanaypratap/redux-without-tantrums/tree/4_create_store)
Store is where you initialize everything and brings actions and reducers together. This section adds a new store. It adds the react (again, plain JS) component and subscribe it to store changes.

##### Store has some major functionality here:
 * Create a store using creatSstore() 
 * Get state of the store using getState() : This initializes the initial values and changes whenever the state changes
 * Subscribe to store change using subscribe() : This ensures that any changes to data is sent back to React application and hence the state for React is updated in turn updating the DOM.
 * Dispatch actions using dipatch(): This is used to call the reducers with data. Basically, to dispatch an action to the redex application.

### Some more functionalities
##### branch: [5_more_functionality](https://github.com/tanaypratap/redux-without-tantrums/tree/5_more_functionality)
To remove an item from the ToDo list click on that item. This one is an extension of the original program, no new concepts are introduced in this one. However, can be treated like a revision of sorts for the above 3 basic concepts.
* This adds another ACTION to remove a TODO item.
* A reducer for the action added 
* creates a dispatch on the UI and update React element to listen to onclick event.

### App Screenshot
It uses bootstrap for some styling. The final app after these five steps looks like below.

<img src="https://github.com/tanaypratap/redux-without-tantrums/blob/master/img-for-readme/screen-shot.JPG">


### Todos

 - Add async operations
 - Syntax improvement of React
 - Use dispatch and connect with React
 - Add Night Mode

License
----

MIT
