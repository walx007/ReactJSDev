#### Rendering UI Intro  
- Instead of using String Template ,React uses JavaScript objects to create React elements.  
- We'll use these React elements to describe what we want the page to look like, and React will be in charge of generating the DOM nodes to achieve the result.

--------------------------------------------------------------

## Lesson 2

- React uses it's ````.createElement()``` to create elements .This method takes in a description of an element and **returns a plain JavaScript object**.  
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
  
  
  

