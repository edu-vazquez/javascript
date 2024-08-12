## OOP (Object-Oriented Programming)

### object
A data structure that stores properties and methods.
```javascript
// Create an object representing a car
const car = {
    make: 'Toyota',        // Property
    model: 'Corolla',      // Property
    year: 2020,            // Property

    // Method to describe the car
    getDescription: function() {
        return `${this.year} ${this.make} ${this.model}`;
    },

    // Method to start the car
    start: function() {
        return `${this.make} ${this.model} is starting...`;
    }
};
```

// Accessing properties
console.log(car.make);           // Output: Toyota
console.log(car.model);          // Output: Corolla

// Using methods
console.log(car.getDescription()); // Output: 2020 Toyota Corolla
console.log(car.start());          // Output: Toyota Corolla is starting...

### class
A blueprint for creating objects with shared properties and methods.
```javascript
// Define a class
class MyClass {
    // Method
    //Properties
}
```

### method
Is a function that is associated with an object. In the context of object-oriented programming (OOP)
```javascript
class myclass () {
  // Method to greet someone
  greet() {
    return `Hello world!`;
    }
}
```

### constructor
Is a special method used to initialize objects.
```javascript
// Define a class named Person
class Person {
    // Constructor to initialize the person's name and age
    constructor(name) {
        this.name = name; // Initialize the name property
    }

    // Method to describe the person
    greet() {
        return `Hello ${this.name}.`;
    }
}

// Create an instance of the Person class
const person1 = new Person('Alice');

// Use the describe method
console.log(person1.describe()); // Output: Hello Alice.
```

#### Inheritance
A way to create a new class from an existing class.
```javascript
class Animal {
    constructor(name) {
        this.name = name;
    }
    speak() {
        return `${this.name} makes a noise.`;
    }
}

class Dog extends Animal {
    speak() {
        return `${this.name} barks.`;
    }
}
```
#### Encapsulation
Hiding internal details with private properties.
```javascript
class BankAccount {
    #balance;
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
```
#### Static Methods
Methods that belong to the class, not instances.
```javascript
class MathUtils {
    static add(a, b) {
        return a + b;
    }
}
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
    }
}
```
