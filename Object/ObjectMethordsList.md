# JavaScript Object Methods

Here is a list of commonly used JavaScript object methods along with their purposes and examples:

## Object Methods with Purpose

| Method                                      | Purpose                                                                 |
|---------------------------------------------|-------------------------------------------------------------------------|
| `Object.assign(target, ...sources)`         | Copies values from one or more source objects to a target object.      |
| `Object.create(proto, [propertiesObject])`  | Creates a new object with the specified prototype.                     |
| `Object.defineProperty(obj, prop, descriptor)` | Adds a property to an object with a specified descriptor.             |
| `Object.defineProperties(obj, props)`       | Adds multiple properties to an object.                                 |
| `Object.entries(obj)`                       | Returns an array of a given object's key-value pairs.                  |
| `Object.freeze(obj)`                        | Freezes an object, preventing modifications.                           |
| `Object.fromEntries(iterable)`              | Converts a list of key-value pairs into an object.                     |
| `Object.getOwnPropertyDescriptor(obj, prop)` | Returns the descriptor of a property.                                 |
| `Object.getOwnPropertyDescriptors(obj)`     | Returns all property descriptors of an object.                         |
| `Object.getOwnPropertyNames(obj)`           | Returns an array of all properties (including non-enumerable) of an object. |
| `Object.getOwnPropertySymbols(obj)`         | Returns an array of all symbol properties of an object.                |
| `Object.getPrototypeOf(obj)`                | Returns the prototype of an object.                                    |
| `Object.is(value1, value2)`                 | Compares if two values are the same.                                   |
| `Object.isExtensible(obj)`                  | Checks if an object is extensible.                                     |
| `Object.isFrozen(obj)`                      | Checks if an object is frozen.                                         |
| `Object.isSealed(obj)`                      | Checks if an object is sealed.                                         |
| `Object.keys(obj)`                          | Returns an array of an object's own enumerable property names.         |
| `Object.preventExtensions(obj)`            | Prevents new properties from being added to an object.                 |
| `Object.seal(obj)`                          | Seals an object, preventing new properties and making existing properties non-configurable. |
| `Object.setPrototypeOf(obj, proto)`         | Sets the prototype of an object.                                       |
| `Object.values(obj)`                        | Returns an array of an object's own enumerable property values.        |
