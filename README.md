# react-q
react assignment question 
Q1. What is React?
Ans ->React is a Single Page Application.React allows developers to create large web applications that can change data, without reloading the page.
The main purpose of React is to be fast, scalable, and simple.

Q2. Differentiate between Real DOM and Virtual DOM?
Ans ->
Real DOM :-
1-it is slower
 2- it can directly update the HTMl element
 3-DOM manipulation is very expensive..
 4- there is a lot of memeory Wastage..
 5-create a new DOM if element Updates

Virtual COM :-
 1- its is faster
 2- it can't be directly update the HTMl element..
 3-DOm manipulation is easy..
 4- no memory is wastage..
 5-Updates the JSX if element Updates..

Q3. List some of the major advantages of React.
Ans -> 
1-Increases the application’s performance with Virtual DOM
2-JSX makes code is easy to read and write
3-It renders both on client and server side
4--Easy to integrate with other frameworks (Angular, BackboneJS) since it is only a view library
5- Easy to write UI Test cases and integration with tools such as JEST.


Q4. What are the limitations of React?
Ans -> 
1- react is just the view. not a full scale framework.
2- library is quite large
3-difficult for the novice programmers to understands.
4-uses inline temlating and jsx.

Q5. Why can't browsers read JSX?
Ans -> 
Browsers can only read JavaScript objects but JSX in not a regular JavaScript object. Thus to enable a browser to read JSX,
first, we need to transform JSX file into a JavaScript object using JSX transformers like Babel and then pass it to the browser.

Q6.What are ES6 features added as compared to ES5?
Ans ->
ES5 supports primitive data types that are string, number, boolean, null, and undefined. In ES6, there are some additions to JavaScript data types.
It introduced a new primitive data type 'symbol' for supporting unique values. In ES5, we could only define the variables by using the var keyword.
 

Q7.  What is One-way Data Binding how that is achieved?
Ans -> Unidirectional data-flow means that data has one, and only one, way to be transferred to other parts of the application.


       import React, { Component } from 'react';
       class App extends Component {
        state = {
          input_value: '',
        };
        render() {
          return <input 
                  name="input_value" 
                  value={this.state.input_value} 
                  />;
        }
        }

Q8. What is a State in React?
Ans -> The state is a built-in React object that is used to contain data or information about the component.

Q9. Differentiate between stateless and stateful components.
Ans -> 
Stateless Cmponents:- 
1-In React, a stateful component is a component that holds some state.
2-class component
3- having state or life cycle method
4- powerfull or more complex using than functional component.
5- holds the some information

statefull Component:- 
1- functional component
2- they dont have state or life cycle method..
3- easy to read and write
4- it is arrow function


Q10. What is the significance of keys in React?
Ans -> 
Keys are used to React to identify which items in the list are changed, updated, or deleted.
In other words, we can say that keys are used to give an identity to the elements in the lists..


Q11. Explain the lifecycle methods of React components in detail?
Ans ->
1-componentDidMount()->>The componentDidMount() method is called after the component is rendered.
2-componentDidUpdate()==>> The componentDidUpdate method is called after the component is updated in the DOM.
3-componentWillUnmount()==>> The componentWillUnmount method is called when the component is about to be removed from the DOM.

phase-->

1-mount--> when component is created
2- update-->when component is updated with state or props..
3-unmount--> when componenet is removed.


Q12.  What are Pure Components?
Ans -> it is the features of the class component in the react and we need to import them into in class component.
it is avoid the re-rendering of the component means when the value of state and props has been updated with the same values.


Q13. Why is it necessary to start component names with a capital letter?
Ans -> 
In JSX, lower-case tag names are considered to be HTML tags. However, lower-case tag names with a dot (property accessor) aren’t.


Q14. What is the use of Refs?
Ans -> Refs are a function provided by React to access the DOM element and the React element that you might have created on your own.
They are used in cases where we want to change the value of a child component, without making use of props and all.
 


Q15. List down the advantages of React Router.
Ans -> 
1- react router is an NPM package.
2- it enables to implement the dynamic routing.
3- It allows you to display pages and allow users to navigate them.
4- It is a fully-featured client and server-side routing library for React.
5- React Router Dom is used to build single-page applications.
         

Q16. How is React Router different from Conventional Routing?
Ans -> 

React Router vs Conventional Routing: React Router is a library for React that provides routing functionality. It is different from conventional routing in a few ways.
First, React Router is declarative. This means that you specify what you want your route to look like, rather than specifying how to get there. This makes it more user-friendly and easier to read.



Q17.  How many ways can we style the React Component?
Ans -> 
internal css
inline css
external css
module css


Q18. Explain CSS Module styling in React?
Ans -> 
In the React application, we usually create a single .css file and import it to the main file so the CSS will be applied to all the components. But using CSS modules helps
to create separate CSS files for each component and is local to that particular file and avoids class name collision..


Q19. What are the three principles that Redux follows?
Ans -> 1- Single source of truth
2- State is read-only
3- Changes are made with pure functions


Q20. List down the components of Redux and explain the function of each component?
Ans -> 
1-store=>  Creates a Redux store that holds the complete state tree of our app. We will have a single store in your app.
2-Reducer=>  A reducer is a pure function, which returns the state of the application based on the action dispatched by the store..
3->Action=>  It is a payload of information that transmits data from an application to a store. They are the sole source of information for the store. One can send them to the store using store. dispatch() .

Example: const action =  {

type: “addEmployee”,

payload

}

dispatch(action);
4-view==> it is component and APi interface.


Q21. How to access the Redux store outside a component?
Ans -> 
import the store, then call store. dispatch() , passing the action you need to dispatch. It works the same as the dispatch function you get from props via react-redux's connect function.


Q22. Why do we use render() in React?
Ans -> 
React renders HTML to the web page by using a function called render().
The purpose of the function is to display the specified HTML code inside the specified HTML element.
In the render() method, we can read props and state and return our JSX code to the root component of our app.


Q23. Explain the Virtual DOM and its working?
Ans ->
In simple words, virtual DOM is just a copy of the original DOM kept in the memory and synced with the real DOM by libraries such as ReactDOM. This process is called Reconciliation.

How Virtual DOM works ?==>
1-So when there is a update in the virtual DOM, react compares the virtual DOM with a snapshot of the virtual DOM taken right before the update of the virtual DOM.

2-With the help of this comparison React figures out which components in the UI needs to be updated. This process is called diffing. The algorithm that is used for the diffing process is called as the diffing algorithm.



Q24. How does the state differ from props in React?
Ans -> 
The key difference between props and state is that state is internal and controlled by the component itself while props are external and controlled by whatever renders the component.


Q25. How would you create a form in React?
Ana ->
React offers a stateful, reactive approach to build a form. The component rather than the DOM usually handles the React form. In React, the form is usually implemented by using controlled components.

There are mainly two types of form input in React.

Uncontrolled component
Controlled component


