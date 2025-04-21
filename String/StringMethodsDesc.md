
## Examples of JavaScript String Methods

### `charAt(index)`
```javascript
const str = "Hello";
console.log(str.charAt(1)); // Output: "e"
```

### `charCodeAt(index)`
```javascript
const str = "Hello";
console.log(str.charCodeAt(1)); // Output: 101 (Unicode of 'e')
```

### `concat(...strings)`
```javascript
const str1 = "Hello";
const str2 = "World";
console.log(str1.concat(" ", str2)); // Output: "Hello World"
```

### `endsWith(searchString)`
```javascript
const str = "Hello World";
console.log(str.endsWith("World")); // Output: true
```

### `includes(searchString)`
```javascript
const str = "Hello World";
console.log(str.includes("World")); // Output: true
```

### `indexOf(searchValue)`
```javascript
const str = "Hello World";
console.log(str.indexOf("o")); // Output: 4
```

### `lastIndexOf(searchValue)`
```javascript
const str = "Hello World";
console.log(str.lastIndexOf("o")); // Output: 7
```

### `localeCompare(compareStr)`
```javascript
const str1 = "apple";
const str2 = "banana";
console.log(str1.localeCompare(str2)); // Output: -1 (str1 comes before str2)
```

### `match(regex)`
```javascript
const str = "The rain in Spain";
console.log(str.match(/ain/g)); // Output: ["ain", "ain"]
```

### `matchAll(regex)`
```javascript
const str = "The rain in Spain";
const matches = str.matchAll(/ain/g);
for (const match of matches) {
    console.log(match[0]); // Output: "ain" (twice)
}
```

### `padEnd(targetLength, padString)`
```javascript
const str = "Hello";
console.log(str.padEnd(10, ".")); // Output: "Hello....."
```

### `padStart(targetLength, padString)`
```javascript
const str = "Hello";
console.log(str.padStart(10, ".")); // Output: ".....Hello"
```

### `repeat(count)`
```javascript
const str = "Hello";
console.log(str.repeat(3)); // Output: "HelloHelloHello"
```

### `replace(searchValue, newValue)`
```javascript
const str = "Hello World";
console.log(str.replace("World", "JavaScript")); // Output: "Hello JavaScript"
```

### `replaceAll(searchValue, newValue)`
```javascript
const str = "Hello World World";
console.log(str.replaceAll("World", "JavaScript")); // Output: "Hello JavaScript JavaScript"
```

### `search(regex)`
```javascript
const str = "The rain in Spain";
console.log(str.search(/ain/)); // Output: 5
```

### `slice(start, end)`
```javascript
const str = "Hello World";
console.log(str.slice(0, 5)); // Output: "Hello"
```

### `split(separator)`
```javascript
const str = "Hello World";
console.log(str.split(" ")); // Output: ["Hello", "World"]
```

### `startsWith(searchString)`
```javascript
const str = "Hello World";
console.log(str.startsWith("Hello")); // Output: true
```

### `substring(start, end)`
```javascript
const str = "Hello World";
console.log(str.substring(0, 5)); // Output: "Hello"
```

### `toLowerCase()`
```javascript
const str = "Hello World";
console.log(str.toLowerCase()); // Output: "hello world"
```

### `toUpperCase()`
```javascript
const str = "Hello World";
console.log(str.toUpperCase()); // Output: "HELLO WORLD"
```

### `trim()`
```javascript
const str = "   Hello World   ";
console.log(str.trim()); // Output: "Hello World"
```

### `trimStart()`
```javascript
const str = "   Hello World   ";
console.log(str.trimStart()); // Output: "Hello World   "
```

### `trimEnd()`
```javascript
const str = "   Hello World   ";
console.log(str.trimEnd()); // Output: "   Hello World"
```

### `valueOf()`
```javascript
const str = new String("Hello World");
console.log(str.valueOf()); // Output: "Hello World"
```
