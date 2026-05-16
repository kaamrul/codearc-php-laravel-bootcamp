<a href="https://github.com/kaamrul/codearc-php-laravel-bootcamp/stargazers"><img src="https://img.shields.io/github/stars/kaamrul/codearc-php-laravel-bootcamp" alt="Stars Badge"/></a>
<a href="https://github.com/kaamrul/codearc-php-laravel-bootcamp/network/members"><img src="https://img.shields.io/github/forks/kaamrul/codearc-php-laravel-bootcamp" alt="Forks Badge"/></a>
<a href="https://github.com/kaamrul/codearc-php-laravel-bootcamp/pulls"><img src="https://img.shields.io/github/issues-pr/kaamrul/codearc-php-laravel-bootcamp" alt="Pull Requests Badge"/></a>
<a href="https://github.com/kaamrul/codearc-php-laravel-bootcamp/issues"><img src="https://img.shields.io/github/issues/kaamrul/codearc-php-laravel-bootcamp" alt="Issues Badge"/></a>
<a href="https://github.com/kaamrul/codearc-php-laravel-bootcamp/graphs/contributors"><img alt="GitHub contributors" src="https://img.shields.io/github/contributors/kaamrul/codearc-php-laravel-bootcamp?color=2b9348"></a>
![Visitors](https://api.visitorbadge.io/api/visitors?path=https%3A%2F%2Fgithub.com%2Fkaamrul%2Fcodearc-php-laravel-bootcamp&labelColor=%23d9e3f0&countColor=%23697689&style=flat)

Don't forget to hit the :star: if you like this repo.

# অধ্যায় ৪: পিএইচপি কন্ট্রোল স্ট্রাকচার (PHP Control Structure)

PHP তে Conditional Control Structure ব্যবহার করা হয় প্রোগ্রামের decision making logic তৈরি করার জন্য।

এই অধ্যায়ে আমরা শিখেছি:
- ৪.১ If / Else / Elseif  
- ৪.২ Nested Conditions  
- ৪.৩ Switch Statement  
- ৪.৪ Ternary Operator  
- ৪.৫ Conditional HTML Output  
- ৪.৬ Break & Continue  

এখন আমরা এগুলো একটি **Real Life Project Scenario** দিয়ে একসাথে বুঝব।

---

# Real Life Scenario: Online Learning Platform (Role-Based System)

ধরো তুমি একটি **Online Learning Platform** বানাচ্ছো (Udemy / LMS system এর মতো)।

এখানে:
- User login করে
- User এর role থাকে (admin / teacher / student)
- Access permission আলাদা হয়
- Content dynamicভাবে দেখাতে হয়
- Data loop করে process করতে হয়

এই পুরো system এ control structure ব্যবহার করা হয়।

---

# ৪.১ If / Else / Elseif — Login & Access Check

প্রথমে user login করেছে কিনা এবং তার status check করা হয়।

```php
$isLoggedIn = true;
```

```php
if ($isLoggedIn) {
    echo "Welcome to Dashboard";
} else {
    echo "Please Login First";
}
```

👉 এখানে সিদ্ধান্ত নেওয়া হচ্ছে user login করেছে কিনা।

---

# ৪.২ Nested Condition — Role Permission System

Login করার পর user এর role check করা হয়।

```php
$isLoggedIn = true;
$role = "admin";

if ($isLoggedIn) {

    if ($role == "admin") {
        echo "Full Admin Access";
    } elseif ($role == "teacher") {
        echo "Teacher Panel Access";
    } else {
        echo "Student Access";
    }

} else {
    echo "Access Denied";
}
```

👉 এখানে এক condition এর ভিতরে আরেক condition ব্যবহার করা হয়েছে।

---

# ৪.৩ Switch Statement — Dashboard Menu Control

Role অনুযায়ী menu control করা হয়।

```php
$role = "teacher";

switch ($role) {

    case "admin":
        echo "Admin Dashboard";
        break;

    case "teacher":
        echo "Teacher Dashboard";
        break;

    case "student":
        echo "Student Dashboard";
        break;

    default:
        echo "No Access";
}
```

👉 একই variable এর multiple condition handle করা সহজ হয়।

---

# ৪.৪ Ternary Operator — Quick Status Check

User active কিনা দ্রুত check করা হয়।

```php
$isActive = true;

echo ($isActive) ? "Active User" : "Inactive User";
```

👉 ছোট condition এক লাইনে লেখা যায়।

---

# ৪.৫ Conditional HTML Output — Dynamic UI

Dashboard এ role অনুযায়ী UI show করা হয়।

```php
$userRole = "admin";
?>

<h1>Dashboard</h1>

<?php if ($userRole == "admin"): ?>
    <button>Manage Users</button>
    <button>System Settings</button>
<?php else: ?>
    <button>View Courses</button>
<?php endif; ?>
```

👉 এখানে PHP + HTML একসাথে dynamic UI তৈরি করছে।

---

# ৪.৬ Break & Continue — Data Processing System

ধরো তুমি user list process করছো।

## Continue (Banned user skip)

```php
$users = ["Rahim", "Banned", "Karim", "Jamal"];

foreach ($users as $user) {

    if ($user == "Banned") {
        continue;
    }

    echo $user . " ";
}
```

👉 banned user skip করা হলো।

---

## Break (Search stop)

```php
$users = ["Rahim", "Karim", "Jamal", "Kamal"];

foreach ($users as $user) {

    if ($user == "Jamal") {
        echo "User Found!";
        break;
    }

}
```

👉 user পেলে loop stop হয়ে যায়।

---

# 🎯 পুরো System একসাথে কীভাবে কাজ করে?

এই system এ:

- If/else → login check  
- Nested → role permission  
- Switch → dashboard routing  
- Ternary → quick status  
- Conditional HTML → UI control  
- Break/Continue → data processing  

---

# Final Real Life Flow

```
User Login
    ↓
Check Authentication (if/else)
    ↓
Check Role (nested condition)
    ↓
Load Dashboard (switch)
    ↓
Show UI (conditional HTML)
    ↓
Process Data (break/continue)
```

---

#  Conclusion

👉 Control Structure হলো একটি system এর brain  
👉 এটা ছাড়া কোনো dynamic application possible না  
👉 Real project (LMS, E-commerce, SaaS) সব জায়গায় ব্যবহার হয়  

---

# 📚 Summary

> PHP Control Structure ব্যবহার করে আমরা program এর flow control করি এবং real-world application এর decision system তৈরি করি।


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