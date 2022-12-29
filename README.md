# Validating Email Addresses with Regex

## Summary
In this tutorial, we will use regex to validate the format of email addresses. We will understand the regex string and learn how to use it to validate email addresses with JavaScript.
​
## Table of Contents
- [Introduction](#introduction)
- [Breakdown of the Regular Expression](#breakdown-of-the-regular-expression)
- [Validating Email Addresses with JavaScript](#validating-email-addresses-with-javascript)
- [Conclusion](#conclusion)
- [Author](#author)
​
## Introduction
Regular expressions, or regex, are a powerful tool for matching patterns in strings. In this tutorial, we will use this regex string to validate the format of email addresses:
​
```/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/```
​
## Breakdown of the Regular Expression
Here's a breakdown of each component:
​
- `^`: This anchor specifies that the regex should match the beginning of the string.
- `([a-z0-9_\.-]+)`: This group matches the local part of the email address, which is the part before the @ symbol. The group consists of one or more lowercase letters, digits, underscores, periods, or hyphens.
- `@`: This symbol is used to separate the local part from the domain part of the email address.
- `([\da-z\.-]+)`: This group matches the domain part of the email address, which is the part after the @ symbol. The group consists of one or more digits, lowercase letters, periods, or hyphens.
- `\.`: This period is used to separate the domain part from the top-level domain (e.g., com, edu, gov).
- `([a-z\.]{2,6})`: This group matches the top-level domain of the email address, which is the part after the period. The group consists of two to six lowercase letters or periods.
- `$`: This anchor specifies that the regex should match the end of the string.