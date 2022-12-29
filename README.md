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

## Validating Email Addresses with JavaScript
To validate email addresses using JavaScript, we can create a regular expression object from the regex string and use the test() method to check if a string matches the regex:
​
```json
let regex = /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/;
​
console.log(regex.test("john.doe@example.com")); // true
console.log(regex.test("jane.doe@example.co.uk")); // true
console.log(regex.test("john.doe@example")); // false
console.log(regex.test("john.doe@.com")); // false
```
​
The first two examples will output true because the email addresses are valid. The third and fourth examples will output false because the email addresses are not valid.
​
In the third example, the domain part of the email address (example) is missing a top-level domain (e.g., com, edu, gov).
​
In the fourth example, the top-level domain (.com) is missing a domain part (e.g., example, gmail, yahoo).
​
## Conclusion
In this tutorial, we learned how to use a regular expression to match and validate email addresses. We broke down the regular expression into its different components and explained what each part does. We also demonstrated how to use the regular expression in JavaScript to validate an email address.
​
Regular expressions are a powerful tool for manipulating and searching text, and are widely used in programming languages and tools. If you want to learn more about regular expressions, here are some resources for further reading:
​
- [Regular-Expressions.info](https://www.regular-expressions.info/)
- [MDN Web Docs: Regular Expressions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions)
​
I hope this tutorial was helpful and that you now have a better understanding of how to use regular expressions to match and validate email addresses.
​
## Author
Teresa Hartsfield hartsfieldt@gmail.com (919)450-5146.
You can find more of my projects on my [GitHub Profile](https://github.com/hartsfieldt).