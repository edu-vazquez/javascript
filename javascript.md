###### object
Is a data structure that allows you to store and organize data and behavior together
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

###### class
```javascript
class myclass () {
  //code
}
```

###### method
Is a function that is associated with an object. In the context of object-oriented programming (OOP)
```javascript
class myclass () {
  // Method to greet someone
  greet() {
    return `Hello world!`;
    }
}
```

###### constructor
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
