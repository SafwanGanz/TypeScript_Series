![TypeScript](images/image1.jpeg)
# TypeScript Learning Series

## Type Composition

**1. Type Aliases**

*Type aliases allow you to create custom types with a descriptive name, which can make your code easier to understand and maintain*

```bash
type UserID = string | number;
let userId: UserID = 123;
```


**2. Interfaces**

*Interfaces define the shape of an object and can be extended or implemented, making them essential for object-oriented patterns in TypeScript*

```bash
interface Person {
  name: string;
  age: number;
}

interface Employee extends Person {
  employeeId: number;
}
```

**3. Functions and Function Types**

*TypeScript allows you to specify the types of function parameters and return types, adding more safety to function usage*

```bash
function greet(name: string): string {
  return `Hello, ${name}`;
}
```

*You can also define function types to create reusable function signatures:*

```bash
type GreetFunction = (name: string) => string;
let greetUser: GreetFunction = (name) => `Hi, ${name}`;
```

**4. Generics**

*Generics provide a way to create reusable components that can work with different types while maintaining strict type checking*

```bash
function wrapInArray<T>(value: T): T[] {
  return [value];
}

const numberArray = wrapInArray(42);  // T inferred as number
const stringArray = wrapInArray("Hello");  // T inferred as string
```
*Generics are commonly used in functions, classes, and interfaces to create flexible, type-safe components*

<a href=" .md">
  <img src="images/button_next.png" alt="Next" style="width: 100px; height: auto; border: none;"/>
</a>


