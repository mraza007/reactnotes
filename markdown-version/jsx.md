## What is `JSX`?
`JSX` stands for JavaScript Syntax Extension or some peoplelike to call this as JavaScript + XML.

JSX allows you write `html` code in JavaScript. For example, `const element= <h1>Hello World!</h1>;`.

It allows us to directly combine our UI logic in JavaScriptin a JS file.

_note:We don't have to use JSX to write code in react but jsx makes our lives easier_.

## JSX Rules
- JSX is more strict than HTML -- elements must either:
  - Have an explicit closing tag: `<b> … </b>`.
  - Be explicitly self-closed: `<input name="x" />
  - Cannot leave off that `/` or will get syntax error.

## Embedding JavaScript in JSX

- You can render javascript in jsx by using `{}`.

```js
class Render extends React.Component {
  render(){
    return <h1>2+2={2+2}</h1>;
    }
    }
```

## Conditional Logic in JSX
- You can use ternary operator.


```js
function getNum(){
	return Math.floor(Math.random() * 10) +1;
}

class Hello extends React.Component {
	render(){
	const num = getNum();
		return (
			<div>	
			<h1>Hello Your number is :{num}!</h1>
			<p>{num === 1 ? 'YESS':'Sorry'}</p>
			</div>
			)
	}
}

```

- Here's another way of doing conditionals in VIM

```js

class Hello extends React.Component {
	render(){
	const num = getNum();
	let msg;
	if (num === 7){
		msg = <h3>"You made it"</h3>;
	}
	else {
		msg = <h3> Try Next Time</h3>;
	}
		return (
			<div>	
			<h1>Hello Your number is :{num}!</h1>
			<p>{msg}</p>
			</div>
			)
	}
	}
```

## Looping In JSX
- Most common method is to use `map`, `array.map(fn)`.

Example ==>

```js
class Hello extends React.Component {
	render(){
		const {name,hobbies} = this.props;
		return(
			<div>
			<h1> Hello My Name is {name} </h1>
			<ul> My Hobbies are {hobbies.map(h => <li>{h}</li>)}</ul>
			</div>
		)
	}
	}
```

```js

class App extends React.Component {
	render(){
		return(
			<div>
			<h1> SLOT MACHINE </h1>
			<Hello name="Frank" hobbies={['playing video games','dancing']} /> 
			</div>
		)
	}
}
```

