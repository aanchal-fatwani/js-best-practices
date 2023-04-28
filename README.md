# JavaScript Best Practices

### Table of Contents

| No. | Title                                                                                                                                                         |
| --- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1   | [Minimize the use of Global Variables](#minimize-the-use-of-global-variables)                                         |
| 2   | [Always Declare Local Variables](#always-declare-local-variables)                                         |
| 3   | [Declarations should be at the top](#declarations-should-be-at-the-top)                                         |
| 4   | [Initialize variables when declared](#initialize-variables-when-declared)                                         |
| 5   | [Declare Objects and Arrays with const](#declare-objects-and-arrays-with-const)                                        |
| 6   | [Don't Use 'new' for Objects](#dont-use-new-for-objects)                                        |
| 7   | [Beware of Automatic Type Conversions](#beware-of-automatic-type-conversions)                                         |
| 8   | [Use Parameter Defaults](#use-parameter-defaults)                                         |
| 9   | [End Your Switches with Defaults](#end-your-switches-with-defaults)                                         |
| 10   | [Avoid Number, String, and Boolean as Objects](#avoid-number-string-and-boolean-as-objects)                                         |
| 11   | [Avoid Using eval](#avoid-using-eval)                                         |
| 12   | [Call things by their name](#call-things-by-their-name)                                         |
| 13   | [Stick to a strict coding style](#stick-to-a-strict-coding-style)                                         |
| 14   | [Comment as much as needed but not more](#comment-as-much-as-needed-but-not-more)                                         |
| 15   | [Avoid mixing CSS or styling with other technologies](#avoid-mixing-css-or-styling-with-other-technologies)                                         |
| 16   | [Use shortcut notation when it makes sense](#use-shortcut-notation-when-it-makes-sense)                                         |
| 17   | [Modularize — one function per task](#modularize--one-function-per-task)                                         |
| 18   | [Enhance progressively](#enhance-progressively)                                         |
| 19   | [Allow for configuration and translation](#allow-for-configuration-and-translation)                                         |
| 20   | [Avoid heavy nesting](#avoid-heavy-nesting)                                         |
| 21   | [Optimize loops](#optimize-loops)                                         |
| 22   | [Keep DOM access to a minimum](#keep-DOM-access-to-a-minimum)                                         |
| 23   | [Don’t write code specific to a certain browser](#dont-write-code-specific-to-a-certain-browser)                                         |
| 24   | [Validate data](#validate-data)                                         |
| 25   | [Avoid overloading HTML and Use Templates Instead](#avoid-overloading-html-and-use-templates-instead)                                         |
| 26   | [Make use of JS libraries](#make-use-of-js-libraries)                                         |
| 27   | [Build the code developer friendly](#build-the-code-developer-friendly)                                         |
| 28   | [Don't Use Shorthand](#dont-use-shorthand)                                         |
| 29   | [Place Scripts at the Bottom of Your Page](#place-scripts-at-the-bottom-of-your-page)                                         |
| 30   | [Declare Variables Outside of the Loops](#declare-variables-outside-of-the-loops)                                         |
| 31   | [Use native methods to Build a String](#use-native-methods-to-build-a-string)                                         |
| 32   | [Use Template Literals](#use-template-literals)                                         |
| 33   | [Don't Pass a String to setInterval or setTimeOut](#dont-pass-a-string-to-setInterval-or-setTimeOut)                                         |
| 34   | [Use {} Instead of new Object()](#use--instead-of-new-object())                                         |
| 35   | [Use [] Instead of new Array()](#use--instead-of-new-array())                                         |
| 36   | [Use the Spread Operator](#use-the-spread-operator)                                         |
| 37   | [Be Careful With for ... in Statements](#be-careful-with-for-in-statements)                                         |
| 38   | [Use Self-Executing Functions](#use-self-executing-functions)                                         |
| 39   | [Use Raw JavaScript instead of Libraries wherever possible](#use-raw-javascript-instead-of-libraries-wherever-possible)                                         |
| 40   | [Quickly Assign Variable Values With Destructuring](#quickly-assign-variable-values-with-destructuring)                                         |
| 41   | [Make use of Iterators and for ... of Loops](#make-use-of-iterators-and-for--of-loops)                                         |
| 42   | [Use async and await](#use-async-and-await)                                         |
| 43   | [Use Arrow Functions more](#use-arrow-functions-more)                                         |
| 44   | [Make use of the JavaScript includes() Method](#make-use-of-the-javascript-includes-method)                                         |
| 45   | [Run Promises in Parallel](#run-promises-in-parallel)                                         |
| 46   | [Use Regex When Extracting or Working With Strings](#use-regex-when-extracting-or-working-with-strings)                                         |
| 47   | [Put JavaScript in a Separate File](#put-javaScript-in-a-separate-file)                                         |
| 48   | [Use Splice to Remove Items From an Array](#use-splice-to-remove-items-from-an-array)                                         |
| 49   | [Incorporate Unit Testing](#incorporate-unit-testing)                                         |
| 50   | [Use Object.freeze to Create Immutable Objects](#use-objectfreeze-to-create-immutable-objects)                                         |
| 51   | [Use the Map and Set Data Structures](#use-the-map-and-set-data-structures)                                         |
| 52   | [Avoid Using InnerHTML](#avoid-using-innerhtml)                                         |
| 53   | [Use Class Syntax for Object-Oriented Programming](#use-class-syntax-for-object-oriented-programming)                                         |
| 54   | [Use the Fetch API for HTTP Requests](#use-the-fetch-api-for-http-requests)                                         |
| 55   | [Use Linters](#use-linters)                                         |


1. ### Minimize the use of Global Variables
    They can be overwritten and cause issues. Use local variables or closures instead.

      **[⬆ Back to Top](#table-of-contents)**


2. ### Always Declare Local Variables
    Undeclared variables become global variables. Use let or const to declare local variables.

      **[⬆ Back to Top](#table-of-contents)**


3. ### Declarations should be at the top
    This keeps all declarations in one place and avoids errors with re-declarations and unintended global variables.

      **[⬆ Back to Top](#table-of-contents)**


4. ### Initialize variables when declared
    This simplifies initialization and avoids undefined values.

      **[⬆ Back to Top](#table-of-contents)**


5. ### Declare Objects and Arrays with const
    This prevents accidental changes.

    **[⬆ Back to Top](#table-of-contents)**


6. ### Don't Use 'new' for Objects
    - Use "" instead of new String()
    - Use 0 instead of new Number()
    - Use false instead of new Boolean()
    - Use {} instead of new Object()
    - Use [] instead of new Array()
    - Use /()/ instead of new RegExp()
    - Use function(){} instead of new Function()

      **[⬆ Back to Top](#table-of-contents)**

      
7. ### Beware of Automatic Type Conversions
    Use === for comparison to avoid automatic type conversions.

      **[⬆ Back to Top](#table-of-contents)**


8. ### Use Parameter Defaults
    Use default values for arguments to avoid undefined values which may break code.

      **[⬆ Back to Top](#table-of-contents)**


9. ### End Your Switches with Defaults
    Always add a default case to switch statements, even if you think it's not necessary.

      **[⬆ Back to Top](#table-of-contents)**

      
10. ### Avoid Number, String, and Boolean as Objects
    Primitive values, such as numbers, strings, and booleans, should be treated as primitive data types and not as objects to optimize the execution speed and avoid side-effects.

      **[⬆ Back to Top](#table-of-contents)**

      
11. ### Avoid Using eval()
    Avoid using the eval() function, as it poses security risks by allowing arbitrary code to be executed.

      **[⬆ Back to Top](#table-of-contents)**


12. ### Call things by their name
    Use clear and easily understandable variable and function names, and avoid ambiguous or confusing names.

      **[⬆ Back to Top](#table-of-contents)**


13. ### Stick to a strict coding style
    This will help reduce the potential bugs, improve code security, and make it easier for other developers to understand the code. Avoid relying on hacks that may later become outdated as new browser versions are released.

      **[⬆ Back to Top](#table-of-contents)**


14. ### Comment as much as needed but not more
    Use commenting to provide relevant information to other developers, but only when necessary. Avoid single line comments, and instead use the /* */ notation for comments.

      **[⬆ Back to Top](#table-of-contents)**


15. ### Avoid mixing CSS or styling with other technologies
    Avoid mixing unrelated technologies, such as adding styling with JavaScript. Keep styling information inside CSS to make it easier to manage and modify the styles.

     **[⬆ Back to Top](#table-of-contents)**


16. ### Use shortcut notation when it makes sense
    Use shortcuts like object literals, ternary notations, and || notation, whenever possible, to optimize code.
    
     **[⬆ Back to Top](#table-of-contents)**


17. ### Modularize — one function per task
    Break down tasks into smaller functions, and create helper functions for repetitive tasks, which makes the code smaller, manageable, and easy to debug.
    
     **[⬆ Back to Top](#table-of-contents)**


18. ### Enhance progressively
    Write code that works even when certain technologies are unavailable, like scripting(for non-JS browsers). This enhances the functionality of your webpage or web product.

    **[⬆ Back to Top](#table-of-contents)**


19. ### Allow for configuration and translation
    Use a configuration object to contain parameters that are likely to change so that it is easier to maintain the code in the future. 
    
    **[⬆ Back to Top](#table-of-contents)**


20. ### Avoid heavy nesting
    Avoid excessive nesting in your code, use generic functions instead, and aim for code that is easy to read and understand.

    Another issue with nesting is variable names and loops. Starting with 'i' as the iterator and moving on to 'j', 'k', 'l', and beyond can quickly get messy. Use descriptive variable names to avoid confusion.

    **[⬆ Back to Top](#table-of-contents)**


21. ### Optimize loops
    Optimize loops by storing the length attribute of an array in a variable to avoid recalculating it on every iteration. Keep computation-heavy code outside of loops to improve performance.
  
    **[⬆ Back to Top](#table-of-contents)**


22. ### Keep DOM access to a minimum
    Reduce DOM access since it is costly and can slow down the performance of your code. Use a tool function to transform a string to DOM elements to improve the code's speed.

    **[⬆ Back to Top](#table-of-contents)**


23. ### Don’t write code specific to a certain browser
    Avoid over-dependence on any specific browser or its features while building your code, and use standards-based code. Otherwise, your code would become obsolete when the browser updates or a new browser is introduced.

    **[⬆ Back to Top](#table-of-contents)**


24. ### Validate data
    Avoid relying on invalid data, validate it before using it to avoid glitches and security threats. Do not solely depend on client-side validation, as it can create security vulnerabilities.

    **[⬆ Back to Top](#table-of-contents)**


25. ### Avoid Overloading HTML and Use Templates Instead
    Use an HTML template and load it via Ajax instead of manipulating a document with innerHTML, which can cause flakiness, especially with certain browsers.

    **[⬆ Back to Top](#table-of-contents)**


26. ### Make use of JS libraries
    Use a JS library to develop web applications since the code would have fewer issues and reduce the number of bugs while maintaining the standards.

    **[⬆ Back to Top](#table-of-contents)**


27. ### Build the code developer friendly
    Do not optimize code for machines and focus on making it easy to understand for other developers. Use the build script to optimize the code for machine use.

    **[⬆ Back to Top](#table-of-contents)**


28. ### Don't Use Shorthand
    Avoid using shorthand, which can be confusing, especially in edge cases. Use curly braces and semi-colons, so the logic and functionality are clear to other developers.

    **[⬆ Back to Top](#table-of-contents)**


29. ### Place Scripts at the Bottom of Your Page
    To reduce page loading time, place scripts at the bottom, especially those that add functionality after the user clicks a button.

    **[⬆ Back to Top](#table-of-contents)**


30. ### Declare Variables Outside of the Loops
    This will help avoid making the engine work any harder than it needs to.

    **[⬆ Back to Top](#table-of-contents)**


31. ### Use native methods to Build a String
    Use native methods like join() instead of a for statement when looping through arrays to make your code faster.

    **[⬆ Back to Top](#table-of-contents)**


32. ### Use Template Literals
    Use template literals instead of traditional strings since they are more flexible and easier to work with.

    **[⬆ Back to Top](#table-of-contents)**


33. ### Don't Pass a String to setInterval or setTimeOut
    Instead, pass a function name to avoid inefficient code and reduce the chances of errors. 

    **[⬆ Back to Top](#table-of-contents)**


34. ### Use {} Instead of new Object()
    Use object literals instead of the new constructor method to create objects in JavaScript since it is a more straightforward process.

    **[⬆ Back to Top](#table-of-contents)**


35. ### Use [] Instead of new Array()
    Use [] to create a new array instead of the new Array() constructor to improve code readability.

    **[⬆ Back to Top](#table-of-contents)**


36. ### Use the Spread Operator
    Use the spread operator (...) to insert all values from one array into another or pass all items of an array as individual elements to another function.

    **[⬆ Back to Top](#table-of-contents)**


37. ### Be Careful With for ... in Statements
    When using a for...in loop to loop through an object, filter out method functions (such as hasOwnProperty) and other inherited properties by wrapping the code in an if statement.

    **[⬆ Back to Top](#table-of-contents)**


38. ### Use Self-Executing Functions
    Make use of self-executing functions to run a function automatically when a page loads or a parent function is called.

    **[⬆ Back to Top](#table-of-contents)**


39. ### Use Raw JavaScript instead of Libraries wherever possible
    Libraries can save time but raw JavaScript is always faster.

    **[⬆ Back to Top](#table-of-contents)**


40. ### Quickly Assign Variable Values With Destructuring
    This allows us to avoid variable assignments for values we don't need.

    **[⬆ Back to Top](#table-of-contents)**


41. ### Make use of Iterators and for ... of Loops
    Iterators in JavaScript are objects which implement the next() method to return an object that stores the next value in a sequence and true or false depending on whether or not there are any more values left. JavaScript also has some built-in iterators like String, Array, Map, etc. You can iterate over them using for ... of loops. 
    
    Use iterators and for...of loops for more concise and less error-prone code.


    **[⬆ Back to Top](#table-of-contents)**


42. ### Use async and await
    Asynchronous functions can be created with the async keyword and take advantage of the await keyword to stop execution until the resolution of returned promises.

    **[⬆ Back to Top](#table-of-contents)**


43. ### Use Arrow Functions more
    Use arrow functions for more readable and concise functional JavaScript code.

    Another notable benefit of arrow functions is that they do not define a scope, instead being within the parent scope. This prevents many of the issues that can occur when using the this keyword. There are no bindings for this in the arrow functions. 'this' has the same value inside the arrow function as it does in the parent scope. However, this means arrow functions can't be used as constructors or methods.

    **[⬆ Back to Top](#table-of-contents)**


44. ### Make use of the Javascript includes() Method
    Use the includes() method to check if a string contains certain characters or if an array contains a specific element.

    **[⬆ Back to Top](#table-of-contents)**


45. ### Run Promises in Parallel
    Run asynchronous tasks in parallel using Promise.all(). It can make the app much faster and more responsive. 

    **[⬆ Back to Top](#table-of-contents)**


46. ### Use Regex When Extracting or Working With Strings
    Use regex instead of complicated string manipulation methods like indexOf() and substring().

    **[⬆ Back to Top](#table-of-contents)**


47. ### Put JavaScript in a Separate File
    Keeping JavaScript in a separate file makes it more organized, reusable, and easier for web browsers to cache.

    **[⬆ Back to Top](#table-of-contents)**


48. ### Use Splice to Remove Items From an Array
    Use splice() to remove elements from an array instead of the delete method.

    **[⬆ Back to Top](#table-of-contents)**


49. ### Incorporate Unit Testing
    Unit testing is essential for ensuring quality code and saving time and money during the development process.

    **[⬆ Back to Top](#table-of-contents)**


50. ### Use Object.freeze to Create Immutable Objects
    Use Object.freeze() to create immutable objects which can't be modified or deleted. This can prevent bugs and improve performance.
    
    **[⬆ Back to Top](#table-of-contents)**

    
51. ### Use the Map and Set Data Structures
    The Map and Set data structures are powerful tools for handling data in JavaScript. They allow you to store data in key-value pairs and unique values, respectively. Use them where appropriate to simplify your code and improve performance. 
    
    **[⬆ Back to Top](#table-of-contents)**


52. ### Avoid Using InnerHTML
    Avoid using innerHTML to modify the content of your web pages. This feature can cause unexpected behavior and security vulnerabilities, so use the DOM manipulation methods provided by the browser instead. 
    
    **[⬆ Back to Top](#table-of-contents)**


53. ### Use Class Syntax for Object-Oriented Programming
    JavaScript class syntax provides a more familiar and structured approach to object-oriented programming. Use it where appropriate to simplify your code and make it more readable.
    
    **[⬆ Back to Top](#table-of-contents)**


54. ### Use the Fetch API for HTTP Requests
    The Fetch API is a modern and powerful way to make HTTP requests in JavaScript. Use it instead of older and less secure techniques like XMLHttpRequest.

    **[⬆ Back to Top](#table-of-contents)**


55. ### Use Linters
    Linters help ensure that your code follows best practices and style guidelines. Use a linter like ESLint to catch errors and enforce standards.

    **[⬆ Back to Top](#table-of-contents)**