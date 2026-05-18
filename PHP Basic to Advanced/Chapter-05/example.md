<a href="https://github.com/kaamrul/codearc-php-laravel-bootcamp/stargazers"><img src="https://img.shields.io/github/stars/kaamrul/codearc-php-laravel-bootcamp" alt="Stars Badge"/></a>
<a href="https://github.com/kaamrul/codearc-php-laravel-bootcamp/network/members"><img src="https://img.shields.io/github/forks/kaamrul/codearc-php-laravel-bootcamp" alt="Forks Badge"/></a>
<a href="https://github.com/kaamrul/codearc-php-laravel-bootcamp/pulls"><img src="https://img.shields.io/github/issues-pr/kaamrul/codearc-php-laravel-bootcamp" alt="Pull Requests Badge"/></a>
<a href="https://github.com/kaamrul/codearc-php-laravel-bootcamp/issues"><img src="https://img.shields.io/github/issues/kaamrul/codearc-php-laravel-bootcamp" alt="Issues Badge"/></a>
<a href="https://github.com/kaamrul/codearc-php-laravel-bootcamp/graphs/contributors"><img alt="GitHub contributors" src="https://img.shields.io/github/contributors/kaamrul/codearc-php-laravel-bootcamp?color=2b9348"></a>
![Visitors](https://api.visitorbadge.io/api/visitors?path=https%3A%2F%2Fgithub.com%2Fkaamrul%2Fcodearc-php-laravel-bootcamp&labelColor=%23d9e3f0&countColor=%23697689&style=flat)

Don't forget to hit the :star: if you like this repo.




# PHP Loops & Iteration — Real Life Project Examples

এই ফাইলে আমরা PHP এর সব ধরনের Loop নিয়ে বাস্তব প্রজেক্টভিত্তিক Example দেখব।

Covered Topics:

- While Loop
- Do While Loop
- For Loop
- Foreach Loop
- Nested Loop
- Loop Control (break / continue)

---

# ১. While Loop

## Example: OTP Verification System
---

বাস্তব প্রজেক্টে User Login বা Payment Verification এর সময় OTP Verification System ব্যবহার করা হয়।

যতক্ষণ পর্যন্ত User সঠিক OTP না দেয়, ততক্ষণ পর্যন্ত সিস্টেম retry করতে দেয়।

এই ধরনের পরিস্থিতিতে `while loop` ব্যবহার করা হয়।

```php
<?php
    $otp = 1234;
    $userOtp = 1111;
    $attempt = 1;

    while ($userOtp != $otp && $attempt <= 3) {

        echo "Invalid OTP. Attempt: $attempt <br>";

        $attempt++;

        // Demo purpose এ ৩য় বারে সঠিক OTP দিচ্ছি
        if ($attempt == 3) {

            $userOtp = 1234;
        }
    }

    if ($userOtp == $otp) {
        echo "OTP Verified Successfully.";
    } else {
        echo "Account Locked.";
    }
?>
```

---

## এক্সাম্পল ডিটেইলস ও যেভাবে কাজ করবে:

- `$otp` এ আসল OTP রাখা হয়েছে
- `$userOtp` এ User এর OTP রাখা হয়েছে
- যতক্ষণ OTP ভুল থাকবে এবং attempt ৩ এর কম হবে loop চলবে
- ৩য় বারে OTP সঠিক হবে
- এরপর loop বন্ধ হয়ে success message দেখাবে

---

# ২. Do While Loop

## Example: Payment Retry System
---

বাস্তব Payment Gateway Integration এ অনেক সময় প্রথম request fail হয়।

তাই অন্তত একবার payment request পাঠিয়ে retry system তৈরি করা হয়।

এই ধরনের ক্ষেত্রে `do while loop` ব্যবহার করা হয়।

```php
<?php
    $paymentSuccess = false;
    $attempt = 1;

    do {
        echo "Processing Payment Attempt: $attempt <br>";

        // Demo: 3rd attempt এ payment success
        if ($attempt == 3) {

            $paymentSuccess = true;

        }
        $attempt++;

    } while (!$paymentSuccess && $attempt <= 5);

    if ($paymentSuccess) {
        echo "Payment Successful.";
    } else {
        echo "Payment Failed.";
    }
?>
```

---

## এক্সাম্পল ডিটেইলস ও যেভাবে কাজ করবে:

- প্রথমে payment request execute হবে
- Payment fail হলে loop আবার চলবে
- ৩য় attempt এ payment success হবে
- Success হওয়ার পর loop বন্ধ হয়ে যাবে

---

# ৩. For Loop

## Example: Bulk Email Sending System
---

বাস্তব Project এ অনেক সময় হাজার হাজার User কে Promotional Email পাঠাতে হয়।

যেহেতু আগে থেকেই জানা থাকে কতজন User আছে, তাই এখানে `for loop` ব্যবহার করা হয়।

```php
<?php
    $totalUsers = 5;

    for ($i = 1; $i <= $totalUsers; $i++) {

        echo "Sending Email to User $i <br>";
    }
?>
```

---

## এক্সাম্পল ডিটেইলস ও যেভাবে কাজ করবে:

- `$totalUsers` এ মোট User সংখ্যা রাখা হয়েছে
- Loop ১ থেকে ৫ পর্যন্ত চলবে
- প্রতিবার একটি User কে email send করবে
- সব User শেষ হলে loop বন্ধ হবে

---

# ৪. Foreach Loop

## Example: Product List Display System
---

বাস্তব E-commerce Website এ Database থেকে Product List এনে display করা হয়।

এই ধরনের ক্ষেত্রে `foreach loop` সবচেয়ে বেশি ব্যবহার করা হয়।

```php
<?php
    $products = [
        [
            "name" => "Laptop",
            "price" => 85000
        ],
        [
            "name" => "Mouse",
            "price" => 1200
        ],
        [
            "name" => "Keyboard",
            "price" => 2500
        ]
    ];

    foreach ($products as $product) {
        echo "Product: " . $product['name'] . "<br>";
        echo "Price: " . $product['price'] . " Tk <br><br>";
    }
?>
```

---

## এক্সাম্পল ডিটেইলস ও যেভাবে কাজ করবে:

- `$products` একটি Array
- প্রতিবার loop একটি Product access করবে
- Product Name এবং Price display করবে
- সব Product শেষ হলে loop বন্ধ হবে

---

# ৫. Nested Loop

## Example: Order & Product Management System
---

বাস্তব E-commerce System এ একটি Order এর মধ্যে একাধিক Product থাকে।

এই ধরনের Nested Data Handle করার জন্য Nested Loop ব্যবহার করা হয়।

```php
<?php
    $orders = [
        "ORD-1001" => [

            "Laptop",
            "Mouse"
        ],
        "ORD-1002" => [
            "Keyboard",
            "Monitor"
        ]
    ];

    foreach ($orders as $orderId => $products) {
        echo "<h3>Order ID: $orderId</h3>";

        foreach ($products as $product) {
            echo "- $product <br>";
        }
        echo "<br>";
    }
?>
```

---

## এক্সাম্পল ডিটেইলস ও যেভাবে কাজ করবে:

- বাইরের loop প্রতিবার একটি Order access করবে
- ভিতরের loop সেই Order এর Product গুলো access করবে
- প্রতিটি Order এর নিচে তার Product List দেখাবে
- সব Order শেষ হলে loop বন্ধ হবে

---

# ৬. Loop Control (break / continue)

# Break Example

## Example: Product Search System
---

বাস্তব Project এ কাঙ্ক্ষিত Product পাওয়া গেলে Search বন্ধ করে দেওয়া হয়।

```php
<?php
    $products = [
        "Laptop",
        "Mouse",
        "Keyboard"
    ];

    foreach ($products as $product) {

        if ($product == "Mouse") {
            echo "Product Found: $product";

            break;
        }

        echo "Searching... $product <br>";
    }
?>
```

---

## এক্সাম্পল ডিটেইলস ও যেভাবে কাজ করবে:

- Loop Product Search করবে
- `Mouse` পাওয়া গেলে `break` execute হবে
- এরপর loop বন্ধ হয়ে যাবে

---

# Continue Example

## Example: Out of Stock Product Skip System
---

বাস্তব Project এ Out of Stock Product skip করে Available Product display করা হয়।

```php
<?php
    $products = [
        [
            "name" => "Laptop",
            "stock" => true
        ],
        [
            "name" => "Mouse",
            "stock" => false
        ],
        [
            "name" => "Keyboard",
            "stock" => true
        ]
    ];

    foreach ($products as $product) {

        if ($product['stock'] == false) {

            continue;

        }

        echo "Available Product: " . $product['name'] . "<br>";
    }
?>
```

---

## এক্সাম্পল ডিটেইলস ও যেভাবে কাজ করবে:

- Loop প্রতিটি Product check করবে
- Out of Stock Product হলে `continue` execute হবে
- সেই iteration skip হয়ে যাবে
- শুধুমাত্র Available Product display হবে

---

# 📚 Final Summary

| Loop Type | Main Purpose |
|---|---|
| While Loop | Condition true থাকা পর্যন্ত loop চালানো |
| Do While Loop | অন্তত একবার code execute করা |
| For Loop | নির্দিষ্ট সংখ্যক iteration চালানো |
| Foreach Loop | Array/Collection এর data access করা |
| Nested Loop | Nested/Complex data handle করা |
| Break | Loop সম্পূর্ণ বন্ধ করা |
| Continue | Current iteration skip করা |

---

# 🎯 Real Life Usage

এই Loop গুলো ব্যবহার করে বাস্তব Project এ:

- Login System
- OTP Verification
- Payment Gateway
- Product Management
- Order Processing
- Email Sending
- Student Management
- Inventory System
- Report Generation
- API Data Processing

ইত্যাদি তৈরি করা হয়।





## 🤝 Contribution

এই Bootcamp Repository আরও ভালো করতে আপনার যেকোনো:

- Suggestion
- Improvement Idea
- Bug Report
- Typo Fix

অত্যন্ত মূল্যবান 💖

Please create an [Issue](https://github.com/kaamrul/codearc-php-laravel-bootcamp/issues) for any improvements, suggestions, or errors in the content.



## 📬 Contact

You can also contact me using [LinkedIn](https://www.linkedin.com/in/kaamrul/) for any queries, collaboration, or feedback.

---

[![Visitors](https://api.visitorbadge.io/api/visitors?path=https%3A%2F%2Fgithub.com%2Fkaamrul&labelColor=%23697689&countColor=%23555555&style=plastic)](https://visitorbadge.io/status?path=https%3A%2F%2Fgithub.com%2Fkaamrul)
![](https://hit.yhype.me/github/profile?user_id=81284918)