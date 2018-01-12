### hoisting

- it places all `var` at the top of the function scope.
- it is very important to understand how hoisting works. please always keep this in mind.

```
// before hoisting
console.log(message)
var message = 'I love Javascript!'
```

```
// after hoisting
var message = 'I love Javascript!'
console.log(message)
```

```
// hoisting with functions
function sampleFunction () {
  var names = []

  for(var i = 0; i < names.length; i++) {
    var modifiedName = names[i].toUpperCase()
    names.push(modifiedName)
  }

  return names
}
```

```
// after hoisting with functions
function sampleFunction () {
  var names = []
  var i;
  var modifiedName;

  for(i = 0; i < names.length; i++) {
    modifiedName = names[i].toUpperCase()
    names.push(modifiedName)
  }

  return names
}
```