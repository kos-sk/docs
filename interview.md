# Frontend dev Tech Interview plan

Matherials for **Frontend engineer** position technical part of interview.

## JavaScript/TypeScript questions section

#### 1. What are the data types present in JS?
Clarify if not mentioned:
  - Truthy and falsy values
  - Difference beetween null and undefined
  - == and ===
  - Why we need bigint 


#### 2. Please explain Hoisting and Scope concepts.
Code explainer. What will be logged in console?
```js
var foo = 1;
var foobar = function() {
  console.log(foo);
  var foo = 2;
}
foobar();
```
Clarify if not mentioned:
  - const and let behviour in terms of hoisting
  - block scope in ES6

#### 3. Tell us about Closures in JS.
Code explainer. What will be logged in console? How to change it to get 'logical' behaviour?
```js
for(var i = 0; i < 10; i++) {
    setTimeout(function() {
        console.log(i);
    }, 1000);
}
```
Clarify if not mentioned:
  - **const** and **let** behviour in terms of hoisting
  - block scope in ES6

#### 4. Prototypes and inheritance.
Clarify if not mentioned:
  - hasOwnProperty() function

Code explainer. What will be logged in console?
```js
Object.prototype.bar = 1;

var foo = {moo: 2};
for(var i in foo) {
    console.log(i);
}
```

#### 5. Multithreading in JS? What is event loop in JS? 
Code explainer. What will be logged in console?
```js
console.log('Hi!');

setTimeout(() => {
    console.log('Execute immediately.');
}, 0);

console.log('Bye!');
```

#### 6. What is Set in JS? What is time complexity of .has() in Set ?
Clarify if not mentioned:
  - BigO notation discussion
  - How Hashtables usually implemented? Collision resolving strategies.

#### 7. How do you clone an object in JS?
Clarify if not mentioned:
  - How JS passes objects: by reference or value?
  - Why JSON.parse(JSON.stringify(obj)) not always an option?

#### 8. What is the purpose of JavaScript UI libraries/frameworks like React, Vue, Angular?
Clarify if not mentioned:
  - Virtual DOM

#### 9. Explain what is meant by "TypeScript is a superset of JavaScript"
Clarify if not mentioned:
  - Key TypeScript Features on top of JavaScript?
  - Benefits?

#### 10. Interface vs Abstract class in TypeScript?
  - ![trololo](/img/troll.png)

#### 11. Generics in TypeScript and why you could use them?
  - Is it possible to use generics with Interfaces?

#### 12. How do you enable strict null checks in TypeScript?
Clarify if not mentioned:
  - Why we need it at all?
  - Other tsconfig.json options?

## CSS/HTML questions section

#### 1.  What is the CSS Box Model?
Clarify if not mentioned:
- Box Sizing (border-box/content-box)
- Auto Margins

#### 2. What is the difference between b and strong tags
Discussion about semantics here.

#### 3. How do you add a comment in HTML and why would you use them?
Discussion about code-commenting culture here.

#### 4. What is the ":hover" pseudo-class and how does it work?
Clarify if not mentioned:
- Other pseudo-classes which you know (:first-child, :enabled, :visited)?

#### 5. What is the web-safe font? Mention some of them?
Clarify if not mentioned:
- What to do if you need a custom font?

#### 6. How do you center a block element with CSS?
Clarify if not mentioned:
  - Horizontal Centering/Vertical Centering - Auto margins/Flexbox (justify-content: center)/?

#### 7. What is a media query?
Clarify if not mentioned:
  - Media types, especially 'print'

#### 8. CSS preprocessors (SASS\LESS\etc) features?
Clarify if not mentioned:
  - SASS: variables, mixins, parent selector (&)

#### 5. Describe approaches to resolving browser compatibility issues in CSS. 
Clarify if not mentioned:
  - W3C Markup Validation Service
  - Did you use CSS linting and formatting tools?  Linters (CSS Lint, Dirty Markup)

## React questions section

#### 1. Can you explain the virtual DOM in React? 
Clarify if not mentioned:
  - What is React Fiber? (Reconciliation), Selective Rendering, Batched Updates, Asynchronous Handling
  
#### 2. What are the differences between class and functional component?
Clarify if not mentioned:
  - Which of them allow lifecycle methods? Which lifecycle methonds do you know?
  - Can functional components be seamlessly integrated with Redux?
  - useState and useContext hooks

#### 3. How do you update the state of a parent component from a child component
Clarify if not mentioned:
  - Global State Management: Redux or MobX. Does any app need it?
  - Data Services to manage shared state?

#### 4. What's wrong with that code?
```js
this.setState({
  counter: this.state.counter + this.props.increment
});
```
Note: Props and State could be changes asyncronously. correct: this.setState((state, props) => 

#### 5. How do you update the state of a parent component from a child component
Clarify if not mentioned:
  - Global State Management: Redux or MobX. Does any app need it?
  - Data Services to manage shared state?

#### 6. What is Higher Order Components (HOCs)?
Any sample were to use it.

#### 7. Is it possible to get access to some DOM element in React?
Hook useRef() or function React.createRef() 

#### 8. React DevTools - how it makes developer's life easier? 

## Tooling and common questions section

#### 1. NPM or Yarn? Differences?
Clarify if not mentioned:
  - paralle or sequential installation?
  - node_modules and .lock files differences

#### 2. Have you ever configured Webpack manually?
Usecase why it could be required?

#### 3. Security-related questions:
Waht do you know about:
   - CORS
   - XSS
   - Approaches to handle user sessions and tokens

#### 4. What is WebSockets? Usecases? 
Long polling approach vs WebSockets?

#### 5. What usually you setup on CI\CD for Frontend part of applications?
Tests Unit\Integration, linting, formatting, publishing.
#### 6. Which branching strategy do you prefer for development?
Here discussion about source control, code review practicies, maybe pros\cons of GitFlow? 
#### 7. Any experience of using components libraries
antd, react suite, extjs, devextream?

#### 8. e.t.c...
