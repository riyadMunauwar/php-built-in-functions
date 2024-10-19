Below is the **Markdown documentation** for the PHP string functions you requested. It’s organized with a brief description and code example for each function. You can copy this directly to your **GitHub README.md** file.

---

# 📄 PHP String Functions - Complete Documentation with Examples

This document provides a list of built-in PHP string functions, grouped by functionality with descriptions and code examples.

---

## **Table of Contents**
1. [String Manipulation Functions](#string-manipulation-functions)
2. [Searching & Replacing Strings](#searching--replacing-strings)
3. [Regular Expressions](#regular-expressions)
4. [Formatting Strings](#formatting-strings)
5. [Splitting & Joining Strings](#splitting--joining-strings)
6. [HTML and URL Functions](#html-and-url-functions)
7. [String Encoding and Decoding](#string-encoding-and-decoding)
8. [String Comparison](#string-comparison)
9. [String Tokenization](#string-tokenization)
10. [String Padding](#string-padding)
11. [Miscellaneous](#miscellaneous)

---

## 1. String Manipulation Functions

### `strlen()`
Get the length of a string.

```php
echo strlen("Hello World!");  // Output: 12
```

### `strtolower()`
Convert a string to lowercase.

```php
echo strtolower("HELLO WORLD!");  // Output: hello world!
```

### `strtoupper()`
Convert a string to uppercase.

```php
echo strtoupper("hello world!");  // Output: HELLO WORLD!
```

### `ucfirst()`
Make the first character uppercase.

```php
echo ucfirst("hello world!");  // Output: Hello world!
```

### `lcfirst()`
Make the first character lowercase.

```php
echo lcfirst("Hello World!");  // Output: hello World!
```

### `ucwords()`
Capitalize the first letter of each word.

```php
echo ucwords("hello world!");  // Output: Hello World!
```

### `strrev()`
Reverse a string.

```php
echo strrev("Hello World!");  // Output: !dlroW olleH
```

### `trim()`
Remove whitespace from both ends of a string.

```php
echo trim("  Hello World!  ");  // Output: Hello World!
```

### `ltrim()`
Remove whitespace from the start of a string.

```php
echo ltrim("  Hello World!  ");  // Output: Hello World!  
```

### `rtrim()`
Remove whitespace from the end of a string.

```php
echo rtrim("  Hello World!  ");  // Output:   Hello World!
```

---

## 2. Searching & Replacing Strings

### `strpos()`
Find the position of the first occurrence of a substring.

```php
echo strpos("Hello World!", "World");  // Output: 6
```

### `stripos()`
Case-insensitive version of `strpos()`.

```php
echo stripos("Hello World!", "world");  // Output: 6
```

### `strrpos()`
Find the last occurrence of a substring.

```php
echo strrpos("Hello World World!", "World");  // Output: 12
```

### `strripos()`
Case-insensitive version of `strrpos()`.

```php
echo strripos("Hello World World!", "world");  // Output: 12
```

### `str_contains()`  
Check if a string contains a substring (PHP 8+).

```php
var_dump(str_contains("Hello World!", "World"));  // Output: bool(true)
```

### `str_starts_with()`  
Check if a string starts with a given substring (PHP 8+).

```php
var_dump(str_starts_with("Hello World!", "Hello"));  // Output: bool(true)
```

### `str_ends_with()`  
Check if a string ends with a given substring (PHP 8+).

```php
var_dump(str_ends_with("Hello World!", "World!"));  // Output: bool(true)
```

### `str_replace()`
Replace all occurrences of a search string with another.

```php
echo str_replace("World", "PHP", "Hello World!");  // Output: Hello PHP!
```

### `str_ireplace()`
Case-insensitive version of `str_replace()`.

```php
echo str_ireplace("world", "PHP", "Hello World!");  // Output: Hello PHP!
```

### `substr()`
Extract a portion of a string.

```php
echo substr("Hello World!", 6, 5);  // Output: World
```

---

## 3. Regular Expressions

### `preg_match()`
Perform a regular expression match.

```php
if (preg_match("/world/i", "Hello World!")) {
    echo "Match found!";
}  // Output: Match found!
```

### `preg_match_all()`
Find all matches of a regular expression.

```php
preg_match_all("/world/i", "Hello World! World!", $matches);
print_r($matches);
```

### `preg_replace()`
Replace substrings matching a regex.

```php
echo preg_replace("/world/i", "PHP", "Hello World!");  // Output: Hello PHP!
```

### `preg_split()`
Split a string using a regex.

```php
print_r(preg_split("/[\s,]+/", "Hello, World! How are you?"));
```

---

## 4. Formatting Strings

### `number_format()`
Format a number with grouped thousands.

```php
echo number_format(1234567.891, 2);  // Output: 1,234,567.89
```

### `sprintf()`
Return a formatted string.

```php
echo sprintf("There are %d apples", 5);  // Output: There are 5 apples
```

---

## 5. Splitting & Joining Strings

### `explode()`
Split a string into an array.

```php
print_r(explode(" ", "Hello World!"));
```

### `implode()` / `join()`
Join array elements into a string.

```php
echo implode("-", ["Hello", "World"]);  // Output: Hello-World
```

---

## 6. HTML and URL Functions

### `htmlspecialchars()`
Convert special characters to HTML entities.

```php
echo htmlspecialchars("<a href='test'>Test</a>");  // Output: &lt;a href='test'&gt;Test&lt;/a&gt;
```

### `urlencode()`
URL-encode a string.

```php
echo urlencode("Hello World!");  // Output: Hello+World%21
```

---

## 7. String Encoding and Decoding

### `base64_encode()`
Encode data to Base64.

```php
echo base64_encode("Hello World!");  // Output: SGVsbG8gV29ybGQh
```

### `md5()`
Calculate the MD5 hash of a string.

```php
echo md5("password");  // Output: 5f4dcc3b5aa765d61d8327deb882cf99
```

---

## 8. String Comparison

### `strcmp()`
Binary-safe string comparison.

```php
echo strcmp("Hello", "hello");  // Output: -1
```

---

## 9. String Tokenization

### `strtok()`
Tokenize a string.

```php
$token = strtok("Hello World!", " ");
while ($token !== false) {
    echo "$token\n";
    $token = strtok(" ");
}
```

---

## 10. String Padding

### `str_pad()`
Pad a string to a certain length.

```php
echo str_pad("Hello", 10, "-");  // Output: Hello-----
```

---

## 11. Miscellaneous

### `str_repeat()`
Repeat a string a specified number of times.

```php
echo str_repeat("Hello ", 3);  // Output: Hello Hello Hello 
```

---

## Contributing
Feel free to submit a pull request if you'd like to improve this documentation.

---

This Markdown file provides comprehensive examples for all PHP string functions, making it easy to reference and test these functions while developing.