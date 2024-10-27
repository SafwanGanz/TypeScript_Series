![TypeScript](images/image1.jpeg)
# TypeScript Learning Series

## Data Structures

*data structures can be represented in various ways.*


**1. Arrays**

*Arrays are used to store a collection of elements*

```bash
let numbers: number[] = [1, 2, 3, 4];
let names: string[] = ["Alice", "Bob", "Charlie"];
```

**2. Tuples**

*Tuples allow storing multiple types in a fixed-size array*

```bash
let person: [string, number];
person = ["Alice", 25];
```

**3. Enums**

*Enums are used to define a set of named constants*

```bash
enum Direction {
    North,
    South,
    East,
    West,
}

let dir: Direction = Direction.North;
```

**4. Interfaces**

*Interfaces are used to define the structure of an object*

```bash
interface Person {
    name: string;
    age: number;
}

let person: Person = {
    name: "Alice",
    age: 25
};
```

**5. Classes**

*Classes are used to create objects with properties and methods*

```bash
class Animal {
    name: string;
    constructor(name: string) {
        this.name = name;
    }
    speak() {
        console.log( `${this.name} makes a noise. ` );
    }
}

let dog = new Animal("Dog");
dog.speak();
```

**6. Maps**

*Maps store key-value pairs with keys of any data type*

```bash
let map: Map<string, number> = new Map();
map.set("Alice", 25);
map.set("Bob", 30);

console.log(map.get("Alice")); // Output: 25
```

**7. Sets**

*Sets store unique values of any type*

```bash
let set: Set<number> = new Set([1, 2, 3, 3]);
set.add(4);
console.log(set); // Output: Set { 1, 2, 3, 4 }
```
