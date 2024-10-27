![TypeScript](images/image1.jpeg)
# TypeScript Learning Series

## Advanced Types

*open up powerful ways to create dynamic, flexible, and reusable types. Here’s an overview of some important advanced types*

**1. Mapped Types**

*Mapped types let you create new types by transforming properties of an existing type. For example, you can make each property of a type optional or readonly*

 ```bash
type Person = {
  name: string;
  age: number;
};

// Make all properties of Person optional

type PartialPerson = {
  [Key in keyof Person]?: Person[Key];
};

// Make all properties of Person readonly

type ReadonlyPerson = {
  readonly [Key in keyof Person]: Person[Key];
};
```

**2. Conditional Types**

*Conditional types allow you to create types that depend on a condition. They use a syntax similar to ternary operators*

```bash
type IsString<T> = T extends string ? "Yes" : "No";

type Test1 = IsString<string>;  // "Yes"
type Test2 = IsString<number>;  // "No"
```

*Conditional types are especially useful in utility types and can be combined with generics*

**3. Utility Types**

*TypeScript comes with a set of built-in utility types that help transform types. Some commonly used ones include:*

> Partial: Makes all properties in a type optional.

```bash
type PartialPerson = Partial<Person>;
```

> Required: Makes all properties in a type required.

```bash
type RequiredPerson = Required<Person>;
```

> Readonly: Makes all properties in a type readonly.

```bash
type ReadonlyPerson = Readonly<Person>;
```

> Pick: Creates a type by picking a set of properties from another type.

```bash
type NameOnly = Pick<Person, "name">;
```

> Omit: Creates a type by omitting a set of properties from another type.

```bash
type WithoutAge = Omit<Person, "age">;
```

*These can be helpful when working with complex types and APIs.*

**4. Index Types and Lookup Types**

*Index types allow you to dynamically reference the types of properties within other types*

```bash
type Person = {
  name: string;
  age: number;
};

type PersonName = Person["name"];  // string
```

**5. Template Literal Types**

*Template literal types allow you to create types based on string literal patterns, similar to JavaScript template literals*

```bash
type Greeting = `Hello, ${string}`;

let message: Greeting = "Hello, World";  // Valid
```

*These are useful for creating types that follow a particular format, such as specific string patterns for CSS classes or IDs*

<a href="advanced_types.md">
  <img src="images/button_next.png" alt="Next" style="width: 100px; height: auto; border: none;"/>
</a>
