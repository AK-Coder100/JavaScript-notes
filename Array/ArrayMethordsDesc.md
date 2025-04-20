## Mutator Methods
- `push()` - Adds one or more elements to the end of an array.
    ```javascript
    const fruits = ['apple', 'banana'];
    fruits.push('orange');
    console.log(fruits); // ['apple', 'banana', 'orange']
    ```

- `pop()` - Removes the last element from an array.
    ```javascript
    const fruits = ['apple', 'banana', 'orange'];
    fruits.pop();
    console.log(fruits); // ['apple', 'banana']
    ```

- `shift()` - Removes the first element from an array.
    ```javascript
    const fruits = ['apple', 'banana', 'orange'];
    fruits.shift();
    console.log(fruits); // ['banana', 'orange']
    ```

- `unshift()` - Adds one or more elements to the beginning of an array.
    ```javascript
    const fruits = ['banana', 'orange'];
    fruits.unshift('apple');
    console.log(fruits); // ['apple', 'banana', 'orange']
    ```

- `splice()` - Adds or removes elements from an array.
    ```javascript
    const fruits = ['apple', 'banana', 'orange'];
    fruits.splice(1, 1, 'grape');
    console.log(fruits); // ['apple', 'grape', 'orange']
    ```

- `sort()` - Sorts the elements of an array.
    ```javascript
    const numbers = [3, 1, 4, 1, 5];
    numbers.sort();
    console.log(numbers); // [1, 1, 3, 4, 5]
    ```

- `reverse()` - Reverses the order of the elements in an array.
    ```javascript
    const numbers = [1, 2, 3];
    numbers.reverse();
    console.log(numbers); // [3, 2, 1]
    ```

- `fill()` - Fills all elements in an array with a static value.
    ```javascript
    const numbers = [1, 2, 3];
    numbers.fill(0);
    console.log(numbers); // [0, 0, 0]
    ```

- `copyWithin()` - Copies part of an array to another location in the same array.
    ```javascript
    const numbers = [1, 2, 3, 4, 5];
    numbers.copyWithin(0, 3);
    console.log(numbers); // [4, 5, 3, 4, 5]
    ```

## Accessor Methods
- `concat()` - Merges two or more arrays.
    ```javascript
    const arr1 = [1, 2];
    const arr2 = [3, 4];
    const result = arr1.concat(arr2);
    console.log(result); // [1, 2, 3, 4]
    ```

- `join()` - Joins all elements of an array into a string.
    ```javascript
    const fruits = ['apple', 'banana', 'orange'];
    const result = fruits.join(', ');
    console.log(result); // 'apple, banana, orange'
    ```

- `slice()` - Returns a shallow copy of a portion of an array.
    ```javascript
    const fruits = ['apple', 'banana', 'orange'];
    const result = fruits.slice(1, 3);
    console.log(result); // ['banana', 'orange']
    ```

- `indexOf()` - Returns the first index of a specified element.
    ```javascript
    const fruits = ['apple', 'banana', 'orange'];
    const index = fruits.indexOf('banana');
    console.log(index); // 1
    ```

- `lastIndexOf()` - Returns the last index of a specified element.
    ```javascript
    const numbers = [1, 2, 3, 2];
    const index = numbers.lastIndexOf(2);
    console.log(index); // 3
    ```

- `includes()` - Checks if an array includes a certain value.
    ```javascript
    const fruits = ['apple', 'banana', 'orange'];
    const result = fruits.includes('banana');
    console.log(result); // true
    ```

- `toString()` - Converts an array to a string.
    ```javascript
    const fruits = ['apple', 'banana', 'orange'];
    console.log(fruits.toString()); // 'apple,banana,orange'
    ```

- `toLocaleString()` - Converts an array to a localized string.
    ```javascript
    const date = [new Date()];
    console.log(date.toLocaleString()); // e.g., '10/10/2023, 12:00:00 AM'
    ```

## Iteration Methods
- `forEach()` - Executes a function for each array element.
    ```javascript
    const numbers = [1, 2, 3];
    numbers.forEach(num => console.log(num));
    // Output: 1 2 3
    ```

- `map()` - Creates a new array with the results of calling a function on every element.
    ```javascript
    const numbers = [1, 2, 3];
    const squared = numbers.map(num => num * num);
    console.log(squared); // [1, 4, 9]
    ```

- `filter()` - Creates a new array with elements that pass a test.
    ```javascript
    const numbers = [1, 2, 3, 4];
    const even = numbers.filter(num => num % 2 === 0);
    console.log(even); // [2, 4]
    ```

- `reduce()` - Reduces the array to a single value by executing a function.
    ```javascript
    const numbers = [1, 2, 3, 4];
    const sum = numbers.reduce((acc, num) => acc + num, 0);
    console.log(sum); // 10
    ```

- `reduceRight()` - Same as `reduce()`, but processes the array from right to left.
    ```javascript
    const numbers = [1, 2, 3, 4];
    const sum = numbers.reduceRight((acc, num) => acc + num, 0);
    console.log(sum); // 10
    ```

- `some()` - Checks if at least one element passes a test.
    ```javascript
    const numbers = [1, 2, 3];
    const hasEven = numbers.some(num => num % 2 === 0);
    console.log(hasEven); // true
    ```

- `every()` - Checks if all elements pass a test.
    ```javascript
    const numbers = [2, 4, 6];
    const allEven = numbers.every(num => num % 2 === 0);
    console.log(allEven); // true
    ```

- `find()` - Returns the first element that passes a test.
    ```javascript
    const numbers = [1, 2, 3];
    const result = numbers.find(num => num > 1);
    console.log(result); // 2
    ```

- `findIndex()` - Returns the index of the first element that passes a test.
    ```javascript
    const numbers = [1, 2, 3];
    const index = numbers.findIndex(num => num > 1);
    console.log(index); // 1
    ```

- `keys()` - Returns an iterator for the keys of an array.
    ```javascript
    const fruits = ['apple', 'banana'];
    const keys = fruits.keys();
    for (let key of keys) {
        console.log(key); // 0 1
    }
    ```

- `values()` - Returns an iterator for the values of an array.
    ```javascript
    const fruits = ['apple', 'banana'];
    const values = fruits.values();
    for (let value of values) {
        console.log(value); // 'apple' 'banana'
    }
    ```

- `entries()` - Returns an iterator for key-value pairs in an array.
    ```javascript
    const fruits = ['apple', 'banana'];
    const entries = fruits.entries();
    for (let [key, value] of entries) {
        console.log(key, value); // 0 'apple', 1 'banana'
    }
    ```

## Other Methods
- `Array.isArray()` - Checks if a value is an array.
    ```javascript
    console.log(Array.isArray([1, 2, 3])); // true
    console.log(Array.isArray('not an array')); // false
    ```

- `Array.from()` - Creates a new array from an array-like or iterable object.
    ```javascript
    const str = 'hello';
    const arr = Array.from(str);
    console.log(arr); // ['h', 'e', 'l', 'l', 'o']
    ```

- `Array.of()` - Creates a new array with a variable number of arguments.
    ```javascript
    const arr = Array.of(1, 2, 3);
    console.log(arr); // [1, 2, 3]
    ```
