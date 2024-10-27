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

