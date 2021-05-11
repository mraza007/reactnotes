## React State

### What is State?
- In any sufficiently advanced webapps, the user interface has to be stateful.
- logged-in users see a different screen than logged out users.
- clicking `edit profile` opens up a modal window.
- sections of a website can expand or collapse.
- the state of the client interface is not always directly tied to state on the server.
- A state is designed to constantly change in response to the events (Think of a chess game)


### What does State Track?
- There are two types of things state on the client/frontend keeps track of:
  - **UI logic** - the changing state of the interface e.g, there is a modal open right now because Im editing my profile.
  - business logic: the changing state of data e.g in my inbox, messages are either read or unread and this in turn affects how they display.
  - Before we used `Vanilla/jQuery State`.

#### React State
- A little Recap:
  - Component
    - A building block of React.
    - Combines logic(JS) and presentation (JSX).
  - Props
    - data passed to a component (or found via defaults)
    - immutable; component cannot change its own props.
  - State
    - internal data specific to a component.
    - data that changes over time.

- In React, state is an instance attribute on a component. Its always an object (POJO),since you'll want to keep track of several keys/values.
- State should be initialized as soon as the component is created.

## React Constructor Function

- If your component is stateless, you can omit the constructor function.
- If you are building a component with state, you need a standard React Constructor.


```js
constructor(props){
  super(props);
  this.state = {
    // things go here
    };
  }
```
- constructor takes one arguement,props
- you must call `super(props)` at start of constructor, which registers your class as a React Component.
- Inside the instance methods,you can refer to `this.state` just like you did `this.state`
- you have to initialize `state` but you don't have to initialize `prop`.

## State VS Props
- State and Props are the most concepts in React after learning about components.

### State
- State is POJO (Plain Old JavaScript Object).
- It is Mutable.
- Stores changing component data.

### Prop
- Prop is POJO (Plain Old JavaScript Object).
- Its not mutable.
- Stores Component Configuration.


## React State Patterns.
- Learn how to update state based off of existing state.
- Properly manage state updates for mutable data structures.
- Discuss best practices for modeling state and designing components.

### setState()
- setState() is asynchronous. So its risky to assume previous call has finished when you call it. Also, React will sometimes batch calls to setState together into on for performance reasons.
- If a call to `setState()` depends on current state, the safest thing is to use the alternate `callback form`.
- Instead of passing an object, pass it a callback with the current state as a parameter.
- The callback should return an object representing a new state.
- `this.setState(callback)`

### Abstracting State Updates.
- The fact you can pass a function to `this.setState` lends itself nicely to more advanced pattern called functional `setState()`.

## Designing State
- Designing the state of a react app is a challenging skill and it takes time.

### Minimizing State
- Putting data as little as possible
- If you need change alot then it is supposed to be in state.

```js
this.state = {
  firstName: 'Matt'
  lastName: 'James'
  birthday: 3/4/2000
  age: 21
  mood: 'happy'
  }
```
* Does first or last name ever changes ?
* Does birthdate ever changes?
* Age does change but we have birthday
* Only mood changes so it makes sense to be in the state.

### State should live on the parent.

* Downward Data Flow.
* This makes the debugging easier because the state is centralized 
