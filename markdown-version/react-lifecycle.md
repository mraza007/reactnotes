# React Component LifeCycle

Every component comes with methods that allow developers to update the application state and reflect the changes in to the UI before/after key react **events**

* There are three main phases to know
  * Mounting
  * Updating
  * unmounting

#### `ComponentDidMount()`

- This method runs after the component is mounted.
- This is a good place to load any data via `AJAX` or setupsubscriptions or timers.
- Calling `setState()` here will trigger re-render , so be cautious.


### `ComponentDidMount()` Example

- Let's start a timer when a Clock instance is first rendered in the DOM.
- `ComponentDidMount()` method runs after the component has been rendered.
- ComponentDidMount() runs first time after the render method

### Making API Calls In React.

- You need `axios` library

```js
import React, { Component } from 'react'
import axios from 'axios'

class Ajax extends Component {
    constructor(props){
        super(props)
            this.state = {
                quote:'Hey There'
            }
        
    }
    componentDidMount(){
        axios.get("https://api.github.com/zen").then(res => {
            this.setState({
                quote:res.data
            })
        })
    }
    render(){
        return(
            <div>
                <h1>Hello World</h1>
                <p>{this.state.quote}</p>
            </div>
        )
    }
}


export default Ajax
```
### `ComponentDidUpdate()`

This is good place to implement any side effect operations.

- syncing up the local storage.
- autosave
- updating the dom for uncontrolled components.

## `componentWillUnmount()`

When a component is unmounted or destroyed, this will be called. this is a place to do clean up like:
- Invalidating timers.
- canceling network requests.
- removing event handlers.
- cleaning up subscriptions.
