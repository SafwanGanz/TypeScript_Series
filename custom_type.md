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
