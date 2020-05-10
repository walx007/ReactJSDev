#### Rendering UI Intro  
- Instead of using String Template ,React uses JavaScript objects to create React elements.  
- We'll use these React elements to describe what we want the page to look like, and React will be in charge of generating the DOM nodes to achieve the result.

--------------------------------------------------------------

## Lesson 2

- React uses it's ```.createElement()``` to create elements .This method takes in a description of an element and **returns a plain JavaScript object**.  

Syntax:  
```React.createElement( /* type */, /* props */, /* content */ );```  

React's .createElement() method to construct a "React element". The .createElement() method has the following signature:

> React.createElement( /* type */, /* props */, /* content */ );   
Let's break down what each item can be:

- type – either a string or a React Component This can be a string of any existing HTML element (e.g. 'p', 'span', or 'header') or you could pass a React component (we'll be creating components with JSX, in just a moment).

- props – either null or an object ,This is an object of HTML attributes and custom data about the element.

- content – null, a string, a React Element, or a React Component



- How do we actully get this above element onto the page?  
 This where React-Dom comes into play.  
 ##### React-Dom:
 React-DOM is just one way to use the React Library.  
  - In React ,process of deciding what to render is comopletl **decoupled** from actual rendering it.  
    - Decoupling make it possible to render stuff on :-
        1. On server.  
        2. On Native Devices.  
        3. On VR palteforms.  
 Here we will use React-DOM bcoz we are working in browser.So ReactDOM.render() rendersour elemnet into DOM Node.    
 
 #### Rendering Elements onto the DOM  
 In the previous video, we used ReactDOM's render() method to render our element onto a particular area of a page. 
 In particular, we rendered the element onto a DOM node called root. But where did this root come from?  
 Apps built with React typically have a single root DOM node. For example, an HTML file may contain a `<div id="root"></div>`. 
 
 ##### JSX | JSX Returns One Main Element, Too just like create element.
 however, we use a syntax extension to describe what your UI should look like. This syntax extension is known as JSX, and just looks similar to plain HTML written right into a JavaScript file. The JSX gets transpiled to React's .createElement() method that outputs HTML to be rendered in the browser.
 
 ##### Intro to Components
So far we've seen how .createElement() and JSX can help us produce some HTML. Typically, though, we'll use one of React's key features, Components, to construct our UI. Components refer to reusable pieces of code ultimately responsible for returning HTML to be rendered onto the page. More often than not, you'll see React components written with JSX.  

Since React's main focus is to streamline building our app's UI, there is only one method that is absolutely required in any React component class: render().

#### 💡 Declaring Components in React 💡, we defined the ContactList component like so:

```class ContactList extends React.Component {// ...}```  
  OR 
 ``` class ContactList extends Component {// ...}``` in this case adjust imports ex- ```import React, { Component } from 'react';```

  
  
  

