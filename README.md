# react-checkbox-list
A bootstrap-style react component for checkbox list

This is just a simple react component that takes a meta data, translates it into a checkbox list and notifies change. That's all it does.

## Install

```sh
npm install react-checkbox-list
or
bower install react-checkbox-list
```

## Usage
Simply require it to use it:

```javascript
var CheckBoxList = require('react-checkbox-list');
```
Provide initial data:

```javascript
var data = [
  {value: 'apple', label: 'Apple'},
  {value: 'orange', label: 'Orange'},
  {value: 'banana', label: 'Banana', checked: true} // check by default
];

<CheckBoxList ref="chkboxList" defaultData={data} onChange={this.handleCheckboxListChange} />
```
Listen for changes and get the selected values:

```javascript
handleCheckboxListChange: function(values) {
  // values is array of selected item. e.g ['apple', 'banana']
}
```

Uncheck all items:

```javascript
uncheckAll: function() {
  this.refs.chkboxList.reset();
}
```

That's it for the API!

## License

MIT.
