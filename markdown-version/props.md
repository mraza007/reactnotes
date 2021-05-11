## Properties aka Props

- props allows us to make our components more customizable.

```js
class Hello extends React.Component {
	render(){
		console.log(this.props)
		return <h1> Hello From {this.props.from} To {this.props.to} </h1>;
	}
}
```

```js
class App extends React.Component {
	render(){
		return(
			<div>
			<Hello to="Ringo" from="Paul"/>
			</div>
		)
	}
}
```

In the example above as you can see we are passing data to our hello component.

## Properties Requirements.

- Properties are for configuring the component.
- Properties are immutable. We cannot change it.
- Properties can be strings. `<User name="tony" title="data-analyst" />`
- You can also use `arrays` , `numbers`, `boolean values`. you might use `{}` to embed the `js` expression.

```js
<User name="Jane" salary={1000} hobbies={["bridge" "reading","test"],} />
```
## Default Props.
- Components cant specify values for missing props. Basically adding a default value.

```js
class Hello extends React.Component {
	static defaultProps = {
		name:'Anon'
	}
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

For instance if someone doesn't pass their name `Anon ` willl be rendered
