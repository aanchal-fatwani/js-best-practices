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
| 41   | [Raw JavaScript Is Always Quicker Than Using a Library](#raw-javaScript-is-always-quicker-than-using-a-library)                                         |
| 42   | [Quickly Assign Variable Values With Destructuring](#quickly-assign-variable-values-with-destructuring)                                         |
| 43   | [Iterators and for ... of Loops](#iterators-and-for-of-loops)                                         |
| 44   | [async and await](#async-and-await)                                         |
| 45   | [Use Arrow Functions](#use-arrow-functions)                                         |
| 46   | [Use the Javascript includes() Method](#use-the-javascript-includes-method)                                         |
| 47   | [Run Promises in Parallel](#run-promises-in-parallel)                                         |
| 48   | [Use Regex When Extracting or Working With Strings](#use-regex-when-extracting-or-working-with-strings)                                         |
| 49   | [Put JavaScript in a Separate File](#put-javaScript-in-a-separate-file)                                         |
| 50   | [Use Splice to Remove Items From an Array](#use-splice-to-remove-items-from-an-array)                                         |
| 51   | [Incorporate Unit Testing](#incorporate-unit-testing)                                         |

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


41. ### Raw JavaScript Is Always Quicker Than Using a Library
    JavaScript libraries, such as jQuery and lodash, can save you an enormous amount of time when coding—especially with AJAX operations. Having said that, always keep in mind that a library can never be as fast as raw JavaScript (assuming you code correctly).

    jQuery's each() method is great for looping, but using a native for statement will always be an ounce quicker.

    **[⬆ Back to Top](#table-of-contents)**

42. ### Quickly Assign Variable Values With Destructuring
    We've already learned about the spread operator in JavaScript earlier in the article. Destructuring is somewhat similar in the sense that it also unpacks values stored inside arrays. The difference is that we can assign these unpacked values to unique variables.

    The syntax is similar to creating an array using the [] shorthand. However, this time the brackets go on the left side of the assignment operator. Here is an example:

    let [person, fruit, , day] = ['Monty', 'apple', 'reading', 'tomorrow'];
    var sentence = `${person} will eat an ${fruit} ${day}.`;
    console.log(sentence);
    // Output: Monty will eat an apple tomorrow.
    Did you notice how we just skipped the assignment of the third array element to any variable by not passing a variable name? This allows us to avoid variable assignments for values we don't need.

    **[⬆ Back to Top](#table-of-contents)**

43. ### Iterators and for ... of Loops
    Iterators in JavaScript are objects which implement the next() method to return an object that stores the next value in a sequence and true or false depending on whether or not there are any more values left. This means that you can create your own iterator objects if you implement the iterator protocol.

    JavaScript also has some built-in iterators like String, Array, Map, etc. You can iterate over them using for ... of loops. This is more concise and less error-prone compared to regular for loops.

    let people = ["Andrew", "Adam", "James", "Jack"];
    let people_count = people.length;
    for(let i = 0; i < people_count; i++) {
        console.log(people[i]);
    }
    /* 
    Andrew 
    Adam 
    James 
    Jack 
    */
    for(person of people) {
        console.log(person);
    }
    /* 
    Andrew 
    Adam 
    James 
    Jack 
    */
    With a for...of loop, we don't have to keep track of the total length of the array or the current index. This can reduce code complexity when creating nested loops.

    **[⬆ Back to Top](#table-of-contents)**

44. ### async and await
    You can use the async keyword to create asynchronous functions, which always return a promise either explicitly or implicitly. Asynchronous functions that you create can take advantage of the await keyword by stopping execution until the resolution of returned promises. The code outside your async function will keep executing normally.

    async function delayed_hello() {
        console.log("Hello Adam!");
        let promise = new Promise((resolve) => {
            setTimeout(() => resolve("Hello Andrew!"), 2000)
        });
        let result = await promise;
        console.log(result);
    }
    console.log("Hello Monty!");
    delayed_hello();
    console.log("Hello Sajal!");
    /* 
    Hello Monty! 
    Hello Adam! 
    Hello Sajal! 
    Hello Andrew! 
    */
    In the above example, "Hello Andrew" is logged after two seconds, while all other hellos are logged immediately. The call to the delayed_hello() function logs "Hello Adam" immediately but waits for the promise to resolve in order to log "Hello Andrew".

    **[⬆ Back to Top](#table-of-contents)**

45. ### Use Arrow Functions
    Arrow functions make the functional elements of JavaScript more appealing to the eye and easier to write.

    Take a look at how we would implement a filter without arrow functions:

    const nums = [1,2,3,4,5,6,7,8];
    const even_nums = nums.filter( function (num) { return num%2 == 0; } )
    Here, the callback function we pass to the filter returns true for any even number.

    Arrow functions make this much more readable and concise though: 

    const nums = [1,2,3,4,5,6,7,8];
    const even_nums = nums.filter(num => num%2 == 0)
    Another notable benefit of arrow functions is that they do not define a scope, instead being within the parent scope. This prevents many of the issues that can occur when using the this keyword. There are no bindings for this in the arrow functions. 'this' has the same value inside the arrow function as it does in the parent scope. However, this means arrow functions can't be used as constructors or methods.

    **[⬆ Back to Top](#table-of-contents)**

46. ### Use the Javascript includes() Method
    The includes() method in JavaScript determines whether or not a string contains the specified characters, or whether an array contains the specified element. If the string or element is found, this function returns true; otherwise, it returns false.

    const str = 'This String contains the word accept';
    console.log(str.includes('accept'));
    //output:true
    It's worth noting that the includes() method on Strings is case sensitive. If you want to match a string no matter the case, just make the target string lowercase first.

    const str = 'This String contains the word accept';
    console.log(str.toLowerCase().includes('string'));
    //output: true

    **[⬆ Back to Top](#table-of-contents)**

47. ### Run Promises in Parallel
    It is preferable to run your asynchronous tasks in parallel as it can make your app much faster and more responsive. If your tasks don't rely on the results from one another, simply wrap them in Promise.all and run them in parallel.

    It is really great to combine async / await and Promise.all, but you must be careful to think through what parts happen sequentially and what parts happen in parallel. Here's an example of fetching the text from an array of URLs concurrently with Promise.all and await.

    const urls = ["https://en.wikipedia.org/wiki/Canada", "https://en.wikipedia.org/wiki/Nigeria", "https://en.wikipedia.org/wiki/Vietnam"]
    const countryInfo = await Promise.all(urls.map( async url =>
      const resp = await fetch(url);
      return resp.text();
    }));
    This will map the URLs in the array to an array of async functions. Each async function will fetch the text from the URL and return it. Since this is an async function, it is actually a Promise. Promise.all will wait on those promises and return the array of text that they loaded when they are all complete.

    **[⬆ Back to Top](#table-of-contents)**

48. ### Use Regex When Extracting or Working With Strings
    Regex (regular expressions) is a really powerful and even fun tool. If you find yourself doing complicated searches and manipulations on strings using methods like indexOf() and substring(), you should reach for regex instead.

    Regular expressions enable you to search for complex patterns, and replace or extract text matching those patterns.

    A classic use of regex is to validate input. For example, the following regex can be used to validate a US five-digit zip code:

    const zipRegex = /\d{5}/
    console.log(zipRegex.test("12345"))
    //output: true 
    console.log(zipRegex.text("B3K 1R2"))
    //output: false

    **[⬆ Back to Top](#table-of-contents)**

49. ### Put JavaScript in a Separate File
    JavaScript can be written in a <script> tag in your HTML, or it can be kept in its own file and linked within your HTML. This helps keep different sorts of code isolated from one another this manner, and makes your code more understandable and well-organized.

    Keeping your JavaScript in separate files outside of the HTML facilitates the reuse of code across multiple HTML files. It provides for easier code reading, and it saves loading time since web browsers can cache external JavaScript files.

    **[⬆ Back to Top](#table-of-contents)**

50. ### Use Splice to Remove Items From an Array
    I've seen developers use the delete method to remove an item from an array. This is incorrect, because the delete function substitutes the object with undefined rather than removing it. In JavaScript, the best approach to remove an element from an array based on its value is to use the indexOf() function to discover the index number of that value in the array, and then use the splice() function to delete that index value.

    var items = ["apple","orange","berries","strawberry"];
    items.splice(2,1);
    console.log(items);
    //output: ['apple', 'orange', 'strawberry']

    **[⬆ Back to Top](#table-of-contents)**

51. ### Incorporate Unit Testing
    Tests are the most effective way to ensure that your code is error-free. Jest is a great place to start, but there are other options that are just as easy to use. Before any code is deployed, it should be subjected to unit testing to ensure that it fulfills quality standards. This promotes a dependable engineering environment that prioritizes quality. Unit testing saves time and money during the product development lifecycle, and it helps developers design better, more efficient code.

    **[⬆ Back to Top](#table-of-contents)**
