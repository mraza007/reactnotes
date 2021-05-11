## React Events
- State most commonly changes in direct response to some event.
- In React, every JSX element has built in attributes representing every kind of browser event.
- They are camel case like `onClick` and take callback functions as event listeners.

```js
<button onClick={function(e) { alert('You have clicked me') } } >
click me 
</button>

```

## There are more than `onClick()` events.
- `onMouseEnter()`
- onCopy() Copy Event alls you to add to clipboard

## Method Binding

- When your event handlers reference the keyword `this` watch out.
- When binding the method you will loose the `this` concept. when you pass a function as a event handler.

## Fixing our Binding.

- Use bind inline.
- Use an arrow function.
- Method bind in the constructor.

 1. Inline

 ```js
 <button onClick={this.Function.bind(this)}> </button>
 ```
#### Pros
- very explicit.

#### Cons
- goes against DRY principle when passed into multiple components.
- every time we call bind we are making a new function._


2. Arrow Function In line
 
```js
 <button onClick={() => this.function_name()}> </button>
```
### Pros
- No mention of Bind.

#### Cons
- goes against DRY principle when passed into multiple components.
- every time we call bind we are making a new function.
- Intent less clear.

### Bind in Constructor.

#### Pros
1. Its Explicit.
2. Its centralized at the top in constructor and its more performant.
3. Only need to bind once.


#### Cons.
1. Just looks ugly.


### Alternative Way of Binding.

```jsx
handleClick = () => {
  console.log("Hello")
  }
```
### Passing arguments in the Bind.
- `this.function_name.bind(this,c)

### Passing Functions to child Components.

- A very common pattern in React.
- The idea: children are often not stateful, but need to tell parents to change state.
- How we send data `back-up` to parent component.

### How data flows.
- A parent component defines a function.
- the function is passed as a prop to a child component.
- the child component invokes the prop.
- The parent function is called usually setting the new state.
- the parent component is re-rendered along the child component.
-
