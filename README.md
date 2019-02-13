


Hosted on Heroku.<br>

### Key learnings:

Calling functions in a component from a different component by passing onClick() in the props:<br>
(I am not 100% sure yet that this is best practice)<br>

#### App.js:<br>
The timeOut function is defined in App.js.
```
<StartButton context={ this.state } onClick={ this.timeOut.bind(this) }/>
```

#### StartButton.js:<br>
The timeOut function in App.js is called via the onClick on the component in StartButton.js
```
render(){
  return (
    <button className="game__start-button" type="button"
      onClick={ this.props.onClick } style={{ display: this.props.context.buttonDisplay }}>
      { this.props.context.buttonMessage }
    </button>
  )
};
```
