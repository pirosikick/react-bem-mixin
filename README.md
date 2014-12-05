react-bem-mixin
==================

React.js Mixin for BEM

## USAGE

```sh
$ npm install --save react-bem-mixin
```

```javascript
var React = require('react');
var BEMMixin = require('react-bem-mixin');

var HelloMessage = React.createClass({
  mixins: [BEMMixin.element('message')],

  render: function () {
    return (
      <h1 className={ this.bem.className }>
        Hello, { this.props.name }!
      </h1>
    );
  }
})

var HelloBlock = React.createClass({
    mixins: [BEMMixin.block('hello')],

    render: function () {
        return (
          <div className={ this.bem.className() }>
            <HelloMessage name="pirosikick" />
          </div>
        );
    }
})

React.renderToString(<HelloBlock/>);
```
```html
<div class="hello">
  <h1 class="hello__message">Hello, pirosikick!</h1>
</div>
```
