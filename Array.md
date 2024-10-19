Here are the **Markdown documentation files** for PHP **Array** and **Associative Array** functions, including descriptions and examples for each function.

---

# 📄 PHP Array Functions Documentation (`arrays.md`)

This file provides a list of PHP’s built-in **array functions** with descriptions and examples.

---

## **Table of Contents**
1. [Array Creation & Basic Functions](#array-creation--basic-functions)
2. [Adding & Removing Elements](#adding--removing-elements)
3. [Searching in Arrays](#searching-in-arrays)
4. [Sorting Arrays](#sorting-arrays)
5. [Array Merging & Slicing](#array-merging--slicing)
6. [Array Iteration](#array-iteration)
7. [Array Filtering & Mapping](#array-filtering--mapping)
8. [Miscellaneous](#miscellaneous)

---

## 1. Array Creation & Basic Functions

### `array()`
Create an array.

```php
$array = array(1, 2, 3);
print_r($array);
```

### `count()`
Get the number of elements in an array.

```php
echo count([1, 2, 3]);  // Output: 3
```

### `array_keys()`
Get all the keys of an array.

```php
$array = ['a' => 1, 'b' => 2];
print_r(array_keys($array));
```

### `array_values()`
Get all the values of an array.

```php
$array = ['a' => 1, 'b' => 2];
print_r(array_values($array));
```

---

## 2. Adding & Removing Elements

### `array_push()`
Add elements to the end of an array.

```php
$array = [1, 2];
array_push($array, 3, 4);
print_r($array);  // Output: [1, 2, 3, 4]
```

### `array_pop()`
Remove the last element from an array.

```php
$array = [1, 2, 3];
array_pop($array);
print_r($array);  // Output: [1, 2]
```

### `array_shift()`
Remove the first element from an array.

```php
$array = [1, 2, 3];
array_shift($array);
print_r($array);  // Output: [2, 3]
```

### `array_unshift()`
Add elements to the beginning of an array.

```php
$array = [2, 3];
array_unshift($array, 1);
print_r($array);  // Output: [1, 2, 3]
```

---

## 3. Searching in Arrays

### `in_array()`
Check if a value exists in an array.

```php
echo in_array(2, [1, 2, 3]);  // Output: 1 (true)
```

### `array_search()`
Search for a value and return its key.

```php
echo array_search(2, [1, 2, 3]);  // Output: 1
```

---

## 4. Sorting Arrays

### `sort()`
Sort an array in ascending order.

```php
$array = [3, 1, 2];
sort($array);
print_r($array);  // Output: [1, 2, 3]
```

### `rsort()`
Sort an array in descending order.

```php
$array = [1, 3, 2];
rsort($array);
print_r($array);  // Output: [3, 2, 1]
```

---

## 5. Array Merging & Slicing

### `array_merge()`
Merge two or more arrays.

```php
$array1 = [1, 2];
$array2 = [3, 4];
print_r(array_merge($array1, $array2));
```

### `array_slice()`
Extract a portion of an array.

```php
$array = [1, 2, 3, 4];
print_r(array_slice($array, 1, 2));  // Output: [2, 3]
```

---

## 6. Array Iteration

### `foreach`
Iterate over an array.

```php
$array = [1, 2, 3];
foreach ($array as $value) {
    echo $value . " ";
}
// Output: 1 2 3
```

---

## 7. Array Filtering & Mapping

### `array_filter()`
Filter the elements of an array using a callback function.

```php
$array = [1, 2, 3, 4];
$result = array_filter($array, fn($x) => $x % 2 === 0);
print_r($result);  // Output: [1 => 2, 3 => 4]
```

### `array_map()`
Apply a callback function to each element of an array.

```php
$array = [1, 2, 3];
$result = array_map(fn($x) => $x * 2, $array);
print_r($result);  // Output: [2, 4, 6]
```

---

## 8. Miscellaneous

### `array_reverse()`
Reverse the order of elements in an array.

```php
$array = [1, 2, 3];
print_r(array_reverse($array));  // Output: [3, 2, 1]
```

---

