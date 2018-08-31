# Task filtering arrays

## Description

To map and filter arrays, taditionally you would use `for` loops
to loop through an array and operate on its values.

```JavaScript
const myArray            = [null, 1, 2, 3, 'four', '5'];
const myArrayOnlyNumbers = [];

for (let i = 0; i < myArray.length; i += 1) {
  const currentValue = myArray[i];
  if ('number' === typeof currentValue) {
    myArrayOnlyNumbers.push(currentValue);
  }
}

console.log(myArrayOnlyNumbers); // logs: [1, 2, 3]
```

This can be done much easier and faster using the filter function:

```JavaScript
const myArray            = [null, 1, 2, 3, 'four', '5'];
const myArrayOnlyNumbers = myArray.filter(currentValue =>
    'number' === typeof currentValue);

console.log(myArrayOnlyNumbers); // logs: [1, 2, 3]
```

## Task

Given is an array:

```JavaScript
const myArray = [{
  _id     : 1,
  username: 'arnold',
  email   : 'arnold.schwarzenegger@coursar.io',
  personal: { firstName: 'Arnold', lastName: 'Schwarzenegger', birthday: '1947-07-30' },
  tags    : ['actor', 'guvernor', 'Mr. Universe', 'Terminator', 'funny'],
  meta    : { createdAt: '2017-05-24', updatedAt: '2018-08-11' },
}, {
  _id     : 2,
  username: 'thedonald',
  email   : 'donald.trump@coursar.io',
  personal: { firstName: 'Donald', middlename: 'John', lastName: 'Trump', birthday: '1946-06-14' },
  tags    : ['President', 'bad actor', 'kriminal', 'stupid'],
  meta    : { createdAt: '2017-09-10', updatedAt: '2018-10-03' },
}, {
  _id     : 3,
  username: 'jackblack',
  email   : 'jack.black@coursar.io',
  personal: { firstName: 'Jack', lastName: 'Black', birthday: '1969-08-28' },
  tags    : ['Tenaciuos D', 'actor', 'songwriter', 'funny'],
  meta    : { createdAt: '2017-08-10', updatedAt: '2018-08-14' },
}, {
  _id     : 4,
  username: 'jimmy',
  email   : 'jim.parsons@coursar.io',
  personal: { firstName: 'Jim', lastName: 'Parsons', birthday: '1973-03-24' },
  tags    : ['Big Bang Theory', 'bad actor', 'far less intelligent than he things he is', 'not funny'],
  meta    : { createdAt: '2017-08-10', updatedAt: '2017-11-14' },
}];
```

1. Filter this array so that it only contains good actors.
   Write the result into the variable `goodActors`;
1. Filter this array so that it only contains funny actors.
   Write the result into the variable `funnyActors`;
1. Filter this array so that it only contains actors bord after 1965.
   Write the result into the variable `kindOfYoungActors`;
1. Filter this array so that it only contains actors data which has been updated in 2018.
   Write the result into the variable `recentlyUpdatedActors`;

## Template

Use the file `solution.js` for the tests to run your solution.
You can use the template in the file to solve your tasks.
If not, there still needs to be a exported `solution` function
which returns said variables.
