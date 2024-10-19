---

# 📄 PHP Associative Array Functions Documentation (`associative_arrays.md`)

This file focuses on **associative arrays** and the functions used to manipulate them.

---

## **Table of Contents**
1. [Creating Associative Arrays](#creating-associative-arrays)
2. [Accessing Values](#accessing-values)
3. [Modifying Arrays](#modifying-arrays)
4. [Sorting Associative Arrays](#sorting-associative-arrays)
5. [Checking Keys and Values](#checking-keys-and-values)
6. [Converting Arrays](#converting-arrays)

---

## 1. Creating Associative Arrays

### `array()`
Create an associative array.

```php
$person = ["name" => "John", "age" => 30];
print_r($person);
```

---

## 2. Accessing Values

### Access by Key

```php
$person = ["name" => "John", "age" => 30];
echo $person["name"];  // Output: John
```

---

## 3. Modifying Arrays

### Add or Update Elements

```php
$person = ["name" => "John"];
$person["age"] = 30;
print_r($person);  // Output: ["name" => "John", "age" => 30]
```

### Remove Elements with `unset()`

```php
unset($person["age"]);
print_r($person);  // Output: ["name" => "John"]
```

---

## 4. Sorting Associative Arrays

### `asort()`
Sort by values while preserving keys.

```php
$array = ["a" => 3, "b" => 1, "c" => 2];
asort($array);
print_r($array);  // Output: ["b" => 1, "c" => 2, "a" => 3]
```

### `ksort()`
Sort by keys.

```php
$array = ["b" => 1, "a" => 2];
ksort($array);
print_r($array);  // Output: ["a" => 2, "b" => 1]
```

---

## 5. Checking Keys and Values

### `array_key_exists()`
Check if a key exists in an array.

```php
$array = ["name" => "John"];
echo array_key_exists("name", $array);  // Output: 1 (true)
```

### `isset()`
Check if a key is set and not null.

```php
$array = ["name" => "John", "age" => null];
var_dump(isset($array["name"]));  // Output: bool(true)
var_dump(isset($array["age"]));   // Output: bool(false)
```

---

## 6. Converting Arrays

### `array_flip()`
Swap keys and values.

```php
$array = ["a" => 1, "b" => 2];
print_r(array_flip($array));  // Output: [1 => "a", 2 => "b"]
```

---

Feel free to submit pull requests if you'd like to improve this documentation.

---

These two files cover the **array functions** and **associative array functions** with clear examples. You can upload these as `arrays.md` and `associative_arrays.md` to your GitHub repository.