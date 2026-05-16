<a href="https://github.com/kaamrul/codearc-php-laravel-bootcamp/stargazers"><img src="https://img.shields.io/github/stars/kaamrul/codearc-php-laravel-bootcamp" alt="Stars Badge"/></a>
<a href="https://github.com/kaamrul/codearc-php-laravel-bootcamp/network/members"><img src="https://img.shields.io/github/forks/kaamrul/codearc-php-laravel-bootcamp" alt="Forks Badge"/></a>
<a href="https://github.com/kaamrul/codearc-php-laravel-bootcamp/pulls"><img src="https://img.shields.io/github/issues-pr/kaamrul/codearc-php-laravel-bootcamp" alt="Pull Requests Badge"/></a>
<a href="https://github.com/kaamrul/codearc-php-laravel-bootcamp/issues"><img src="https://img.shields.io/github/issues/kaamrul/codearc-php-laravel-bootcamp" alt="Issues Badge"/></a>
<a href="https://github.com/kaamrul/codearc-php-laravel-bootcamp/graphs/contributors"><img alt="GitHub contributors" src="https://img.shields.io/github/contributors/kaamrul/codearc-php-laravel-bootcamp?color=2b9348"></a>
![Visitors](https://api.visitorbadge.io/api/visitors?path=https%3A%2F%2Fgithub.com%2Fkaamrul%2Fcodearc-php-laravel-bootcamp&labelColor=%23d9e3f0&countColor=%23697689&style=flat)

Don't forget to hit the :star: if you like this repo.

# অধ্যায় ৩: পিএইচপি কন্ট্রোল স্ট্রাকচার (PHP Control Structure)


পিএইচপি **কন্ট্রোল স্ট্রাকচার (Control Structure)** হলো এমন কিছু প্রোগ্রামিং কাঠামো ও নির্দেশনার সমষ্টি, যার মাধ্যমে একটি প্রোগ্রামের কার্যপ্রবাহ নিয়ন্ত্রণ ও পরিচালনা করা হয়। এটি নির্ধারণ করে কোন নির্দেশ কখন কার্যকর হবে, কোন শর্তে চলবে, কতবার পুনরাবৃত্তি হবে এবং কোন পরিস্থিতিতে কার্যপ্রবাহ পরিবর্তিত হবে। কন্ট্রোল স্ট্রাকচার ব্যবহার করে একটি সাধারণ প্রোগ্রামকে যৌক্তিক, গতিশীল, কার্যকর এবং ব্যবহারকারীর প্রয়োজন অনুযায়ী পরিচালনাযোগ্য করা সম্ভব হয়। 

প্রোগ্রাম তৈরির সময় বিভিন্ন পরিস্থিতিতে ভিন্ন ভিন্ন সিদ্ধান্ত গ্রহণের প্রয়োজন হয়। যেমন— কোনো শর্ত সত্য হলে একটি কাজ সম্পাদন করা, মিথ্যা হলে অন্য কাজ করা, অথবা একই কাজ বারবার চালানো। এসব কাজ সম্পাদনের জন্য কন্ট্রোল স্ট্রাকচার ব্যবহৃত হয়। এর মাধ্যমে প্রোগ্রামের ভেতরে সিদ্ধান্ত গ্রহণ, পুনরাবৃত্তি, এবং কার্যপ্রবাহ নিয়ন্ত্রণের মতো গুরুত্বপূর্ণ কাজ সম্পন্ন করা যায়।

পিএইচপি কন্ট্রোল স্ট্রাকচারের মধ্যে শর্তভিত্তিক নির্দেশনা, পুনরাবৃত্তিমূলক কাঠামো এবং কার্যপ্রবাহ পরিবর্তনকারী নির্দেশনা অন্তর্ভুক্ত রয়েছে। এগুলোর সাহায্যে একটি প্রোগ্রামকে আরও বুদ্ধিমান, সংগঠিত এবং দক্ষভাবে পরিচালনা করা সম্ভব হয়।

সহজভাবে বলতে গেলে:

```
সংক্ষেপে বলা যায়, পিএইচপি কন্ট্রোল স্ট্রাকচার হলো এমন একটি ব্যবস্থা, যা একটি প্রোগ্রামের চলার ধারা নিয়ন্ত্রণ করে এবং প্রয়োজন অনুযায়ী সিদ্ধান্ত গ্রহণ ও পুনরাবৃত্তিমূলক কাজ সম্পাদন করতে সহায়তা করে।
```

### উদাহরণ

পিএইচপি কন্ট্রোল স্ট্রাকচার এর অন্তর্ভুক্ত:

<table>
  <thead>
    <tr>
      <th>গ্রুপ</th>
      <th>নির্দেশনা</th>
      <th>বর্ণনা</th>
    </tr>
  </thead>

  <tbody>
    <!-- Conditional Statements -->
    <tr>
      <td rowspan="2"><b>Conditional Statements</b></td>
      <td>if/else</td>
      <td>একটি শর্ত যাচাই করে। শর্ত সত্য হলে নির্দিষ্ট কোড কার্যকর হয়, আর মিথ্যা হলে else অংশের কোড কার্যকর হয়।</td>
    </tr>
    <tr>
      <td>switch</td>
      <td>একটি মান যাচাই করে এবং সেই মান অনুযায়ী বিভিন্ন কোড ব্লকের মধ্যে নির্দিষ্ট কোড কার্যকর করে।</td>
    </tr>

    <!-- Loop Statements -->
    <tr>
      <td rowspan="4"><b>Loop Statements</b></td>
      <td>for</td>
      <td>নির্দিষ্ট সংখ্যক বার একটি কোড ব্লক চালায়। এটি শুরু মান, শেষ মান এবং ধাপের মানের উপর ভিত্তি করে কাজ করে।</td>
    </tr>
    <tr>
      <td>while</td>
      <td>যতক্ষণ নির্দিষ্ট শর্ত সত্য থাকে, ততক্ষণ কোড বারবার কার্যকর হয়।</td>
    </tr>
    <tr>
      <td>do...while</td>
      <td>প্রথমে একবার কোড কার্যকর করে, তারপর শর্ত সত্য থাকলে পুনরায় কোড চালাতে থাকে।</td>
    </tr>
    <tr>
      <td>foreach</td>
      <td>একটি অ্যারে বা সংগ্রহের প্রতিটি উপাদানের উপর পর্যায়ক্রমে কাজ করে এবং প্রতিটির জন্য নির্দিষ্ট কোড কার্যকর করে।</td>
    </tr>

    <!-- Flow Control Statements -->
    <tr>
      <td rowspan="4"><b>Flow Control Statements</b></td>
      <td>break</td>
      <td>কোনো লুপ বা switch নির্দেশনার কার্যক্রম তাৎক্ষণিকভাবে বন্ধ করে দেয়।</td>
    </tr>
    <tr>
      <td>continue</td>
      <td>বর্তমান ধাপটি বাদ দিয়ে লুপের পরবর্তী ধাপে চলে যায়।</td>
    </tr>
    <tr>
      <td>return</td>
      <td>একটি ফাংশনের কার্যক্রম শেষ করে এবং প্রয়োজন হলে একটি মান ফেরত পাঠায়।</td>
    </tr>
    <tr>
      <td>throw</td>
      <td>একটি ব্যতিক্রম সৃষ্টি করে, যা পরে ব্যতিক্রম ব্যবস্থাপনার মাধ্যমে ধরা ও পরিচালনা করা যায়।</td>
    </tr>
  </tbody>
</table>

এগুলোর মাধ্যমে একটি প্রোগ্রামকে যৌক্তিক, গতিশীল এবং কার্যকরভাবে পরিচালনা করা যায়।



## PHP তে মোট কয়েক ধরনের Operator আছে

PHP তে প্রধানত নিচের Operator গুলো সবচেয়ে বেশি ব্যবহার হয়ঃ

- **[৩.১ অ্যারিথমেটিক বা গাণিতিক অপারেটর (Arithmetic Operators)](3.1-arithmetic-operators.md)**
- **[৩.২ ইনক্রিমেন্ট ও ডিক্রিমেন্ট অপারেটর (Increment & Decrement)](3.2-increment-decrement-operators.md)**
- **[৩.৩ অ্যাসাইনমেন্ট অপারেটর (Assignment Operators)](3.3-assignment-operators.md)**
- **[৩.৪ কম্পারিজন বা তুলনামূলক অপারেটর (Comparison Operators)](3.4-comparisaon-operators.md)**
- **[৩.৫ লজিক্যাল বা যৌক্তিক অপারেটর (Logical Operators)](3.5-logical-operators.md)**
- **[৩.৬ স্ট্রিং অপারেটর: কনক্যাটিনেশন বনাম ইন্টারপোলেশন (String operators)](3.6-string-operators.md)**
- **[৩.৭ অ্যারে অপারেটর (Array Operators)](3.7-array-operators.md)**
- **[৩.৮ শর্তাধীন/ত্রয়ী অপারেটর (Conditional/Ternary Operator)](3.8-conditional-operators.md)**
- **[৩.৯ বিল্ট-ইন ফাংশন এবং ডেটা হ্যান্ডলিং (Built-in Function and Data Handling)](3.9-built-in-functions.md)**


## কেন Operators & Expressions গুরুত্বপূর্ণ?

অপারেটর এবং এক্সপ্রেশন শুধু গাণিতিক হিসাব নয়, বরং কোডের লজিক্যাল আর্কিটেকচার তৈরির প্রধান হাতিয়ার। 

আধুনিক পিএইচপি-র নতুন অপারেটরগুলো (যেমন ?-> বা ??) কোডকে অনেক বেশি ক্লিন এবং এরর-মুক্ত রাখতে সাহায্য করে। 

একজন লারাভেল ডেভেলপার হিসেবে এই অপারেটরগুলোর সঠিক অগ্রাধিকার এবং সিকিউরিটি ইমপ্লিকেশন জানা অত্যন্ত জরুরি।



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
