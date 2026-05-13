<a href="https://github.com/kaamrul/codearc-php-laravel-bootcamp/stargazers"><img src="https://img.shields.io/github/stars/kaamrul/codearc-php-laravel-bootcamp" alt="Stars Badge"/></a>
<a href="https://github.com/kaamrul/codearc-php-laravel-bootcamp/network/members"><img src="https://img.shields.io/github/forks/kaamrul/codearc-php-laravel-bootcamp" alt="Forks Badge"/></a>
<a href="https://github.com/kaamrul/codearc-php-laravel-bootcamp/pulls"><img src="https://img.shields.io/github/issues-pr/kaamrul/codearc-php-laravel-bootcamp" alt="Pull Requests Badge"/></a>
<a href="https://github.com/kaamrul/codearc-php-laravel-bootcamp/issues"><img src="https://img.shields.io/github/issues/kaamrul/codearc-php-laravel-bootcamp" alt="Issues Badge"/></a>
<a href="https://github.com/kaamrul/codearc-php-laravel-bootcamp/graphs/contributors"><img alt="GitHub contributors" src="https://img.shields.io/github/contributors/kaamrul/codearc-php-laravel-bootcamp?color=2b9348"></a>
![Visitors](https://api.visitorbadge.io/api/visitors?path=https%3A%2F%2Fgithub.com%2Fkaamrul%2Fcodearc-php-laravel-bootcamp&labelColor=%23d9e3f0&countColor=%23697689&style=flat)

Don't forget to hit the :star: if you like this repo.

# 📘 PHP Operators & Expressions Full Example

```php
<?php

// ========================================
// PHP Operators & Expressions Full Example
// ========================================


// ----------------------------------------
// 1. Variable Declaration
// ----------------------------------------

$name = "Kamrul"; // String variable
$age = 25; // Integer variable
$salary = 50000; // Employee salary
$bonus = 10000; // Bonus amount
$presentDays = 24;
$totalDays = 26;


// ----------------------------------------
// 2. Arithmetic Operators
// ----------------------------------------

// Addition Operator (+)
$totalSalary = $salary + $bonus;

// Subtraction Operator (-)
$salaryAfterTax = $totalSalary - 5000;

// Multiplication Operator (*)
$yearlySalary = $totalSalary * 12;

// Division Operator (/)
$attendancePercentage = ($presentDays / $totalDays) * 100;

// Modulus Operator (%)
// Even/Odd check
$number = 8;

// Exponentiation Operator (**)
$power = 2 ** 3;


// ----------------------------------------
// 3. Increment & Decrement Operators
// ----------------------------------------

$count = 5;

$count++; // Increment by 1
$count--; // Decrement by 1


// ----------------------------------------
// 4. Assignment Operators
// ----------------------------------------

$total = 100;

$total += 50; // $total = $total + 50
$total -= 20; // $total = $total - 20
$total *= 2;  // $total = $total * 2
$total /= 5;  // $total = $total / 5


// ----------------------------------------
// 5. Comparison Operators
// ----------------------------------------

$x = 10;
$y = "10";

// Loose comparison (Only value compare)
$isEqual = ($x == $y);

// Strict comparison (Value + Data type compare)
$isIdentical = ($x === $y);

// Not equal
$isNotEqual = ($x != 20);

// Greater than
$isGreater = ($x > 5);

// Less than
$isLess = ($x < 20);

// Greater than or equal
$isGreaterOrEqual = ($x >= 10);

// Less than or equal
$isLessOrEqual = ($x <= 15);


// ----------------------------------------
// 6. Logical Operators
// ----------------------------------------

$email = true;
$password = true;

// AND Operator
$loginSuccess = ($email && $password);

// OR Operator
$isAdmin = false;
$isModerator = true;

$accessGranted = ($isAdmin || $isModerator);

// NOT Operator
$isLoggedIn = false;


// ----------------------------------------
// 7. String Concatenation Operator
// ----------------------------------------

$firstName = "Md";
$lastName = "Kamrul";

// Concatenation using .
$fullName = $firstName . " " . $lastName;


// Concatenation Assignment (.=)
$message = "Hello";
$message .= " World";


// ----------------------------------------
// 8. Array Operators
// ----------------------------------------

$array1 = [
    "name" => "Kamrul"
];

$array2 = [
    "age" => 25
];

// Union Operator
$resultArray = $array1 + $array2;


// ----------------------------------------
// 9. Conditional (Ternary) Operator
// ----------------------------------------

$studentAge = 20;

// If age >= 18 তাহলে Adult
// না হলে Minor
$status = ($studentAge >= 18) ? "Adult" : "Minor";


// ----------------------------------------
// 10. Built-in Functions
// ----------------------------------------

// String length
$stringLength = strlen($fullName);

// Convert to uppercase
$upperName = strtoupper($fullName);

// Convert to lowercase
$lowerName = strtolower($fullName);

// First letter capital
$capitalizedName = ucfirst("kamrul");

// Remove extra spaces
$trimmedText = trim("   Hello World   ");

// Current date
$currentDate = date("Y-m-d");

// Current timestamp
$currentTime = time();

// Random number
$randomNumber = rand(1, 100);

// Check string
$isString = is_string($name);

// Check integer
$isInteger = is_int($age);

// Empty check
$emptyValue = "";

$isEmpty = empty($emptyValue);

// Variable exists or not
$isSet = isset($salary);


// ----------------------------------------
// Output Section
// ----------------------------------------

echo "<h2>PHP Operators Full Example</h2>";

echo "<hr>";

echo "<h3>Arithmetic Operators</h3>";

echo "Total Salary: " . $totalSalary . "<br>";
echo "Salary After Tax: " . $salaryAfterTax . "<br>";
echo "Yearly Salary: " . $yearlySalary . "<br>";
echo "Attendance Percentage: " . $attendancePercentage . "%<br>";
echo "Power Result: " . $power . "<br>";

if ($number % 2 == 0) {
    echo $number . " is Even<br>";
} else {
    echo $number . " is Odd<br>";
}

echo "<hr>";

echo "<h3>Assignment Operators</h3>";

echo "Final Total: " . $total . "<br>";

echo "<hr>";

echo "<h3>Comparison Operators</h3>";

var_dump($isEqual);
echo "<br>";

var_dump($isIdentical);
echo "<br>";

var_dump($isNotEqual);
echo "<br>";

var_dump($isGreater);
echo "<br>";

var_dump($isLess);
echo "<br>";

echo "<hr>";

echo "<h3>Logical Operators</h3>";

if ($loginSuccess) {
    echo "Login Successful<br>";
}

if ($accessGranted) {
    echo "Access Granted<br>";
}

if (!$isLoggedIn) {
    echo "Please Login<br>";
}

echo "<hr>";

echo "<h3>String Operators</h3>";

echo "Full Name: " . $fullName . "<br>";
echo "Message: " . $message . "<br>";

echo "<hr>";

echo "<h3>Conditional Operator</h3>";

echo "Student Status: " . $status . "<br>";

echo "<hr>";

echo "<h3>Built-in Functions</h3>";

echo "String Length: " . $stringLength . "<br>";
echo "Uppercase: " . $upperName . "<br>";
echo "Lowercase: " . $lowerName . "<br>";
echo "Capitalized: " . $capitalizedName . "<br>";
echo "Trimmed Text: " . $trimmedText . "<br>";
echo "Current Date: " . $currentDate . "<br>";
echo "Current Timestamp: " . $currentTime . "<br>";
echo "Random Number: " . $randomNumber . "<br>";

echo "<br>";

echo "is_string(): ";
var_dump($isString);

echo "<br>";

echo "is_int(): ";
var_dump($isInteger);

echo "<br>";

echo "empty(): ";
var_dump($isEmpty);

echo "<br>";

echo "isset(): ";
var_dump($isSet);

?>
```



---
## 📚 অধ্যায়ের নেভিগেশন

| ⬅️ পূর্ববর্তী পাঠ | 🏠 সূচিপত্র | ➡️ পরবর্তী পাঠ |
|---|---|---|
| [ভেরিয়েবল](2.2-variables.md) | [হোম](../README.md) | [গাণিতিক বা অ্যারিথমেটিক অপারেটর](3.1-arithmetic-operators.md) |


---

## 🤝 Contribution

এই Bootcamp Repository আরও ভালো করতে আপনার যেকোনো:

- Suggestion
- Improvement Idea
- Bug Report
- Typo Fix

অত্যন্ত মূল্যবান 💖

Please create an [Issue](https://github.com/kaamrul/codearc-php-laravel-bootcamp/issues) for any improvements, suggestions, or errors in the content.

---

## 📬 Contact

You can also contact me using [LinkedIn](https://www.linkedin.com/in/kaamrul/) for any queries, collaboration, or feedback.

---

[![Visitors](https://api.visitorbadge.io/api/visitors?path=https%3A%2F%2Fgithub.com%2Fkaamrul&labelColor=%23697689&countColor=%23555555&style=plastic)](https://visitorbadge.io/status?path=https%3A%2F%2Fgithub.com%2Fkaamrul)
![](https://hit.yhype.me/github/profile?user_id=81284918)
