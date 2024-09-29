# Js Simplify Coding

This package help to simplify our coding journy in javascript. It's Provide Various Fuction and method to help achive more functionality to solve your problem.

## Installation

To install this package run

```bash
  npm install js-simplify-coding
```

## Documentation

## 1. Deep Copy

Your Can copy nested Array and Object its return new array/object
. Try this

```bash
  require('js-simplify-coding');
```

or

```bash
  import 'js-simplify-coding';
```

Example 1:-

```bash
  let object1={
        name:'Test',
        age:20,
        address:{
            pincode:100000,
            phone:'90XXXXXXXX'
        },
        hobby:['cricket','Learning']
  }

  let object2=object1._deepClone()
  object1.age=40;

  console.log(object1)
  console.log(object2);

```

Output:-

```bash
{
  name: 'Test',
  age: 40,
  address: { pincode: 100000, phone: '90XXXXXXXX' },
  hobby: [ 'cricket', 'Learning' ]
}

{
  name: 'Test',
  age: 20,
  address: { pincode: 100000, phone: '90XXXXXXXX' },
  hobby: [ 'cricket', 'Learning' ]
}

```

Example 2:-

```bash

let arr1 = [3, 4, 5, 6];
let arr2 = arr1._deepClone();
arr1.push(4444);

console.log(arr1);
console.log(arr2);

```

Output:-

```bash

[ 3, 4, 5, 6, 4444 ]
[ 3, 4, 5, 6 ]

```
