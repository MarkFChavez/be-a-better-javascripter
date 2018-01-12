### var, let and const

- `var` is function-scoped.
- `let` and `const` are block-scoped.
- `const` is not immutable; but you can't change its reference
- Always use `const` if you think the value won't change; Use `let` otherwise.
- Try to avoid `var` as much as possible.

```
e.g.
const person = {
  name: 'mark'
}

person.name = 'joel' // this works

person = { name: 'bad' } // this doesn't
```

```
// var
function firstFunction () {
  // first function scope
  var name = 'Mark'

  function secondFunction () {
    // second function scope
    var language = 'English'
  }

  secondFunction()

  console.log(name) // Mark
  console.log(language) // English
}
```

```
// let
function myFunction () {
  // new scope
  function insideScope () {
    let name = 'Mark'
  }

  insideScope()

  console.log(name) // undefined
}
```