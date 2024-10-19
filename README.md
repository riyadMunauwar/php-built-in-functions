---

# 📄 PHP Built-in Function Documentation Templates  

Below are example Markdown files for:

1. **Math Functions**
2. **Date and Time Functions**
3. **Filesystem Functions**
4. **Error Handling Functions**
5. **Session Management Functions**

---

## 1. **PHP Math Functions Documentation (`math_functions.md`)**

```markdown
# 📄 PHP Math Functions Documentation

This document provides a list of PHP’s built-in math functions with descriptions and examples.

---

## **Table of Contents**
1. [Basic Math Functions](#basic-math-functions)
2. [Random Numbers](#random-numbers)
3. [Trigonometric Functions](#trigonometric-functions)
4. [Advanced Math Functions](#advanced-math-functions)

---

## 1. Basic Math Functions

### `abs()`
Returns the absolute value of a number.

```php
echo abs(-5);  // Output: 5
```

### `pow()`
Returns the power of a number.

```php
echo pow(2, 3);  // Output: 8
```

### `sqrt()`
Returns the square root of a number.

```php
echo sqrt(16);  // Output: 4
```

---

## 2. Random Numbers

### `rand()`
Generate a random integer.

```php
echo rand(1, 10);  // Output: Random number between 1 and 10
```

---

## 3. Trigonometric Functions

### `sin()`
Returns the sine of a number (in radians).

```php
echo sin(pi() / 2);  // Output: 1
```

---

## 4. Advanced Math Functions

### `log()`
Returns the natural logarithm of a number.

```php
echo log(10);  // Output: 2.302585...
```
```

---

## 2. **PHP Date and Time Functions Documentation (`date_time_functions.md`)**

```markdown
# 📄 PHP Date and Time Functions Documentation

This document provides examples and explanations for PHP’s date and time functions.

---

## **Table of Contents**
1. [Getting the Current Date and Time](#getting-the-current-date-and-time)
2. [Formatting Dates](#formatting-dates)
3. [Timezones](#timezones)
4. [Date Differences](#date-differences)

---

## 1. Getting the Current Date and Time

### `date()`
Formats a local date and time.

```php
echo date("Y-m-d H:i:s");  // Output: 2024-10-19 14:30:00
```

---

## 2. Formatting Dates

### `strtotime()`
Parse a time string into a timestamp.

```php
echo date("Y-m-d", strtotime("next Sunday"));  // Output: 2024-10-20
```

---

## 3. Timezones

### `date_default_timezone_set()`
Set the default timezone.

```php
date_default_timezone_set("Asia/Dhaka");
echo date("H:i:s");  // Output: Current time in Dhaka
```

---

## 4. Date Differences

### `date_diff()`
Calculate the difference between two dates.

```php
$date1 = date_create("2024-10-19");
$date2 = date_create("2024-12-25");
$diff = date_diff($date1, $date2);
echo $diff->format("%R%a days");  // Output: +67 days
```
```

---

## 3. **PHP Filesystem Functions Documentation (`filesystem_functions.md`)**

```markdown
# 📄 PHP Filesystem Functions Documentation

This document provides a list of filesystem functions used to manage files and directories in PHP.

---

## **Table of Contents**
1. [Reading and Writing Files](#reading-and-writing-files)
2. [Directory Management](#directory-management)
3. [File Properties](#file-properties)

---

## 1. Reading and Writing Files

### `file_get_contents()`
Reads the contents of a file into a string.

```php
$content = file_get_contents("example.txt");
echo $content;
```

### `file_put_contents()`
Writes data to a file.

```php
file_put_contents("example.txt", "Hello World!");
```

---

## 2. Directory Management

### `mkdir()`
Create a new directory.

```php
mkdir("new_directory");
```

### `rmdir()`
Remove an empty directory.

```php
rmdir("new_directory");
```

---

## 3. File Properties

### `file_exists()`
Check if a file exists.

```php
if (file_exists("example.txt")) {
    echo "File exists.";
}
```
```

---

## 4. **PHP Error Handling Functions Documentation (`error_handling_functions.md`)**

```markdown
# 📄 PHP Error Handling Functions Documentation

This document lists PHP’s error handling functions with examples.

---

## **Table of Contents**
1. [Basic Error Handling](#basic-error-handling)
2. [Custom Error Handlers](#custom-error-handlers)
3. [Exception Handling](#exception-handling)

---

## 1. Basic Error Handling

### `error_reporting()`
Set the error reporting level.

```php
error_reporting(E_ALL);
```

---

## 2. Custom Error Handlers

### `set_error_handler()`
Define a custom error handler.

```php
set_error_handler(function($errno, $errstr) {
    echo "Error: [$errno] $errstr";
});
```

---

## 3. Exception Handling

### `try...catch` Block
Handle exceptions.

```php
try {
    throw new Exception("Something went wrong!");
} catch (Exception $e) {
    echo $e->getMessage();
}
```
```

---

## 5. **PHP Session Management Functions Documentation (`session_management.md`)**

```markdown
# 📄 PHP Session Management Functions Documentation

This document covers PHP’s session functions with examples.

---

## **Table of Contents**
1. [Starting Sessions](#starting-sessions)
2. [Managing Session Variables](#managing-session-variables)
3. [Destroying Sessions](#destroying-sessions)

---

## 1. Starting Sessions

### `session_start()`
Start a new session or resume an existing one.

```php
session_start();
```

---

## 2. Managing Session Variables

### `$_SESSION` Superglobal
Store and access session variables.

```php
$_SESSION["username"] = "John";
echo $_SESSION["username"];  // Output: John
```

---

## 3. Destroying Sessions

### `session_destroy()`
Destroy the session and clear session data.

```php
session_destroy();
```
```

---

### Conclusion

You can copy each of these Markdown templates to individual files (`math_functions.md`, `date_time_functions.md`, etc.) in your GitHub repository. This ensures all major PHP built-in function categories are well-documented for easy reference and understanding.