---
title: CodeNation - Week 1
date: "2020-11-01T22:30:03.284Z"
description: "JavaScript fundametals"
---

Week 1 of the [CodeNation](https://wearecodenation.com/) bootcamp saw us diving straight into JavaScript fundamentals. At a high level here are some of the things I have learned:

##Variables
Variables are containers for storing data. In Javascript these containers don't specifically have to be assigned the type of data they will hold i.e Int, String & Boolean.

```javascript
let number = 1;
let name = "Sam Wilson";
let firstGatsbySite = true;
```

##Arrays
Unlike variables, Arrays can hold multiple values and multiple different data types within the same Array, including other Arrays.

```javascript
let favouriteMovies = ["Star Wars","Toy Story","Coco","Tangled"]
let randomArray = ["Star Wars",1,["num1","num2","num3"],"Apple"]
```

##Loops
Loops enable us to run code blocks multiple times to prevent repeating code. There are multiple different loops which all have their own individual use cases. It is important to know that the do/while loop doesn't check the conditional statement until the loop has been run once.

```javascript
for(i = 0; i < 5; i++){
    console.log(i);
}
//Expected result 0 1 2 3 4

let i = 0;

while(i < 5){
    console.log(i);
    i++;
}
//Expected result 0 1 2 3 4

let i = 0;
do{
    console.log(i);
    i++;
}
while(i < 5)
//Expected result 0 1 2 3 4


```

##Functions
In JavaScript we can create Functions, Functions are blocks of code that can perform specific tasks/calculate values. These functions are stored in memory until they are called.

The below Functions takes 2 arguments, num1 & num2 and adds the values together. The sum of these values are then returned (using the return keyword) and can be used when the Function is called and either be logged to the console or stored in a variable.

```javascript
let addTwoNumbers (num1,num2) => {
    return num1+num2;
}

console.log(addTwoNumbers(1,2))
//Expected result : 3
let sumOfTwoNumbers = addTwoNumbers(2,2);
console.log(sumOfTwoNumbers);
//Expected result : 4
```

##Objects
An object can contain multiple properties, the example below a person object; has a name, an age, an array of their favourite movies and even a function that will return a greeting.

```javascript
const person = {
    name: "Sam Wilson",
    age: "29",
    city: "Nottingham",
    favouriteMovies: ["Star Wars","Toy Story","Coco","Tangled"],
    function greeting(){
        return `Hi, my name is ${this.name}.`;
    }
}

console.log(person.name);
//Expected result: "Sam Wilson"
console.log(person.favouriteMovies[0]);
//Expected result: "Star Wars"
console.log(greeting());
//Expected result: "Hi, my name is Sam Wilson."
```