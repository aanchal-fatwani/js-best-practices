# JavaScript Best Practices

### Table of Contents

| No. | Title                                                                                                                                                         |
| --- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1   | [Minimize the use of Global Variables and Functions](#minimize-the-use-of-global-variables-and-functions)                                         |
| 2   | [Always Declare Local Variables](#always-declare-local-variables)                                         |
| 3   | [Declarations should be at the top](#declarations-should-be-at-the-top)                                         |
| 4   | [Initialize variables when declared](#initialize-variables-when-declared)                                         |
| 5   | [Declare Objects and Arrays with const](#declare-objects-and-arrays-with-const)                                        |
| 6   | [Don't Use 'new' for Objects](#dont-use-new-for-objects)                                        |
| 7   | [Beware of Automatic Type Conversions](#beware-of-automatic-type-conversions)                                         |
| 8   | [Use Parameter Defaults](#use-parameter-defaults)                                         |
| 9   | [End Your Switches with Defaults](#end-your-switches-with-defaults)                                         |
| 10   | [Use Static Types with TypeScript or Flow](#use-static-types-with-typescript-or-flow) |
| 11   | [Avoid Using eval](#avoid-using-eval)                                         |
| 12   | [Call things by their name](#call-things-by-their-name)                                         |
| 13   | [Stick to a strict coding style](#stick-to-a-strict-coding-style)                                         |
| 14   | [Comment as much as needed but not more](#comment-as-much-as-needed-but-not-more)                                         |
| 15   | [Avoid mixing CSS or styling with other technologies](#avoid-mixing-css-or-styling-with-other-technologies)                                         |
| 16   | [Use shortcut notation when it makes sense](#use-shortcut-notation-when-it-makes-sense)                                         |
| 17   | [Modularize - one function per task](#modularize---one-function-per-task)                                         |
| 18   | [Enhance progressively](#enhance-progressively)                                         |
| 19   | [Allow for configuration and translation](#allow-for-configuration-and-translation)                                         |
| 20   | [Avoid heavy nesting](#avoid-heavy-nesting)                                         |
| 21   | [Optimize loops](#optimize-loops)                                         |
| 22   | [Keep DOM access to a minimum](#keep-dom-access-to-a-minimum)                                         |
| 23   | [Don’t write code specific to a certain browser](#dont-write-code-specific-to-a-certain-browser)                                         |
| 24   | [Validate data](#validate-data)                                         |
| 25   | [Avoid overloading HTML and Use Templates Instead](#avoid-overloading-html-and-use-templates-instead)                                         |
| 26   | [Carefully decide to make use of JS libraries or work with raw JS](#carefully-decide-to-make-use-of-js-libraries-or-work-with-raw-js)                                      |
| 27   | [Build the code developer friendly](#build-the-code-developer-friendly)                                         |
| 28   | [Don't Use Shorthand](#dont-use-shorthand)                                         |
| 29   | [Place Scripts at the Bottom of Your Page](#place-scripts-at-the-bottom-of-your-page)                                         |
| 30   | [Declare Variables and Functions Outside of the Loops](#declare-variables-and-functions-outside-of-the-loops)                                         |
| 31   | [Use native methods to Build a String](#use-native-methods-to-build-a-string)                                         |
| 32   | [Use Template Literals](#use-template-literals)                                         |
| 33   | [Don't Pass a String to setInterval or setTimeOut](#dont-pass-a-string-to-setinterval-or-settimeout)                                         |
| 34   | [Use object literals and arrays instead of constructors](#use-object-literals-and-arrays-instead-of-constructors)                                         |
| 35   | [Use SetTimeout instead of SetInterval](#use-settimeout-instead-of-setinterval) |
| 36   | [Use the Spread Operator](#use-the-spread-operator)                                         |
| 37   | [Be Careful With for ... in Statements](#be-careful-with-for--in-statements)                                         |
| 38   | [Use Self-Executing Functions](#use-self-executing-functions)                                         |
| 39   | [Use Event Emitters instead of Callbacks](#use-event-emitters-instead-of-callbacks) |
| 40   | [Quickly Assign Variable Values With Destructuring](#quickly-assign-variable-values-with-destructuring)                                         |
| 41   | [Make use of Iterators and for ... of Loops](#make-use-of-iterators-and-for--of-loops)                                         |
| 42   | [Use async and await](#use-async-and-await)                                         |
| 43   | [Use Arrow Functions more](#use-arrow-functions-more)                                         |
| 44   | [Make use of the JavaScript includes() Method](#make-use-of-the-javascript-includes-method)                                         |
| 45   | [Run Promises in Parallel](#run-promises-in-parallel)                                         |
| 46   | [Use Regex When Extracting or Working With Strings](#use-regex-when-extracting-or-working-with-strings)                                         |
| 47   | [Put JavaScript in a Separate File](#put-javascript-in-a-separate-file)                                         |
| 48   | [Use Splice to Remove Items From an Array](#use-splice-to-remove-items-from-an-array)                                         |
| 49   | [Incorporate Testing](#incorporate-testing)                                         |
| 50   | [Use Object.freeze to Create Immutable Objects](#use-objectfreeze-to-create-immutable-objects)                                         |
| 51   | [Use the Map and Set Data Structures](#use-the-map-and-set-data-structures)                                         |
| 52   | [Avoid Using InnerHTML](#avoid-using-innerhtml)                                         |
| 53   | [Use Class Syntax for Object-Oriented Programming](#use-class-syntax-for-object-oriented-programming)                                         |
| 54   | [Use the Fetch API for HTTP Requests](#use-the-fetch-api-for-http-requests)                                         |
| 55   | [Use Linters](#use-linters)                                         |
| 56   | [Use the Proxy Object to Intercept Object Operations](#use-the-proxy-object-to-intercept-object-operations) |
| 57   | [Use Server-Side Rendering for Improved Performance](#use-server-side-rendering-for-improved-performance)                                         |
| 58   | [Use Event Delegation](#use-event-delegation)                                         |
| 59   | [Use Memoization to Improve Performance](#use-memoization-to-improve-performance)                                         |
| 60   | [Use Web Workers](#use-web-workers)                                         |
| 61   | [Use the Object.assign Method for Object Composition](#use-the-objectassign-method-for-object-composition)                                                 |
| 62   | [Use Web Components for Reusable UI Elements](#use-web-components-for-reusable-ui-elements)                                                 |
| 63   | [Use the DRY (Don't Repeat Yourself) Principle](#use-the-dry-dont-repeat-yourself-principle)                                                 |
| 64   | [Use Error Handling](#use-error-handling)                                                 |
| 65   | [Use Web Storage API for Data Storage](#use-web-storage-api-for-data-storage)                                                 |
| 66   | [Use Factory Functions instead of Constructors](#use-factory-functions-instead-of-constructors)                                                 |
| 67   | [Avoid Global Imports](#avoid-global-imports)                                                 |
| 68   | [Use Functional Programming Principles](#use-functional-programming-principles)                   |
| 69   | [Use Promises Wisely](#use-promises-wisely)                                                    |
| 70   | [Use Performance Profiling Tools](#use-performance-profiling-tools)                           |
| 71   | [Use ES6 Modules](#use-es6-modules)                                                |
| 72   | [Use File-Based Routing instead of URL Routing](#use-file-based-routing-instead-of-url-routing) |
| 73   | [Use Multiple `.catch()` statements for Promises](#use-multiple-catch-statements-for-promises) |
| 74   | [Use Error-First Callbacks](#use-error-first-callbacks)           |

1. ### Minimize the use of Global Variables and Functions
    Global variables and functions can conflict with other code libraries, can be overwritten and cause issues. Functions can be placed in a module or namespace. For variables, local variables or closures can be used instead.

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

    Primitive values, such as numbers, strings, and booleans, should be treated as primitive data types and not as objects to optimize the execution speed and avoid side-effects.

    Suppose we have a constructor function named Person that initializes a person object with a name and age property.

        function Person(name, age) {
          this.name = name;
          this.age = age;
        }

        let person1 = new Person("John", 30);
        let person2 = new Person("Alex", 25);

    Now, let's see what happens if we forget to use the 'new' keyword while creating an object from the Person constructor:

        let person3 = Person("Mary", 20);

    In this case, person3 will be undefined because the constructor function doesn't return any value. This can lead to confusion and unexpected results in your code if you're not careful.
    To prevent this kind of issue, it's recommended to use object literals instead of constructors for creating new objects in JavaScript.

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

10. ### Use Static Types with TypeScript or Flow 
    In JavaScript, we have two popular static typing options, TypeScript and Flow. Both of these help us catch errors early on and greatly improve code quality.
    When working with large codebases and complex functions, static typing can greatly increase the maintainability and quality of code. By using TypeScript (or Flow), not only can you catch errors early, but you can also greatly improve code completion and documentation, making it easier for yourself and other developers to understand the code and maintain it over time.

    **[⬆ Back to Top](#table-of-contents)**


11. ### Avoid Using eval()
    Avoid using the eval() function, as it poses security risks by allowing arbitrary code to be executed.

    A string variable `code` which contains some JavaScript code needs to be executed dynamically at runtime. The `eval()` function could be used to execute the code:

        let code = "console.log('Hello, world!')";
        eval(code); // Outputs "Hello, world!" to the console

    However, using `eval()` in this way is not recommended since it could open up your application to security vulnerabilities. An attacker could potentially inject malicious code into the `code` variable, which would then be executed by the `eval()` function. For example:

        let code = "alert('You have been hacked!')";
        eval(code); // Displays a popup with the message "You have been hacked!"

    Instead, a safer way to execute dynamic code is using the `Function()` constructor. The `Function()` constructor creates a new Function object that can execute the code passed to it as a string. Here is an example:

        let code = "console.log('Hello, world!')";
        let executeCode = new Function(code);
        executeCode(); // Outputs "Hello, world!" to the console

    With this approach, the code is still executed dynamically at runtime, but there is no risk of code injection since the code is not executed until it is passed to the `Function()` constructor, which provides a controlled environment for the execution of the code.

    While `eval()` can be a powerful tool, it is important to use it with caution and take steps to prevent security vulnerabilities. Using the `Function()` constructor is often a safer and more secure alternative to `eval()`.

      **[⬆ Back to Top](#table-of-contents)**


12. ### Call things by their name
    Use clear and easily understandable variable and function names, and avoid ambiguous or confusing names.

      **[⬆ Back to Top](#table-of-contents)**


13. ### Stick to a strict coding style
    This will help reduce potential bugs, improve code security, and make it easier for other developers to understand the code. Avoid relying on hacks that may later become outdated as new browser versions are released. Use 'use strict' to enforce stricter syntax and avoid potential errors.

      **[⬆ Back to Top](#table-of-contents)**


14. ### Comment as much as needed but not more
    Use commenting to provide relevant information to other developers, but only when necessary.

      **[⬆ Back to Top](#table-of-contents)**


15. ### Avoid mixing CSS or styling with other technologies
    Avoid mixing unrelated technologies, such as adding styling with JavaScript. Keep styling information inside CSS to make it easier to manage and modify the styles.

     **[⬆ Back to Top](#table-of-contents)**


16. ### Use shortcut notation when it makes sense
    Use shortcuts like object literals, ternary notations, and || notation, whenever possible, to optimize code. In many cases, short-circuiting is a more concise and readable way to express conditions than ternary operators. This approach involves using boolean operators like && and || to check conditions and return values.
    
     **[⬆ Back to Top](#table-of-contents)**


17. ### Modularize - one function per task
    Break down tasks into smaller functions, and create helper functions for repetitive tasks, which makes the code smaller, manageable, and easy to debug. Function composition helps to organize code into small and modular functions. Avoid creating long chains of functions that can make code difficult to understand and debug. Instead of chaining all of the functions together in one long chain, it's better to break them up into separate functions and call them individually.

     **[⬆ Back to Top](#table-of-contents)**


18. ### Enhance progressively
    Write code that works even when certain technologies are unavailable, like scripting(for non-JS browsers). This enhances the functionality of your webpage or web product.

    **[⬆ Back to Top](#table-of-contents)**


19. ### Allow for configuration and translation
    Use a configuration object to contain parameters that are likely to change so that it is easier to maintain the code in the future. 
    
    **[⬆ Back to Top](#table-of-contents)**


20. ### Avoid heavy nesting
    Avoid excessive nesting in your code, use generic functions instead, and aim for code that is easy to read and understand.

    A common issue with nesting is variable names and loops. Starting with 'i' as the iterator and moving on to 'j', 'k', 'l', and beyond can quickly get messy. Use descriptive variable names to avoid confusion.

    **[⬆ Back to Top](#table-of-contents)**


21. ### Optimize loops
    Optimize loops by storing the length attribute of an array in a variable to avoid recalculating it on every iteration. Keep computation-heavy code outside of loops to improve performance.
  
    **[⬆ Back to Top](#table-of-contents)**


22. ### Keep DOM access to a minimum
    Reduce DOM access since it is costly and can slow down the performance of your code. Use a tool function to transform a string to DOM elements to improve the code's speed.

        // Bad code - accessing DOM multiple times
        const element1 = document.createElement('div')
        element1.id = "myElement1"
        element1.textContent = "Hello, world!"
        element1.style.color = 'red'

        const element2 = document.createElement('div')
        element2.id = "myElement2"
        element2.textContent = "Hello, world!"
        element2.style.color = 'blue'


        // Good code - accessing DOM once using a tool function
        function createElementsFromString(str) {
        const div = document.createElement('div');
        div.innerHTML = str.trim();
        return div.firstChild;
        }

        const element1 = createElementsFromString('<div id="myElement1">Hello, world!</div>');
        element1.style.color = 'red';

        const element2 = createElementsFromString('<div id="myElement2">Hello, world!</div>');
        element2.style.color = 'blue';


    **[⬆ Back to Top](#table-of-contents)**


23. ### Don’t write code specific to a certain browser
    Avoid over-dependence on any specific browser or its features while building your code, and use standards-based code. Otherwise, your code would become obsolete when the browser updates or a new browser is introduced.

    **[⬆ Back to Top](#table-of-contents)**


24. ### Validate data
    Avoid relying on invalid data, validate it before using it to avoid glitches and security threats. Do not solely depend on client-side validation, as it can create security vulnerabilities. Relying solely on client-side validation can introduce security vulnerabilities in the application. This is because client-side validation can be bypassed or manipulated by malicious users since the validation code is running on the user's machine and is therefore under their control.
    
    For example, an attacker can simply disable or modify the client-side validation code using browser developer tools. They can also send unauthorized requests to the server, bypassing the client-side validation altogether. In either case, the server assumes the data passed through client-side validation and processes it with the assumption that it is valid. This can lead to the introduction of vulnerabilities such as SQL injections, path traversals, and other security issues.

    Therefore, it is important to implement server-side validation in addition to client-side validation to ensure a more secure application.

    **[⬆ Back to Top](#table-of-contents)**


25. ### Avoid Overloading HTML and Use Templates Instead
    Use an HTML template and load it via Ajax instead of manipulating a document with innerHTML, which can cause flakiness, especially with certain browsers. This is because loading HTML via Ajax and manipulating the DOM directly with innerHTML can cause issues with performance, security, and browser compatibility.
    Use HTML templates and load them via Ajax. This involves separating the HTML markup from the JavaScript code, so you can manipulate the data and content without affecting the structure of the document.

    Templates can be created using various JavaScript libraries and frameworks such as Handlebars, Mustache, and React. These libraries allow you to write HTML-like syntax that can be rendered to the DOM at runtime. 

        // Define a template using Handlebars syntax
        var template = Handlebars.compile("<h1>{{title}}</h1><p>{{content}}</p>");

        // Define some data to be inserted into the template
        var data = { title: "Hello World", content: "Lorem ipsum dolor sit amet." };

        // Render the template to a DOM element
        var rendered = template(data);
        document.getElementById("my-div").innerHTML = rendered;

    Additionally, we should avoid the pitfalls of using innerHTML, which may lead to security vulnerabilities, cross-site scripting (XSS) attacks, and other issues.

    **[⬆ Back to Top](#table-of-contents)**


26. ### Carefully decide to make use of JS libraries or work with raw JS
    The decision to use JavaScript libraries or raw JavaScript depends on the project requirements and your team's expertise.

    JS libraries are prewritten codes that are developed to handle a specific task, like DOM manipulation, AJAX requests, CSS animations, etc. This allows developers to focus on building the core functionality of their applications rather than worrying about low-level implementation details. They can significantly reduce development time, eliminate the need for duplicate coding effort, and provide better code consistency and quality.

    On the other hand, using raw JavaScript can optimize page load times and improve performance by avoiding the external library files. Raw JavaScript also offers greater control, flexibility, and customization options than what a library can provide.

    In conclusion, both libraries and raw JavaScript have their advantages and disadvantages. Evaluate project requirements, performance, load times, team expertise, and desired outcomes to make a decision that fits best for your project.

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


30. ### Declare Variables and Functions Outside of the Loops
    These variables and functions will be created multiple times which will hurt the performance of your code. Move such variables and functions outside the loop instead.

    **[⬆ Back to Top](#table-of-contents)**


31. ### Use native methods to Build a String
    Use native methods like join() instead of a for statement when looping through arrays to make your code faster.
    In addition to the join() method, there are many other native methods available in the String prototype that can be used to manipulate strings. Some examples include slice(), substring(), toLowerCase(), and toUpperCase(). Choosing to use these native methods over writing custom string manipulation methods can lead to faster and more maintainable code.

    **[⬆ Back to Top](#table-of-contents)**


32. ### Use Template Literals
    Use template literals instead of traditional strings since they are more flexible and easier to work with.

    **[⬆ Back to Top](#table-of-contents)**


33. ### Don't Pass a String to setInterval or setTimeOut
    Instead, pass a function name to avoid inefficient code and reduce the chances of errors. 

    When we pass a string, it gets evaluated in a global scope and it is difficult to debug code. It also creates a slight overhead as the string has to be evaluated within the global scope, which can impact the performance of your application. 

    On the other hand, when we pass a function name, it directly invokes the function, and there is no overhead of string evaluation. This makes the code more efficient and less prone to errors.

    ```javascript
    // Not Recommended Way (String Method)
    setTimeout('alert("Hello World!")', 500);

    // Recommended Way (Function Method)
    setTimeout(() => {
        alert("Hello World!");
    }, 500);
    ```

    In this example, we are using the `setTimeout` method to display an alert message after 500 milliseconds. In the first example, we pass a string as a parameter to the `setTimeout` method, which will execute the code `"alert('Hello World!')"` after 500 milliseconds. This is not recommended because the string has to be evaluated in a global scope and it can be error-prone.

    In the second example, we pass an anonymous function as a parameter to the `setTimeout` method. This is the recommended way because it directly invokes the function, and there is no overhead of string evaluation. Additionally, the use of an anonymous function allows for more flexibility and provides cleaner and more readable code.

    **[⬆ Back to Top](#table-of-contents)**


34. ### Use object literals and arrays instead of constructors 
    Object literals and arrays are a more straightforward way to create objects and arrays in JavaScript than using the new constructor method.
    Use {} Instead of new Object() and use [] Instead of new Array() as when using the new constructor method in JavaScript, there are a few potential pitfalls to be aware of.

    One common issue is accidental type coercion. When using new with a non-primitive value (like an object or array), the 'new' keyword can cause unexpected type coercion. For example, if you accidentally omit the new keyword when creating a new instance of an object using a constructor function, the 'this' keyword inside the constructor will refer to the global object instead of the new object you intended to create, which can lead to unintended consequences in your code.

    Additionally, the new keyword can add a bit of extra complexity and confusion when creating objects or arrays. By using object literals ({}) or array literals ([]) instead of the new constructor notation, you can simplify your code and make it easier to understand.

    **[⬆ Back to Top](#table-of-contents)**


35. ### Use SetTimeout instead of SetInterval
    Use the SetTimeout function instead of SetInterval to prevent performance issues. It's generally better to use setTimeout when the processing time of each iteration of the task cannot be predicted or when there is asynchronous code involved.

    Using setInterval
        function makeApiRequest() {
        fetch('https://example.api.com/data')
            .then(response => response.json())
            .then(data => {
            // Process data here
            console.log(data);
            })
            .catch(error => {
            console.error('Error fetching data:', error);
            });
        }

        setInterval(makeApiRequest, 5000);

    Using setTimeout
        function makeApiRequest() {
        fetch('https://example.api.com/data')
            .then(response => response.json())
            .then(data => {
            // Process data here
            console.log(data);
            })
            .catch(error => {
            console.error('Error fetching data:', error);
            })
            .finally(() => {
            // Make the next request after 5 seconds
            setTimeout(makeApiRequest, 5000);
            });
        }

        makeApiRequest();

    **[⬆ Back to Top](#table-of-contents)**


36. ### Use the Spread Operator
    Use the spread operator (...) to insert all values from one array into another or pass all items of an array as individual elements to another function. It can also be used for copying objects and arrays, rather than using Object.assign or slice methods.

    **[⬆ Back to Top](#table-of-contents)**


37. ### Be Careful With for ... in Statements
    When using a for...in loop to loop through an object, filter out method functions (such as hasOwnProperty) and other inherited properties by wrapping the code in an if statement.

    ```
    const obj = {
        a: 1,
        b: 2,
        c: 3,
        hasOwnProperty: function() {
            // This is a method function
        },
        toString: Object.prototype.toString
        };

    for (let key in obj) {
        if (typeof obj[key] !== "function" && key !== "hasOwnProperty" && key !== "toString") {
            console.log(key, obj[key]);
        }
    }
    ```

    Filtering out method functions and other inherited properties can make your code more readable and maintainable.

    **[⬆ Back to Top](#table-of-contents)**


38. ### Use Self-Executing Functions
    Make use of self-executing functions to run a function automatically when a page loads or a parent function is called. This approach can be beneficial as it ensures that the code runs immediately, without having to be called elsewhere in the code.

    Using self-executing functions can also help avoid conflicts with other scripts, global variables and namespace issues, particularly when dealing with libraries or code that contains lots of functions.

    **[⬆ Back to Top](#table-of-contents)**


39. ### Use Event Emitters instead of Callbacks
    While using callbacks work perfectly fine in a small codebase, it can lead to callback hell, which becomes difficult to maintain and debug as the codebase grows. Using event emitters will improve code maintainability, readability, and prevent callback hell.

    Using Event Emiitter
        const EventEmitter = require('events');

        const eventEmitter = new EventEmitter();

        const processReport = (report) => {
        console.log(`Report processed: ${report}`);
        };

        // Registering the event with a callback function
        eventEmitter.on('processReport', processReport);

        const reportGenerator = () => {
        // Generate report
        const report = 'Some report';

        // Emitting the event with report as the parameter
        eventEmitter.emit('processReport', report);
        }

        // Generating the report
        reportGenerator();
 
    Using Callbacks
        const processReport = (report, callback) => {
        // Do some processing
        console.log(`Report processed: ${report}`);
        // Call the callback function once processing is done
        return callback();
        }

        const reportGenerator = (callback) => {
        // Generate report
        const report = 'Some report';
        // Process the report with a callback
        processReport(report, callback);
        }

        // Generating the report with a callback
        reportGenerator(() => {
        console.log('Report generation complete.');
        });

    **[⬆ Back to Top](#table-of-contents)**


40. ### Quickly Assign Variable Values With Destructuring
    Use destructuring to extract values from objects and arrays easily. This allows us to avoid variable assignments for values we don't need. Also, destructuring assignments can be used for function arguments to make them more in line for readability.

    **[⬆ Back to Top](#table-of-contents)**


41. ### Make use of Iterators and for ... of Loops
    Iterators in JavaScript are objects which implement the next() method to return an object that stores the next value in a sequence and true or false depending on whether or not there are any more values left. JavaScript also has some built-in iterators like String, Array, Map, etc. You can iterate over them using for ... of loops. 

        const arr = [1, 2, 3, 4, 5];

    // Using for loops
        for (let i = 0; i < arr.length; i++) {
            console.log(arr[i]);
        }
    
    // Using for...of loop
        for (const item of arr) {
            console.log(item);
        }

    // Using iterators
        const mySet = new Set([1, 2, 3, 4, 5]);

        // create an iterator object using the `values()` method
        const setIterator = mySet.values();

        let nextValue = setIterator.next();

        while (!nextValue.done) {
            console.log(nextValue.value);
            nextValue = setIterator.next();
        }
    
    Use iterators and for...of loops for more concise and less error-prone code.

    **[⬆ Back to Top](#table-of-contents)**


42. ### Use async and await
    Promises can be used for Asynchronous Code to avoid callback hell. Also, asynchronous functions can be created with the async keyword and take advantage of the await keyword to stop execution until the resolution of returned promises. Use async and await keywords for cleaner, more readable asynchronous code.

    **[⬆ Back to Top](#table-of-contents)**


43. ### Use Arrow Functions more
    Use arrow functions for more readable and concise functional JavaScript code.

    Another notable benefit of arrow functions is that they do not define a scope, instead being within the parent scope. This prevents many of the issues that can occur when using the 'this' keyword. There are no bindings for 'this' in the arrow functions. 'this' has the same value inside the arrow function as it does in the parent scope. However, this means arrow functions can't be used as constructors or methods.

    **[⬆ Back to Top](#table-of-contents)**


44. ### Make use of the Javascript includes() Method
    Use the includes() method to check if a string contains certain characters or if an array contains a specific element.

    **[⬆ Back to Top](#table-of-contents)**


45. ### Run Promises in Parallel
    Run asynchronous tasks in parallel using Promise.all(). It can make the app much faster and more responsive. 

    **[⬆ Back to Top](#table-of-contents)**


46. ### Use Regex When Extracting or Working With Strings
    Use regex instead of complicated string manipulation methods like indexOf() and substring().

    const myString = "I love my dog";

    // Using indexOf
    const containsDog = myString.indexOf("dog") !== -1;

    // Using regex
    const containsDog = /dog/.test(myString);

    console.log(containsDog) // true

    **[⬆ Back to Top](#table-of-contents)**


47. ### Put JavaScript in a Separate File
    Keeping JavaScript in a separate file makes it more organized, reusable, and easier for web browsers to cache.

    **[⬆ Back to Top](#table-of-contents)**


48. ### Use Splice to Remove Items From an Array
    Use splice() to remove elements from an array instead of the delete method.

    The `delete` method removes the specified element from an array by setting it to undefined. It does not actually remove the element from the array. This means that the array length does not change and the deleted element is replaced with `undefined`.

    ```javascript
    const myArray = ["apple", "banana", "orange"];
    delete myArray[1];

    console.log(myArray); // ["apple", undefined, "orange"]
    ```

    Note that the length of `myArray` is still 3, and the element at index 1 is now `undefined`.

    On the other hand, `splice()` method modifies the contents of an array by removing or replacing existing elements and/or adding new elements. It can remove one or more elements from an array and returns the removed elements as a new array. When we use `splice()`, we can completely remove an element from the array by manipulating the original array. This means that the length of the array is updated and the array is re-indexed.

    ```javascript
    const myArray = ["apple", "banana", "orange"];
    myArray.splice(1, 1);

    console.log(myArray); // ["apple", "orange"]
    ```

    In this example, we use `splice()` to remove the element at index 1 (which is "banana") from the array. As a result, the length of the array is now 2 and the element at index 1 is "orange".

    In conclusion, `splice()` method should be used to remove elements from an array instead of `delete` method because `splice()` method can completely remove an element from an array and update its length and indices. On the other hand, `delete` method only sets the element to `undefined`, leaving its place in the array with a gap of `undefined`. Therefore, `splice()` method provides a cleaner and more consistent way of manipulating arrays.

    **[⬆ Back to Top](#table-of-contents)**


49. ### Incorporate Testing
    Testing is essential for catching bugs and preventing issues down the line. It ia also is essential for ensuring quality code and saving time and money during the development process. Use unit and integration tests to ensure your code is working as expected.

    **[⬆ Back to Top](#table-of-contents)**


50. ### Use Object.freeze to Create Immutable Objects
    Use Object.freeze() to create immutable objects which can't be modified or deleted. This can prevent bugs and improve performance.
    
    **[⬆ Back to Top](#table-of-contents)**

    
51. ### Use the Map and Set Data Structures
    The Map and Set data structures are powerful tools for handling data in JavaScript. They allow you to store data in key-value pairs and unique values, respectively. Use them where appropriate to simplify your code and improve performance. 
    
    **[⬆ Back to Top](#table-of-contents)**


52. ### Avoid Using InnerHTML
    Avoid using innerHTML to modify the content of your web pages. This feature can cause unexpected behavior and security vulnerabilities, so use the DOM manipulation methods provided by the browser instead. 

    `innerHTML` is a property that allows developers to modify the HTML content of an element in the DOM by replacing the entire content of the element with new HTML code. While it is a convenient way to change the HTML content of a web page, there are several reasons why developers should avoid using `innerHTML`, and instead use the DOM manipulation methods provided by the browser.

    1. Security vulnerabilities: This is because `innerHTML` can be used to inject malicious scripts into a web page, which can then be executed by unsuspecting users.

    2. Overwriting event listeners: `innerHTML` replaces the entire content of an element, including any event listeners that may be attached to child elements. This means that if you use `innerHTML` to add new content to an element, any event listeners that were previously attached to child elements will be lost.

    3. Performance: `innerHTML` is a slower way to modify the content of a web page than using the DOM manipulation methods. This is because when you use `innerHTML`, the browser has to re-parse and re-render the entire element, which is an expensive process.

    4. Separation of concerns: Manipulating DOM objects through `innerHTML` mixes HTML markup with JavaScript code, breaking the separation of concerns principle. This makes the code hard to maintain and debug.

    In conclusion, it is highly recommended that developers avoid using `innerHTML` to modify the content of web pages. Instead, they should use the DOM manipulation methods provided by the browser. Using these methods is faster, more secure, and helps maintain clear separation between HTML markup and JavaScript code.
    
    **[⬆ Back to Top](#table-of-contents)**


53. ### Use Class Syntax for Object-Oriented Programming
    JavaScript class syntax provides a more familiar and structured approach to object-oriented programming. Use it where appropriate to simplify your code and make it more readable.

    One of the main benefits of using class syntax over the traditional constructor/prototype approach is that it encourages better code organization and promotes the separation of concerns. You can use class syntax to create modular, reusable, and extendable code.

    Another benefit of using class syntax is that it is easier to extend and subclass classes. Classes created with the class syntax can easily be extended and overridden by creating new classes that inherit from them. This inheritance can be achieved using the extends keyword.

    Here's an example of creating a simple class using class syntax and instantiating an object:
    ```
    class Person {
        constructor(name, age) {
            this.name = name;
            this.age = age;
        }
        sayHello() {
            console.log(`Hello, my name is ${this.name} and I am ${this.age} years old.`);
        }
    }

    const john = new Person('John', 30);
    john.sayHello();
    ```

    In this example, we defined a Person class with a constructor that initializes the name and age properties of a Person object. We also defined a sayHello method that logs a greeting message to the console. We then instantiated a 'John' object from the Person class and called the sayHello method on it.

    Using class syntax in your JavaScript code provides a more structured and familiar approach to OOP, making your code easier to read and maintain. It also promotes separation of concerns and enables easy extension of classes.

    **[⬆ Back to Top](#table-of-contents)**


54. ### Use the Fetch API for HTTP Requests
    The Fetch API is a modern and powerful way to make HTTP requests in JavaScript. Use it instead of older and less secure techniques like XMLHttpRequest.

    **[⬆ Back to Top](#table-of-contents)**


55. ### Use Linters
    Linters help ensure that your code follows best practices and style guidelines. Use a linter like ESLint to catch errors and enforce standards.

    **[⬆ Back to Top](#table-of-contents)**


56. ### Use the Proxy Object to Intercept Object Operations 
    Use the Proxy object to intercept object operations and customize their behavior. This can be useful for adding validation or access control to objects.

    const user = {
        firstName: 'John',
        lastName: 'Doe',
        password: 'secret'
        };

        const userProxy = new Proxy(user, {
        get(target, property) {
            if (property === 'password') {
            throw new Error('Access denied');
            } else {
            return target[property];
            }
        },
        set(target, property, value) {
            if (property === 'firstName') {
            throw new Error('Cannot modify first name');
            } else {
            target[property] = value;
            }
        }
        });

        console.log(userProxy.firstName); // "John"
        console.log(userProxy.lastName); // "Doe"
        console.log(userProxy.password); // Throws "Access denied" error
        userProxy.firstName = 'Jane'; // Throws "Cannot modify first name" error
        userProxy.age = 25; // Adds the "age" property to the user object
        console.log(userProxy.age); // 25

    **[⬆ Back to Top](#table-of-contents)**


57. ### Use Server-Side Rendering for Improved Performance
    Use server-side rendering to improve the initial load time and performance of your web application, especially for mobile devices with slower network speeds.

    **[⬆ Back to Top](#table-of-contents)**


58. ### Use Event Delegation
    Use event delegation to reduce the number of event listeners added to the page, reducing overhead, and improving performance.

    **[⬆ Back to Top](#table-of-contents)**


59. ### Use Memoization to Improve Performance
    Use memoization to cache the results of expensive function calls, improving performance when the same calculation is needed later.

    **[⬆ Back to Top](#table-of-contents)**


60. ### Use Web Workers
    Use web workers to offload heavy computation tasks to a separate thread, improving the responsiveness of your web application.

    **[⬆ Back to Top](#table-of-contents)**


61. ### Use the Object.assign Method for Object Composition
    The Object.assign method can be used to merge objects together to create new objects quickly and easily. This method is especially useful for composition-based programming.

    Object composition, also known as object aggregation or object delegation, is a programming technique that involves combining two or more objects to create a new object with the desired behavior and functionality. Instead of using inheritance to create new objects, composition-based programming uses existing objects to build new ones.

    JavaScript provides the Object.assign method for object composition. This method can be used to merge two or more objects together to create a new object quickly and easily. The Object.assign method takes two or more objects as parameters and returns a new object that is a merge of all the objects passed as parameters.

    ```javascript
    const person = {
    name: 'John',
    age: 30,
    gender: 'male'
    };

    const job = {
    company: 'Acme Inc.',
    position: 'Engineer'
    };

    const employee = Object.assign({}, person, job);
    console.log(employee);
    ```

    In this example, we have two objects, `person` and `job`. We want to merge these two objects together to create a new object called `employee`. We call the `Object.assign()` method with an empty object `{}` as the first parameter, followed by `person` and `job`. This creates a new object called `employee` that is a merge of `person` and `job`.

    In the new object `employee`, all properties and methods from `person` and `job` are now available. In the case where a key exists on both objects, the value from the last object passed in wins. 

    Object.assign is especially useful in cases where you want to use a specific set of properties from an existing object to compose a new object without touching the original object.

    Overall, Object.assign can be used for object composition in your JavaScript code because it provides a quick and easy way to merge objects together and create new objects with desired behavior and functionality.

    **[⬆ Back to Top](#table-of-contents)**


62. ### Use Web Components for Reusable UI Elements
    Web Components are a set of web APIs that allow you to create reusable UI elements for web applications. Web Components provide encapsulation, making it possible for you to create isolated components with a scope that protects them from the rest of the web page. This isolation makes them an excellent choice for teams and developers who want to reuse UI elements that can be shared across multiple web applications. 

    Web Components consist of three main parts: 
    1. Custom Elements - Allow you to create your own HTML tags 
    2. Shadow DOM - Provides a way to encapsulate DOM and CSS so that your styles won’t affect or be affected by the rest of the page 
    3. HTML Templates - Allow you to declaratively define DOM structure.

    Advantages:
    1. They provide a standardized way of defining custom elements, which means you can create UI components that can be used across different frameworks or even in vanilla JavaScript. This standardization makes it easier for developers to share and reuse components, which reduces development time and maintenance costs.

    2. They allow you to create components that are encapsulated from the rest of your code or the DOM. This encapsulation helps reduce name collisions and makes it easier to reason about component behavior, which can be particularly useful in large web applications or team settings.

    3. Web Components provide an abstraction layer for creating complex UI elements. By combining the Custom Elements, Shadow DOM, and Templates APIs, you can create UI elements that are far more complex than what is possible with traditional HTML and CSS. This not only results in a more modular code structure but also improves the overall maintainability and usability of the application.

    Overall, by using Web Components to create reusable UI elements, you can reduce development time and maintenance costs, as well as improve the separation of concerns within your codebase.

    **[⬆ Back to Top](#table-of-contents)**


63. ### Use DRY (Don't Repeat Yourself) Principle
    Avoid repeating the same code in multiple places. Instead, use functions, classes, or modules to encapsulate the commonly used code.

    **[⬆ Back to Top](#table-of-contents)**


64. ### Use Error Handling
    Add proper error handling to your code to catch and handle errors in a graceful way. This can prevent crashes and improve the user experience.

    **[⬆ Back to Top](#table-of-contents)**


65. ### Use Web Storage API for Data Storage
    Use the Web Storage API to store data in the browser, reducing the need for network requests and improving the performance of your web application.

    **[⬆ Back to Top](#table-of-contents)**


66. ### Use Factory Functions instead of Constructors
    In JavaScript, Factory functions are an alternative to constructors for creating objects. They provide a way to encapsulate and control the object creation process, and they allow for the creation of immutable objects.

    Factory functions are regular functions that return an object. You can pass parameters to the function to specify the initial state of the object, and the function can perform any necessary setup or validation before returning the object.

    ```javascript
    function createPerson(name, age) {
    return {
        name,
        age,
        sayHello() {
        console.log(`Hello, my name is ${this.name} and I am ${this.age} years old.`);
        }
    };
    }

    const person = createPerson('John', 30);
    person.sayHello();
    ```

    In this example, `createPerson` is a factory function that takes two parameters, `name` and `age`, and returns an object with those properties set. The object also has a method, `sayHello`, that prints a greeting to the console. 

    One of the key advantages of factory functions over constructors is that they allow for the creation of immutable objects. An immutable object is an object whose state cannot be changed after it is created. This can be useful in situations where you want to enforce a safer and more predictable state for the objects in your program.

    ```javascript
    function createImmutablePerson(name, age) {
    return Object.freeze({
        name,
        age,
        sayHello() {
        console.log(`Hello, my name is ${this.name} and I am ${this.age} years old.`);
        }
    });
    }
    const immutablePerson = createImmutablePerson('Jane', 25);
    ```

    In this example, the `Object.freeze()` method is used to create an immutable object. This method prevents any changes from being made to the object's properties. You can still call methods on the object, but you cannot change its state.

    Overall, factory functions are an excellent alternative to constructors for creating objects in JavaScript. They allow for better control over the creation process, and they offer the ability to create immutable objects.

    **[⬆ Back to Top](#table-of-contents)**


67. ### Avoid Global Imports
    Avoid Global Imports for Javascript Modules to prevent namespace pollution.

    In JavaScript, global imports can be used to bring in functionality from other modules, making it available to the entire program. However, this can lead to namespace pollution, where different modules can define variables and functions with the same name, causing unexpected behavior.

    To avoid this, it's recommended to avoid global imports for JavaScript modules. Instead, use module imports to keep each module's namespace separate.

    ```javascript
    // importing the entire lodash library globally
    import _ from 'lodash';

    // using the map function from lodash
    const numbers = [1, 2, 3, 4, 5];
    const doubledNumbers = _.map(numbers, n => n * 2);
    console.log(doubledNumbers);
    ```

    In this example, the entire lodash library is imported globally using the `_` variable, which is then used to call the `map` function. However, this can cause namespace pollution if other modules in the program also use the `_` variable.

    Instead, use module imports to keep each module's namespace separate:
    ```javascript
    // importing only the map function from lodash
    import { map } from 'lodash';

    // using the map function from lodash
    const numbers = [1, 2, 3, 4, 5];
    const doubledNumbers = map(numbers, n => n * 2);
    console.log(doubledNumbers);
    ```

    In this example, only the `map` function is imported from lodash using object destructuring syntax. This keeps the `map` function isolated to the module it's being used in, and avoids any potential namespace pollution.

    By avoiding global imports for JavaScript modules, you can keep your code more organized and prevent potential conflicts between modules.

    **[⬆ Back to Top](#table-of-contents)**


68. ### Use Functional Programming Principles
    Functional programming is a programming paradigm that emphasizes the use of functions to define computation rather than imperative statements. It advocates for using immutability, pure functions, and higher-order functions as a means of developing robust, maintainable, and readable code.

    Immutability, or the inability of objects to change after creation, is one of the fundamental principles of functional programming. It enables programs to be more predictable, easier to test, and less prone to errors. By using immutable objects, you can avoid unintended side effects and create code that is easier to reason about.

    Pure functions are another key concept in functional programming. These are functions that do not rely on any external state and always produce the same output for a given input. They are side-effect free and enable code to be written in a declarative manner rather than an imperative one. By using pure functions, you can minimize the number of side effects in your program and create more predictable and testable code.

    Higher-order functions are functions that can take other functions as their input or return functions as their output. They are useful for abstracting away complexity and can improve code reuse and maintainability.

    Functional programming techniques like map, filter, and reduce can also be used to improve data handling. These techniques allow you to apply operations to collections of data without the need for explicit iteration. Moreover, when chaining these techniques, they can reflect complex transformations in a single line of code.

    Currying and composition are two more techniques employed by functional programming, this time for event handling. Currying involves turning a function with multiple arguments into a series of functions with one argument. This simplifies event handling by allowing events with complex arguments to be handled more easily. Composition, on the other hand, involves chaining functions together to create more complex functionality. It enables developers to build complex systems out of small, reusable functions, improving code reuse and maintainability.

    In summary, functional programming principles and techniques like immutability, pure functions, higher-order functions, map, filter, reduce, currying, and composition can be used to create more robust, maintainable, and readable code. They can help developers minimize unintended side effects, abstract away complexity, and improve code reuse and maintainability, all of which can make for a better development experience and stronger software products.

    **[⬆ Back to Top](#table-of-contents)**


69. ###  Use Promises Wisely
    Promises can be used for Asynchronous Code to avoid callback hell. Promises can simplify and improve your asynchronous code, but they should be used carefully. Avoid creating too many promises at once, and always handle errors properly.

    **[⬆ Back to Top](#table-of-contents)**


70. ### Use Performance Profiling Tools
    Use performance profiling tools like Chrome's DevTools to identify performance issues in your code.

    **[⬆ Back to Top](#table-of-contents)**


71. ### Use ES6 Modules
    ES6 modules allow you to import and export code modules between files, reducing coupling and improving maintainability. Also, Default Exports can be used for Javascript Modules to keep the code cleaner and organized.

    **[⬆ Back to Top](#table-of-contents)**


72. ### Use File-Based Routing instead of URL Routing
    Use File-Based Routing instead of URL Routing to make code simpler and more maintainable. It can also help to structure sub-routes better as within URL routing, it can create a scenario where to incorporate all the URLs can increase the length of the object and file.

    File-based routing, also known as page-based routing, is an alternative to URL-based routing that simplifies the organization and management of web application routes. In file-based routing, each route is defined as a separate file, typically with a filename that matches the corresponding route's URL path. When a user navigates to a particular route, the server serves up the contents of the corresponding file.

    One of the main benefits of file-based routing is that it makes web application code simpler and more maintainable. With file-based routing, routing is handled by the file system rather than by a routing configuration file. This approach eliminates the need for separate routing logic and makes the routing process more transparent and easier to understand.

    File-based routing can also improve the structure of sub-routes by allowing them to be organized more clearly and logically. Within URL routing, as the number of routes grows, it can create a cumbersome object or file with excessive length. In contrast, file-based routing allows sub-routes to be organized within separate directories, making it easier to locate and modify specific routes.

    Another benefit of file-based routing is that it can simplify the process of adding new routes or modifying existing ones. Instead of maintaining a routing configuration file, developers can simply add or modify files in the appropriate directories, greatly simplifying the process of managing routes.

    When building web applications, routing is one of the fundamental components that enable users to navigate between different pages or resources. Two common approaches for routing in web applications are URL routing and file-based routing.

    For example, let's say we're building a simple blogging application with the following routes:
    - / (home page)
    - /blog (blog page)
    - /blog/post (single post page)

    In URL routing, we may create a router that maps each of these routes to its corresponding function:
    ```
    app.get('/', (req, res) => {
    // render home page
    });

    app.get('/blog', (req, res) => {
    // render blog page
    });

    app.get('/blog/post', (req, res) => {
    // render single post page
    });
    ```

    However, in file-based routing, we may organize our code into separate files that correspond to each route:
    ```
    - src
    - routes
        - home.js
        - blog.js
        - post.js
    ```

    In `home.js`, we define the handling logic for the home page route:
    ```
    const express = require('express');
    const router = express.Router();

    router.get('/', (req, res) => {
    // render home page
    });

    module.exports = router;
    ```

    In `blog.js`, we define the handling logic for the blog page route:
    ```
    const express = require('express');
    const router = express.Router();

    router.get('/', (req, res) => {
    // render blog page
    });

    module.exports = router;
    ```

    In `post.js`, we define the handling logic for the single post page route:
    ```
    const express = require('express');
    const router = express.Router();

    router.get('/', (req, res) => {
    // render single post page
    });

    module.exports = router;
    ```

    In summary, File-based routing offers a simpler, more organized alternative to URL-based routing that can help developers build maintainable applications with clear and logical routing structures. By breaking up routes into separate files, developers can better manage and modify routing logic and create a more transparent and easier-to-understand application routing process.

    **[⬆ Back to Top](#table-of-contents)**


73. ### Use Multiple `.catch()` statements for Promises
    Use Multiple `.catch()` statements for Promises to handle errors easily and have clear error messages.

    **[⬆ Back to Top](#table-of-contents)**


74. ### Use Error-First Callbacks
    By consistently using Error-First Callbacks throughout the application, we can handle errors in a standardized and consistent manner, making it easier to identify and debug issues. Additionally, by providing more meaningful error messages, we can make it easier for developers to understand and address any issues that may occur.
      const fetchData = (callback) => {
        axios.get('https://api.example.com/data')
        .then((response) => {
            setData(response.data);
            callback(null, response.data);
        })
        .catch((error) => {
            callback(error);
        });
    };

    fetchData((error, data) => {
        if (error) {
        console.log(`Error fetching data: ${error.message}`);
        } else {
        console.log(`Fetched data: ${data}`);
        }
    });

    **[⬆ Back to Top](#table-of-contents)**
