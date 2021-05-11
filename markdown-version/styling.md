## Styling

```js
class Hello extends React.Component {
	render(){
		console.log(this.props)
		const {s1,s2,s3} = this.props
		const winner = (s1 === s2) && (s2 === s3)
		const styles = {fontSize:'20px', backgroundColor:'yellow' };
		return (
			<div>
			<h3 style={styles}>{s1} {s2} {s3} </h3>
			<h1 className={winner ? 'win':'lose'}>{winner ? 'WINNER !!!' : 'LOSSER'}</h1>

			</div>
			)
	}
}

```
you can toggle css classes based on a condition
