# What is Component?
- The building blocks of React breaking down into reusable pieces.
- Pieces of UI and view Logic
- `js`,`html`,`css` combined together into one.

## Example Component (Not a react example)

```js
class Dog {
  constructor (name,color) {
    this.name = name;
    this.color = color;
    }

    render () { 
      return `<p>${this.name}</p>`
    }
}
```
- Everything in react app is comprised of a component.

## Writing Components in React

- You can write components as a `function` or a `class`.
- Function components are similar to `Class` components but `Class` component offers more features compared to function component.
- We will mostly use `class` components.

## Functions VS Class Components.

### Function Components
- Function Components are used for simpler stuff 
- Write Logic in JS function.
- No render method needed,just return content
- Functions can't use import features like `state` or `LifeCycle Methods`
- With introduction of `react hooks` you can write full featured fuctions.

## Structuring Components (App Layout)
- Each Component is represented by a file. For example Hello Component might be a `Hello.js` File. In simple wordsone component per file.
- Then we use `App` Component to render all our other components.


