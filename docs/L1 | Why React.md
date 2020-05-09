https://www.linkedin.com/pulse/compose-me-function-composition-javascript-kevin-greene  
https://hackernoon.com/javascript-functional-composition-for-every-day-use-22421ef65a10

#### Why React  
There 4 things that make React Special-  
1. It's Composition Modal.
2. It's Declrative Nature.
3. The way data flows through a component.
4. React is just "javascript".

##### The Composition Modal
- *Composition* - Composition is to combine simple functions to build more complicated ones.  
In programing context ,Composition occurs when simple functions are combined together to create more complex functions.  
- A good function should follow the "DOT" rule:
> Do One Thing  

Composition is built from simple functions. Let's look at an example:  
```function getProfileLink (username) { return 'https://github.com/' + username }```  
This function is ridiculously simple, isn't it? It's just one line! Similarly, the getProfilePic function is also just a single line:
```function getProfilePic (username) {return 'https://github.com/' + username + '.png?size=200'}```  
These are definitely simple functions, so to compose them, we'd just combine them together inside another function:

```function getProfileData (username) { return {pic: getProfilePic(username), link: getProfileLink(username) }} ```   
Now we could have written getProfileData without composition by providing the data directly:

```getProfileData (username) {return {pic: 'https://github.com/' + username + '.png?size=200',link: 'https://github.com/' + username}}```  
There's nothing technically wrong with this at all; this is entirely accurate JavaScript code. But this isn't composition. 
There are also a couple of potential issues with this version that isn't using composition. If the user's link to GitHub is needed somewhere else, then duplicate code would be needed.
A good function should follow the "DOT" rule:

> Do One Thing.  

In the composed version, each function just does one thing:  
- `getProfileLink` – just builds up a string of the user's GitHub profile link  
- `getProfilePic` – just builds up a string the user's GitHub profile picture  
- `getProfileData` – returns a new object .

##### React & Composition  
React makes use of the power of composition, heavily! React builds up pieces of a UI using components.


