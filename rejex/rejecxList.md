
# 🌟 Fundamentals of Writing Regular Expressions (Regex) with Examples 🌟

Regular expressions (regex) are powerful patterns used to match character combinations in strings. Below are the fundamental concepts with examples:

---

## 1. **🔤 Basic Syntax**
- `.`: Matches any single character except newline.  
    ```javascript
    const regex = /a.c/;
    console.log(regex.test("abc")); // true
    console.log(regex.test("ac"));  // false
    ```
- `^`: Matches the start of a string.  
    ```javascript
    const regex = /^Hello/;
    console.log(regex.test("Hello world")); // true
    console.log(regex.test("world Hello")); // false
    ```
- `$`: Matches the end of a string.  
    ```javascript
    const regex = /world$/;
    console.log(regex.test("Hello world")); // true
    console.log(regex.test("world Hello")); // false
    ```
- `*`: Matches 0 or more occurrences of the preceding element.  
    ```javascript
    const regex = /ab*/;
    console.log(regex.test("a"));    // true
    console.log(regex.test("abb"));  // true
    ```
- `+`: Matches 1 or more occurrences of the preceding element.  
    ```javascript
    const regex = /ab+/;
    console.log(regex.test("ab"));   // true
    console.log(regex.test("a"));    // false
    ```
- `?`: Matches 0 or 1 occurrence of the preceding element.  
    ```javascript
    const regex = /colou?r/;
    console.log(regex.test("color"));  // true
    console.log(regex.test("colour")); // true
    ```
- `{n}`: Matches exactly `n` occurrences of the preceding element.  
    ```javascript
    const regex = /a{3}/;
    console.log(regex.test("aaa")); // true
    console.log(regex.test("aa"));  // false
    ```
- `{n,}`: Matches `n` or more occurrences.  
    ```javascript
    const regex = /a{2,}/;
    console.log(regex.test("aa"));    // true
    console.log(regex.test("aaaa"));  // true
    ```
- `{n,m}`: Matches between `n` and `m` occurrences.  
    ```javascript
    const regex = /a{2,4}/;
    console.log(regex.test("aa"));    // true
    console.log(regex.test("aaaaa")); // false
    ```

---

## 2. **🔢 Character Classes**
- `[abc]`: Matches any one of the characters `a`, `b`, or `c`.  
    ```javascript
    const regex = /[aeiou]/;
    console.log(regex.test("apple")); // true
    console.log(regex.test("sky"));   // false
    ```
- `[^abc]`: Matches any character except `a`, `b`, or `c`.  
    ```javascript
    const regex = /[^0-9]/;
    console.log(regex.test("abc")); // true
    console.log(regex.test("123")); // false
    ```
- `[a-z]`: Matches any lowercase letter from `a` to `z`.  
    ```javascript
    const regex = /[a-z]/;
    console.log(regex.test("hello")); // true
    console.log(regex.test("123"));   // false
    ```
- `[0-9]`: Matches any digit.  
    ```javascript
    const regex = /[0-9]/;
    console.log(regex.test("123")); // true
    console.log(regex.test("abc")); // false
    ```

---

## 3. **📚 Predefined Character Classes**
- `\d`: Matches any digit (equivalent to `[0-9]`).  
    ```javascript
    const regex = /\d+/;
    console.log(regex.test("123")); // true
    console.log(regex.test("abc")); // false
    ```
- `\D`: Matches any non-digit.  
    ```javascript
    const regex = /\D+/;
    console.log(regex.test("abc")); // true
    console.log(regex.test("123")); // false
    ```
- `\w`: Matches any word character (alphanumeric + underscore).  
    ```javascript
    const regex = /\w+/;
    console.log(regex.test("hello_123")); // true
    console.log(regex.test("@#$"));       // false
    ```
- `\W`: Matches any non-word character.  
    ```javascript
    const regex = /\W+/;
    console.log(regex.test("@#$")); // true
    console.log(regex.test("abc")); // false
    ```
- `\s`: Matches any whitespace character.  
    ```javascript
    const regex = /\s+/;
    console.log(regex.test(" "));   // true
    console.log(regex.test("abc")); // false
    ```
- `\S`: Matches any non-whitespace character.  
    ```javascript
    const regex = /\S+/;
    console.log(regex.test("abc")); // true
    console.log(regex.test(" "));   // false
    ```

---

## 4. **📍 Anchors**
- `\b`: Matches a word boundary.  
    ```javascript
    const regex = /\bcat\b/;
    console.log(regex.test("cat"));      // true
    console.log(regex.test("scatter")); // false
    ```
- `\B`: Matches a non-word boundary.  
    ```javascript
    const regex = /\Bcat/;
    console.log(regex.test("scatter")); // true
    console.log(regex.test("cat"));     // false
    ```

---

## 5. **🔗 Groups and Alternation**
- `(abc)`: Matches the exact sequence `abc`.  
    ```javascript
    const regex = /(cat|dog)/;
    console.log(regex.test("cat")); // true
    console.log(regex.test("dog")); // true
    ```
- `|`: Acts as an OR operator.  
    ```javascript
    const regex = /a|b/;
    console.log(regex.test("a")); // true
    console.log(regex.test("c")); // false
    ```

---

## 6. **🛠️ Escaping Special Characters**
- Use `\` to escape special characters.  
    ```javascript
    const regex = /\./;
    console.log(regex.test("."));  // true
    console.log(regex.test("abc")); // false
    ```

---

## 7. **⚙️ Modifiers**
- `i`: Case-insensitive matching.  
    ```javascript
    const regex = /hello/i;
    console.log(regex.test("Hello")); // true
    console.log(regex.test("HELLO")); // true
    ```
- `g`: Global matching (find all matches).  
    ```javascript
    const regex = /a/g;
    console.log("banana".match(regex)); // ['a', 'a', 'a']
    ```
- `m`: Multiline matching.  
    ```javascript
    const regex = /^hello/m;
    console.log(regex.test("hello\nworld")); // true
    ```

---

## 8. **🔍 Lookaheads and Lookbehinds**
- `(?=...)`: Positive lookahead.  
    ```javascript
    const regex = /\d(?=px)/;
    console.log(regex.test("5px")); // true
    console.log(regex.test("5em")); // false
    ```
- `(?!...)`: Negative lookahead.  
    ```javascript
    const regex = /\d(?!px)/;
    console.log(regex.test("5em")); // true
    console.log(regex.test("5px")); // false
    ```
- `(?<=...)`: Positive lookbehind.  
    ```javascript
    const regex = /(?<=\$)\d+/;
    console.log(regex.test("$100")); // true
    console.log(regex.test("USD100")); // false
    ```
- `(?<!...)`: Negative lookbehind.  
    ```javascript
    const regex = /(?<!\$)\d+/;
    console.log(regex.test("USD100")); // true
    console.log(regex.test("$100"));  // false
    ```

---

## 9. **📖 Examples**
- `^\d{3}-\d{2}-\d{4}$`: Matches a Social Security number format (e.g., `123-45-6789`).  
    ```javascript
    const regex = /^\d{3}-\d{2}-\d{4}$/;
    console.log(regex.test("123-45-6789")); // true
    ```
- `\bcat\b`: Matches the word `cat` as a whole word.  
    ```javascript
    const regex = /\bcat\b/;
    console.log(regex.test("cat"));      // true
    console.log(regex.test("scatter")); // false
    ```
- `\w+@\w+\.\w+`: Matches an email address (e.g., `example@domain.com`).  
    ```javascript
    const regex = /\w+@\w+\.\w+/;
    console.log(regex.test("example@domain.com")); // true
    ```

---

## 10. **🧪 Testing and Debugging**
- Use tools like [regex101](https://regex101.com/) or [RegExr](https://regexr.com/) to test and debug your regex patterns.
- Experiment with different patterns to understand their behavior.
- Always test edge cases to ensure your regex works as expected.
