![TypeScript](images/image1.jpeg)
# TypeScript Learning Series

##  custom type

*TypeScript can be used to create a custom type for various kinds of data structures*

**1. Defining Types**


> Syntax:

```bash
type Person = {
  name: string;
  age: number;
  email?: string; // Optional property
};

// Using the type

const person1: Person = {
  name: "Alice",
  age: 25
};
```

> Features:


*Union and Intersection Types*

```bash
type Name = string;
type Age = number;
type Person = Name | Age;

// Intersection

type Address = { street: string };
type Contact = { phone: string };
type Employee = Address & Contact;


Type Aliases

type StringOrNumber = string | number;
```

**2. Defining Interfaces**


> Syntax:

```bash
interface Person {
  name: string;
  age: number;
  email?: string;
}

// Using the interface

const person2: Person = {
  name: "Bob",
  age: 30
};
```
> Features

```bash
interface ContactInfo {
  phone: string;
}

interface Employee extends Person, ContactInfo {
  employeeId: number;
}

Merging Interfaces

interface Dog {
  breed: string;
}

interface Dog {
  age: number;
}

const myDog: Dog = { breed: "Labrador", age: 5 };
```

**3. Choosing Between Type and Interface**

*Use type if you need to create a union of string literals*

```bash
type Direction = "left" | "right" | "up" | "down";
```

<a href=" custom_type.md">
  <img src="images/button_next.png" alt="Next" style="width: 100px; height: auto; border: none;"/>
</a>
