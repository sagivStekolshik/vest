# Enforce - n4s

Enforce is a validations assertions library. It provides rules that you can test your data against.

By default, enforce throws an error when your validations fail. These errors should be caught by a validation testing framework such as [Vest](https://github.com/ealush/vest).

You can extend Enforce per need, and you can add your custom validation rules in your app.

```js
import enforce from 'n4s';

enforce(4).isNumber();
// passes

enforce(4).isNumber().greaterThan(2);
// passes

enforce(4)
  .lessThan(2) // throws an error, will not carry on to the next rule
  .greaterThan(3);
```

## Installation

```
npm i n4s
```

## Using enforce without a testing framework

If you wish to use enforce's functionality without it throwing errors, you can use its [ensure](./ensure) interface.

## Content

- [List of Enforce rules](./rules)
- [Business reated rules](./business_rules)
- [Custom Enforce Rules](./custom)
- [Non throwing validations (ensure)](./ensure)
