1. Write the output with reason

```js
const person = {
  firstName: 'John',
  lastName: 'Doe',
};

let person2 = person;

person.firstName = 'Arya';

console.log(person2.firstName); output: Arya :Here we copy the value of person to person2 and the address of both is same so the value of firstName is `Arya` instead of `John`.

console.log(person.firstName); output: Arya : Value of firstName replaced with `Arya`.

console.log(person.lastName); output: Doe : Value of lastName is `Doe`. 

console.log(person == person2); output: true : Address of both variable is same.

console.log(person === person2); output: true: Address of both variable is same.

console.log(person.lastName === person2.lastName); output: true : value of both is same. 
```

2. Write the output with reason:

```js
let person = {
  firstName: 'John',
  lastName: 'Doe',
  address: {
    street: 'North 1st',
    city: 'San Jose',
    state: 'CA',
    country: 'USA',
  },
};

let personTwo = { ...person };

person.firstName = 'Arya';
person.city = 'Navada';

console.log(personTwo.firstName); John: Here value of person is cloned into personTwo, So the value of firstName is `John`
console.log(person.firstName); Arya: Here value of firstName in person variable replaced with value `Arya`
console.log(personTwo.lastName); Doe: Here value of person is cloned into personTwo, So the value of lastName is `Doe`
console.log(person.firstName === personTwo.firstName); false: Values of both are same but address of both are different so output is false 
console.log(person == personTwo); false: Values of both are same but address of both are different so output is false 
console.log(person === personTwo); false: Values of both are same but address of both are different so output is false 
console.log(person.address === personTwo.address); true: Here the value and address of both are same so output is true 
console.log(person.address == personTwo.address); true: Here the value and address of both are same so output is true 
console.log(personTwo.address.city); San Joes: Here the value and address of both are same so output is San Joes
console.log(person.address.city); : Value of city is `Navada`.
console.log(person.address.city == personTwo.address.city); true: Here the address of both are same so output is true
```

3. Write the output with reason:

```js
let person = {
  firstName: 'John',
  lastName: 'Doe',
  address: {
    street: 'North 1st',
    city: 'San Jose',
    state: 'CA',
    country: 'USA',
  },
};

let personTwo = { ...person, address: { ...person.address } };

person.firstName = 'Arya';
person.city = 'Navada';

console.log(personTwo.firstName); John: Here value of person is cloned into personTwo, So the value of firstName is `John`
console.log(person.firstName); Arya: Here value of firstName in person variable replaced with value `Arya`
console.log(personTwo.lastName); Doe:  Here value of person is cloned into personTwo, So the value of lastName is `Doe`
console.log(person.firstName === personTwo.firstName); false: Both variable value is different from each other so output is false. 
console.log(person == personTwo); false: Addrres is different 
console.log(person === personTwo); false: Addrres is different 
console.log(person.address === personTwo.address); false: Addrres is different 
console.log(person.address == personTwo.address); false: Addrres is different 
console.log(personTwo.address.city); San Jose: value of city is `San Jose`
console.log(person.address.city); San Jose: value of city is `Navada`
console.log(person.address.city == personTwo.address.city); false: Here address are different but we are compairing same value which equals to each other.
```

4. Clone the `blogs` variable into a new variable named `clonedBlogs`

```js
let blogs = [
  {
    id: 1,
    title: 'Post #1',
    body: 'My first blog post',
  },
  {
    id: 2,
    title: 'Post #2',
    body: 'My second blog post',
  },
  {
    id: 3,
    title: 'Post #3',
    body: 'My third blog post',
  },
];

// Your code goes here

let clonedBlogs = [{...blogs[0]}, {...blogs[1]}, {...blogs[2]}]


```

5. Clone the `question` variable into a new variable named `questionClone`

```js
var questions = [
  {
    prompt: 'Why is the sky blue?',
    responses: [
      'Because the color blue was on sale at Wallmart',
      'Because blue is the prettiest color',
      'Because the air molecules difract blue light more than any other color',
    ],
  },
  {
    prompt: 'Why are leaves usually green?',
    responses: [
      'So green caterpillars can hide better.',
      'Because leaves can more easily make energy with green light',
      "Because leaves absorb red and blue light so it's green that is reflected",
    ],
  },
];

let questionClone = [{...questions[0], responses:[...questions[0].responses]}, {...questions[1], responses:[...questions[1].responses]}]


```

6. Clone the `allBlogs` variable into a new variable named `allBlogsClone`

```js
var allBlogs = {
  id: 1,
  title: 'Alamofire JSON Serialization',
  body: 'All about serialization in Alamofire...',
  author: {
    id: 1,
    fullName: 'Jeff Potter',
    username: 'jpotts18',
  },
  comments: [
    {
      id: 1,
      body: 'Thanks for the help Jeff, this saved me hours',
    },
    {
      id: 2,
      body: 'Your welcome. I am happy to help!',
    },
  ],
};


let allBlogsClone = {...allBlogs, author: {...allBlogs.author}, comments: [{ ...allBlogs.comments[0], ...allBlogs.comments[1]

}]}

```

7. Clone the `person` variable into a new variable named `clonedPerson`

```js
let person = [
  {
    input: { name: 'Ryan' },
    output: { name: 'Ryan' },
  },
  {
    input: { name: { first: 'Ryan', last: 'Haskell-Glatz' } },
    output: { firstName: 'Ryan', lastName: 'Haskell-Glatz' },
  },
  {
    input: { name: 'Ryan', age: 24 },
    output: { name: 'Ryan', age: 24 },
  },
  {
    input: {
      name: { first: 'Ryan', last: 'Haskell-Glatz' },
      birthday: { year: 1993, month: 'Nov' },
    },
    output: {
      firstName: 'Ryan',
      lastName: 'Haskell-Glatz',
      birthdayYear: 1993,
      birthdayMonth: 'Nov',
    },
  },
];



let clonedPerson = JSON.parse(JSON.stringify(person));

```

8. Write a function named `cloneObject` that accepts an object and returns the clone of the object

```js
function cloneObject(clone) {
  return JSON.parse(JSON.stringify(clone));
}
// Run the test below to check your function

let user = {
  name: 'John',
  house: 'Stark',
  sisters: ['Arya', 'Sansa'],
};
let cloned = cloneObject(user);

let person = {
  firstName: 'John',
  lastName: 'Doe',
  address: {
    street: 'North 1st',
    city: 'San Jose',
    state: 'CA',
    country: 'USA',
  },
};

let clonedPerson = cloneObject(person);

console.log(
  `The user object is ${
    user == cloned ? `not clone` : `cloned successfully 😁👑`
  }`
);
console.log(
  `The person object is ${
    person == clonedPerson ? `not clone` : `cloned successfully 😁👑`
  }`
);
```
