# Js Simplify Coding

This package help to simplify our coding journy in javascript. It's Provide Various Fuction and method to help achive more functionality to solve your problem.

## Installation

To install this package run

```bash
  npm install js-simplify-coding
```

## Documentation

## 1. Deep Copy

You Can copy nested Array and Object its return new array/object
. Try this

```bash
  require('js-simplify-coding');
```

#### or

```bash
  import 'js-simplify-coding';
```

#### Example 1:-

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

#### Output:-

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

#### Example 2:-

```bash

let arr1 = [3, 4, 5, 6];
let arr2 = arr1._deepClone();
arr1.push(4444);

console.log(arr1);
console.log(arr2);

```

#### Output:-

```bash

[ 3, 4, 5, 6, 4444 ]
[ 3, 4, 5, 6 ]

```

## 2. Check Is Equal

You can compare two variable value of any data type (Array/Object ) and nested value. Try this

```base
const { isEqual } = require("js-simplify-coding");

```

#### or

```base
import {isEqual} from 'js-simplify-coding';

```

### isEqual(arg1,arg2,symbol)

#### 1. arg1 (Required) First value

#### 2. arg2 (Required) Second value

#### 3. symbol (Optional), ('==' or '===') default (==)

#### Example 1:-

```bash
console.log(isEqual(2,2))
console.log(isEqual(5,'5'))
console.log(isEqual(10,10,'==='))
console.log(isEqual(10,"10",'==='))

```

#### Output:-

```bash
true
true
true
false

```

#### Example 2:-

```bash

let temp1 = {
  name: "Nitesh",
  age: 25,
  arr: [9, 88, 8],
  info: {
    add: "Bihar",
  },
  hi: undefined,
};

let temp2 = {
  name: "Nitesh",
  age: 25,
  arr: [8, 88, 9],
  info: {
    add: "Bihar",
  },
  hi: undefined,
};

let temp3 = {
  name: "Nitesh",
  age: 26,
  arr: [8, 88, 9],
  info: {
    add: "Bihar",
  },
  hi: undefined,
};

let temp4 = {
  name: "Nitesh",
  age: "25",
  arr: [8, 88, 9],
  info: {
    add: "Bihar",
  },
  hi: undefined,
};

console.log(isEqual(temp1, temp2));
console.log(isEqual(temp1, temp2,'==='));
console.log(isEqual(temp1, temp3));
console.log(isEqual(temp1, temp4,'==='));

```

#### Output:-

```bash
true
true
false
false

```
