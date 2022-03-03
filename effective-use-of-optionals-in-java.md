
### The problems with `null`
If you are a Java developer then you must have used `null` to refer as "the absence of a value". And it might not be the case that you never got a `NullPointerException` in any of your Java program. If you have written code in Java 8 or later then you might have known that Java has introduced `java.util.Optional<T>` as an alternative to `null`. In this article I'm going to explain what is `Optional` and how you can use it effectively. But before going too far, I want you to think about the problems with using `null` and how `null` has created an useful(!) exception to a nightmare to all the existing Java developers.

I would like to mention the most common problems you may face while using `null` like the following: 

1. Null is meaningless. When an object refer to `null`, it indicates the absence of value. But it's hard to tell whether the value is actually empty (intentionally/logically) or not initialized yet or empty due to a bug in your algorithm/logic. 
2. Unncessarily null checking compromises readability by increasing nested indentations and code verbosity. 
3. Source of errors. As Java doesn't enforce null checking, so when you forget to check null-ablity of an object it may produce the annoying `NullPointerException`.
4. `null` carries no information about the intention of use - type information, if missing value is permitted or not etc,.
5. and more...

### Introduction to `Optional<T>`
Java 8 introduces a new class called java.util.Optional<T> that’s inspired by Haskell and Scala. The class may contain an optional value otherwise empty value. The intention of the Optional class isn’t to replace every single null reference rather help you design comprehensible APIs, bring better readability, and obviously help to avoid the `NullPointerException`.

Using Optionals can bring the following benefits to your code:
1. Declaring a variable of type `Optional<T>` indicates that the variable of that type may contain missing value. 
2. Enforces "null checking" by encapsulating the actual value
3. 


So, I think you have got enough reasons to use Optional, let's get your hands dirtly with few examples and step-by-step you will know effective use of Optional.

## Creating Optionals:
  * Empty optional
  * Optional with non-null value
  * Optional with null value
  
## Extracting and transforming values from Optionals: 
