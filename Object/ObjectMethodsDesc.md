
## Examples of Object Methods with Purpose

### `Object.assign(target, ...sources)`
**Purpose:** Copies values from one or more source objects to a target object.
```javascript
const target = { a: 1 };
const source = { b: 2, c: 3 };
const result = Object.assign(target, source);
console.log(result); // { a: 1, b: 2, c: 3 }
```

### `Object.create(proto, [propertiesObject])`
**Purpose:** Creates a new object with the specified prototype.
```javascript
const proto = { greet: function() { console.log('Hello!'); } };
const obj = Object.create(proto);
obj.greet(); // Hello!
```

### `Object.defineProperty(obj, prop, descriptor)`
**Purpose:** Adds a property to an object with a specified descriptor.
```javascript
const obj = {};
Object.defineProperty(obj, 'name', {
    value: 'John',
    writable: false
});
console.log(obj.name); // John
obj.name = 'Doe'; // Error in strict mode
```

### `Object.defineProperties(obj, props)`
**Purpose:** Adds multiple properties to an object.
```javascript
const obj = {};
Object.defineProperties(obj, {
    name: { value: 'John', writable: true },
    age: { value: 30, writable: false }
});
console.log(obj); // { name: 'John', age: 30 }
```

### `Object.entries(obj)`
**Purpose:** Returns an array of a given object's key-value pairs.
```javascript
const obj = { a: 1, b: 2 };
console.log(Object.entries(obj)); // [['a', 1], ['b', 2]]
```

### `Object.freeze(obj)`
**Purpose:** Freezes an object, preventing modifications.
```javascript
const obj = { a: 1 };
Object.freeze(obj);
obj.a = 2; // No effect
console.log(obj.a); // 1
```

### `Object.fromEntries(iterable)`
**Purpose:** Converts a list of key-value pairs into an object.
```javascript
const entries = [['a', 1], ['b', 2]];
const obj = Object.fromEntries(entries);
console.log(obj); // { a: 1, b: 2 }
```

### `Object.getOwnPropertyDescriptor(obj, prop)`
**Purpose:** Returns the descriptor of a property.
```javascript
const obj = { a: 1 };
const descriptor = Object.getOwnPropertyDescriptor(obj, 'a');
console.log(descriptor); // { value: 1, writable: true, enumerable: true, configurable: true }
```

### `Object.getOwnPropertyDescriptors(obj)`
**Purpose:** Returns all property descriptors of an object.
```javascript
const obj = { a: 1 };
const descriptors = Object.getOwnPropertyDescriptors(obj);
console.log(descriptors);
// { a: { value: 1, writable: true, enumerable: true, configurable: true } }
```

### `Object.getOwnPropertyNames(obj)`
**Purpose:** Returns an array of all properties (including non-enumerable) of an object.
```javascript
const obj = { a: 1, b: 2 };
console.log(Object.getOwnPropertyNames(obj)); // ['a', 'b']
```

### `Object.getOwnPropertySymbols(obj)`
**Purpose:** Returns an array of all symbol properties of an object.
```javascript
const sym = Symbol('key');
const obj = { [sym]: 'value' };
console.log(Object.getOwnPropertySymbols(obj)); // [Symbol(key)]
```

### `Object.getPrototypeOf(obj)`
**Purpose:** Returns the prototype of an object.
```javascript
const obj = {};
console.log(Object.getPrototypeOf(obj)); // {}
```

### `Object.is(value1, value2)`
**Purpose:** Compares if two values are the same.
```javascript
console.log(Object.is(25, 25)); // true
console.log(Object.is(NaN, NaN)); // true
```

### `Object.isExtensible(obj)`
**Purpose:** Checks if an object is extensible.
```javascript
const obj = {};
console.log(Object.isExtensible(obj)); // true
Object.preventExtensions(obj);
console.log(Object.isExtensible(obj)); // false
```

### `Object.isFrozen(obj)`
**Purpose:** Checks if an object is frozen.
```javascript
const obj = Object.freeze({ a: 1 });
console.log(Object.isFrozen(obj)); // true
```

### `Object.isSealed(obj)`
**Purpose:** Checks if an object is sealed.
```javascript
const obj = Object.seal({ a: 1 });
console.log(Object.isSealed(obj)); // true
```

### `Object.keys(obj)`
**Purpose:** Returns an array of an object's own enumerable property names.
```javascript
const obj = { a: 1, b: 2 };
console.log(Object.keys(obj)); // ['a', 'b']
```

### `Object.preventExtensions(obj)`
**Purpose:** Prevents new properties from being added to an object.
```javascript
const obj = { a: 1 };
Object.preventExtensions(obj);
obj.b = 2; // Error in strict mode
console.log(obj); // { a: 1 }
```

### `Object.seal(obj)`
**Purpose:** Seals an object, preventing new properties and making existing properties non-configurable.
```javascript
const obj = { a: 1 };
Object.seal(obj);
obj.a = 2; // Allowed
delete obj.a; // Error in strict mode
console.log(obj); // { a: 2 }
```

### `Object.setPrototypeOf(obj, proto)`
**Purpose:** Sets the prototype of an object.
```javascript
const proto = { greet: function() { console.log('Hello!'); } };
const obj = {};
Object.setPrototypeOf(obj, proto);
obj.greet(); // Hello!
```

### `Object.values(obj)`
**Purpose:** Returns an array of an object's own enumerable property values.
```javascript
const obj = { a: 1, b: 2 };
console.log(Object.values(obj)); // [1, 2]
```