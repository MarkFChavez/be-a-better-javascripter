### destructuring

```
var person = {
  name: 'mark',
  email: 'mark@js.com'
}

var { name, email } = person
```

```
// default value
var person = {
  email: 'hey@test.com'
}

var { name = 'Mark', email } = person

console.log(name) // Mark
```

```
// change object property name
var person = {
  n: 'mark',
  e: 'hey@test.com'
}

var { n: name, e: email } = person

console.log(name) // mark
console.log(email) // hey@test.com
```

```
// for arrays
var names = ['mark', 'christopher', 'billy']
var [a, b, c] = names

console.log(a) // mark
console.log(b) // christopher
console.log(c) // billy
```

```
// head and tail for arrays
var members = ['bob', 'joe', 'dan', 'albert']
var [bob, ...rest] = members

console.log(bob) // bob
console.log(rest) // ['joe', 'dan', 'albert']
```