1.Differences Between interface and type in TypeScript Both can define object structures. 
      1.interface is good for working with classes and can be merged if declared multiple times. 
      2.type is more flexible — can be used with unions, intersections, and primitives. interface uses extends for extending.

Example: Defining a Union and a Primitive Alias Using type for a union: 

type Status = "success" | "error" | "loading";
function showStatus(status: Status) 
{ 
console.log("Status is:", status); 
}
showStatus("success");

This cannot be done with interface: 
// This is NOT valid: 
interface Status = "success" | "error" | "loading";

Using type for primitives: 
type ID = string | number;
const userId: ID = 123; 
const guestId: ID = "guest-001";

This cannot be done with interface either: 
// Invalid: 
interface ID = string | number;

2.What is type inference in TypeScript? Why is it helpful? 
1.TypeScript uses inference to reduce the need for manual typing. 
2.It makes the code cleaner and still type-safe.

Example: let name = "Alice";
let age = 30;
function greet(user: string) { return Hello, ${user}; }
const greeting = greet(name);

We didn't specify string or number, but TypeScript knows it from the assigned values.
