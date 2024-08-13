## statements
### switch
```javascript
const fruit = 'apple'; // Variable to test
switch (fruit) {
    case 'apple':
    case 'banana':
        console.log('This is a fruit.');
        break;
    case 'carrot':
        console.log('This is a vegetable.');
        break;
    default:
        console.log('Unknown item.');
}
```
## functions
### function declaration:

```javascript
// Function declaration
function greet(name) {
    return `Hello, ${name}!`;
}
// Using the function
console.log(greet('Alice')); // Output: Hello, Alice!
```
### function expression:
```javascript
// Function expression
const add = function(a, b) {
    return a + b;
};
// Using the function
console.log(add(5, 3)); // Output: 8
```
### arrow function:
```javascript
// Arrow function, Block Body Syntax
const multiply = (a, b) => {
    return a * b
    };
// arrow functon: Concise Body Syntax
const multiply = (a, b) => a * b;  //implicit return

// Using the function
console.log(multiply(4, 6)); // Output: 24
```

## OOP (object-oriented programming)

### object
is a data structure that stores properties and methods. 
**property** key-value pairs. 
**key** is the name of the property in the object.
**alue** is the data associated with a particular key in the object.
```javascript
// Define an object
const car = {
    make: 'Toyota',
    model: 'Corolla',
    year: 2020,
    getDescription() {
        return `${this.year} ${this.make} ${this.model}`;
    }
};

// Access properties
console.log(car.make);                // dot notation | Output: Toyota
console.log(car['make']);            // bracket notation (useful when the key is dynamic or not a valid identifier): | Output: Toyota

// Access methods
console.log(car.getDescription());    // Output: 2020 Toyota Corolla

// Adding a New Property:
car.color = 'Blue'; // Adds a new key 'color' with the value 'Blue'

//Modifying an Existing Property:
car.year = 2021; // Updates the value of 'year' to 2021

//Deleting a Property using delete Operator:
delete car.isElectric; // Removes the 'isElectric' property from the car object

//Enumerating Properties using for...in Loop:
for (let key in car) {
    console.log(key + ': ' + car[key]);
}
```
### class
is a blueprint for creating objects with shared properties and methods.
```javascript
// Define a class
class Car {
    constructor(make, model, year) {
        this.make = make;    // Property
        this.model = model;  // Property
        this.year = year;    // Property
    }

    // Method to get a description of the car
    getDescription() {
        return `${this.year} ${this.make} ${this.model}`;
    }
}

// Create new instances of the Car class
const car1 = new Car('Toyota', 'Corolla', 2020);

// Access properties and methods of the instances
console.log(car1.make);             // Output: Toyota
console.log(car1.getDescription()); // Output: 2020 Toyota Corolla
```
### class: method
is a function that is associated with an object. In the context of object-oriented programming (OOP)
```javascript
class MyClass {
  greet() {
    return `Hello world!`;
  }
}

// Create an instance and call the method
const instance = new MyClass();
console.log(instance.greet()); // Output: Hello world!
```
### class: constructor
Is a special method used to initialize objects.
```javascript
class Person {
    constructor(name) {
        this.name = name;
    }
    greet() {
        return `Hello ${this.name}.`;
    }
}
// Create an instance and call the constructor
const person1 = new Person('Alice');
console.log(person1.greet()); // Output: Hello Alice.
```
#### Inheritance
A way to create a new class from an existing class.
```javascript
// Base class
class Animal {
    constructor(name) {
        this.name = name;
    }
    speak() {
        return `${this.name} makes a noise.`;
    }
}
// Subclass
class Dog extends Animal {
    speak() {
        return `${this.name} barks.`;
    }
}
// Create an instance of the subclass
const dog = new Dog('Rex');
console.log(dog.speak()); // Output: Rex barks.
```
#### Encapsulation
Hiding internal details with private properties.
```javascript
class BankAccount {
    #balance; // Private property
    constructor(initialBalance) {
        this.#balance = initialBalance;
    }
    getBalance() {
        return this.#balance;
    }
    deposit(amount) {
        if (amount > 0) {
            this.#balance += amount;
        }
    }
}
// Create an instance and use methods
const account = new BankAccount(100);
account.deposit(50);
console.log(account.getBalance()); // Output: 150
```
#### Static Methods
Methods that belong to the class, not instances.
```javascript
class MathUtils {
    static add(a, b) {
        return a + b;
    }
}
// Call static method on the class
console.log(MathUtils.add(5, 3)); // Output: 8
```
#### Getters and Setters
Special methods to get and set property values.
```javascript
class Person {
    constructor(name) {
        this._name = name;
    }
    get name() {
        return this._name;
    }
    set name(value) {
        this._name = value;
    }}

// Create an instance and use getters/setters
const person = new Person('Alice');
console.log(person.name); // Output: Alice
person.name = 'Bob';
console.log(person.name); // Output: Bob

```


### glosary
**element** is a part of the Document Object Model (DOM) <div>, <p>, <a>, etc.
**instance :** is a specific object created from a class or prototype.

### APIS
**requestAnimationFrame()** is used in web development to create smooth animations in the browser
```javascript
requestAnimationFrame(callback);
```

**clearRect()** is part of the HTML5 Canvas API, is a method used to clear a rectangular area of the canvas, effectively removing any content within that region.
```javascript
context.clearRect(x, y, width, height);
```
context = canvas.getContext("2d");
x: The x-coordinate of the rectangle’s starting point.
y: The y-coordinate of the rectangle’s starting point.
width: The width of the rectangle.
height: The height of the rectangle.
