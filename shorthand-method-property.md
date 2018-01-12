### shorthand method and property name

- if the object key has the same name as its value, you can omit the
value.
- for methods, you can omit the `function` keyword

```
// BEFORE
function getPerson (name, age, email) {
  const person = {
    name: name,
    age: age,
    email: email,
    save: function () {
      // save something here
    }
  }

  return person
}
```

```
// AFTER
function getPerson (name, age, email) {
  const person = {
    name,
    age,
    email,
    save () {
      // save something here
    }
  }

  return person
}
```