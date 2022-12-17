# What is Hoisting

In JavaScript, "hoisting" refers to the way variable and function declarations are treated within the JavaScript interpreter. When a variable or function is declared, it is automatically moved to the top of its current scope. This means that a variableor function can be used before it is declared.

Here is an example to illustrate how hoisting works:

```javascript
console.log(x); // Output: undefined
var x = 5;
```

In the example above, the **console.log** statement is executed before the **x** variable is declared. However, because of hoisting, the interpreter automatically moves the declaration of **x** to the top of the current scope, so the **console.log** statement does not throw an error. Instead, it outputs **undefined**, because the value of **x** has not been assigned yet.

It is important to note that hoisting only affects the declarations of variables and functions, not the assignment of values. In other words, the value of **x** is not assigned until the line **var x = 5** is reached, even though the declaration of **x** is moved to the top of the current scope.

Hoisting can lead to some unexpected behavior, especially for developers who are new to JavaScript. It is a good practice to always declare variables and functions at the beginning of their respective scopes to avoid any potential confusion.

# If it is a bad practice, why was it created?

Hoisting was introduced in JavaScript as a way to make it easier for developers to write code. It allows developers to use variables and functions before they are declared, which can make the code more readable and easier to write. For example, consider the following code:

```javascript
doSomething();

function doSomething() {
  console.log("Hello, World!");
}
```

Without hoisting, this code would throw an error because the **doSomething** function is called before it is declared. However, because of hoisting, the interpreter automatically moves the declaration of the **doSomething** function to the top of the current scope, so the code runs without any errors.

While hoisting can be helpful in some cases, it can also lead to problems if it is not understood or used correctly. For example, if a developer tries to use a variable before it is declared, the interpreter will automatically move the declaration to the top of the current scope, but the variable will still be undefined until it is assigned a value. This can lead to unexpected behavior and can be difficult to debug.

To avoid these potential problems, it is generally considered a best practice to declare all variables and functions at the beginning of their respective scopes, rather than relying on hoisting to move them to the top. This can help to ensure that your code is more predictable and easier to understand.
