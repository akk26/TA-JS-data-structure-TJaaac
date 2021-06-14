```js
let user = {
  name: 'Arya',
  sibling: ['Robb', 'Ryan', 'John'],
};
let allBrothers = ['Robb', 'Ryan', 'John'];
let brothersCopy = user.sibling;
let usename = user.name;
let newUser = user;
```

1. Memory representation

- Create the memory representation of the above snippet on notebook.
- Take a photo/screenshot and add it to the folder `code`

<!-- To add this image here use ![name](./hello.jpg) -->
![memory-box](./memory-box.jpg)
![memory-box](./memory-box-2.jpg)

2. Answer the following with reason:

- `user == newUser;` // true : Output is true because the address of both are same.
- `user === newUser;` // true : Output is true because the address of both are same.
- `user.name === newUser.name;` // true : Output is true because the address of both are same.
- `user.name == newUser.name;` // true : Output is true because the address of both are same.
- `user.sibling == newUser.sibling;` //true : Output is true because the address of both are same.
- `user.sibling === newUser.sibling;` // true : Output is true because the address of both are same.
- `user.sibling == allBrothers;` // false : Output is false because the address are different.
- `user.sibling === allBrothers;` // false : Output is false because the address are different
- `brothersCopy === allBrothers;` // false : Output is false because the address are different
- `brothersCopy == allBrothers;` // false : Output is false because the address are different
- `brothersCopy == user.sibling;` // true : Output is true because the address of both are same.
- `brothersCopy === user.sibling;`// true : Output is true because the address of both are same.
- `brothersCopy[0] === user.sibling[0];`// true : Output is true because the address of both are same.
- `brothersCopy[1] === user.sibling[1];` // true : Output is true because the address of both are same.
- `user.sibling[1] === newUser.sibling[1];` // true : Output is true because the address of both are same.
