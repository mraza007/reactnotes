## ES 2015 Module Imports.

We have two files `helper.js` and `index.js`

#### `helper.js` code

```js
function hello (){
    alert('HELLO WE MADE IT');
}

export default hello;
```

As you can see `helper.js` is exporting `hello()` function.

and this will be imported by `index.js` file.


```js
import hello from './helper';

hello();
```
