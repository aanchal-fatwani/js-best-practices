# JavaScript Best Practices

### Table of Contents

| No. | Title                                                                                                                                                         |
| --- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1   | [Avoid Global Variables](#avoid-global-variables)                                         |
| 2   | [Always Declare Local Variables](#always-declare-local-variables)                                         |
| 3   | [Declarations on Top](#declarations-on-top)                                         |
| 4   | [Initialize Variables](#initialize-variables)                                         |
| 5   | [Declare Objects with const](#declare-objects-with-const)                                         |
| 6   | [Declare Arrays with const](#declare-arrays-with-const)                                         |
| 7   | [Don't Use new Object](#dont-use-new-object)                                         |
| 8   | [Beware of Automatic Type Conversions](#beware-of-automatic-type-conversions)                                         |
| 9   | [Use === Comparison](#use--comparison)                                         |
| 10   | [Use Parameter Defaults](#use-parameter-defaults)                                         |
| 11   | [End Your Switches with Defaults](#end-your-switches-with-defaults)                                         |
| 12   | [Avoid Number, String, and Boolean as Objects](#avoid-number-string-and-boolean-as-objects)                                         |
| 13   | [Avoid Using eval](#avoid-using-eval)                                         |
| 14   | [Call things by their name](#call-things-by-their-name)                                         |
| 15   | [Stick to a strict coding style](#stick-to-a-strict-coding-style)                                         |
| 16   | [Comment as much as needed but not more](#comment-as-much-as-needed-but-not-more)                                         |
| 17   | [Avoid mixing CSS or styling with other technologies](#avoid-mixing-css-or-styling-with-other-technologies)                                         |
| 18   | [Use shortcut notation when it makes sense](#use-shortcut-notation-when-it-makes-sense)                                         |
| 19   | [Modularize — one function per task](#modularize--one-function-per-task)                                         |
| 20   | [Enhance progressively](#enhance-progressively)                                         |
| 21   | [Allow for configuration and translation](#allow-for-configuration-and-translation)                                         |
| 22   | [Avoid heavy nesting](#avoid-heavy-nesting)                                         |
| 23   | [Optimize loops](#optimize-loops)                                         |
| 24   | [Keep DOM access to a minimum](#keep-DOM-access-to-a-minimum)                                         |
| 25   | [Don’t yield to browser whims](#dont-yield-to-browser-whims)                                         |
| 26   | [Don’t trust any data](#dont-trust-any-data)                                         |
| 27   | [Add functionality with JavaScript, don’t create too much content](#add-functionality-with-javaScript-dont-create-too-much-content)                                         |
| 28   | [Build on the shoulders of giants](#build-on-the-shoulders-of-giants)                                         |
| 29   | [Development code is not live code](#development-code-is-not-live-code)                                         |
| 30   | [Don't Use Shorthand](#dont-use-shorthand)                                         |
| 31   | [Place Scripts at the Bottom of Your Page](#place-scripts-at-the-bottom-of-your-page)                                         |
| 32   | [Declare Variables Outside of the Loops](#declare-variables-outside-of-the-loops)                                         |
| 33   | [The Fastest Way to Build a String](#the-fastest-way-to-build-a-string)                                         |
| 34   | [Use Template Literals](#use-template-literals)                                         |
| 35   | [Don't Pass a String to setInterval or setTimeOut](#dont-pass-a-string-to-setInterval-or-setTimeOut)                                         |
| 36   | [Use {} Instead of new Object()](#use--instead-of-new-object())                                         |
| 37   | [Use [] Instead of new Array()](#use--instead-of-new-array())                                         |
| 38   | [Use the Spread Operator](#use-the-spread-operator)                                         |
| 39   | [Be Careful With for ... in Statements](#be-careful-with-for-in-statements)                                         |
| 40   | [Self-Executing Functions](#self-executing-functions)                                         |
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

1. ### Avoid Global Variables

    Minimize the use of global variables.

    This includes all data types, objects, and functions.

    Global variables and functions can be overwritten by other scripts.

    Use local variables or closures instead.

      **[⬆ Back to Top](#table-of-contents)**

2. ### Always Declare Local Variables

    All variables used in a function should be declared as local variables.
    
    Local variables must be declared with the let or const keyword, otherwise they will become global variables.

      **[⬆ Back to Top](#table-of-contents)**
      
3. ### Declarations on Top

    All declarations should be at the top of each script or function.

    This will:
    - Provide a single place to look for local variables
    - Make it easier to avoid unwanted (implied) global variables
    - Reduce the possibility of unwanted re-declarations

      **[⬆ Back to Top](#table-of-contents)**
      
4. ### Initialize Variables

     All variables should be initialized at the time of declaration.

     This will:
      - Provide a single place to initialize variables
      - Avoid undefined values

      **[⬆ Back to Top](#table-of-contents)**

5. ### Declare Objects with const
      Declaring objects with const will prevent any accidental change.

      **[⬆ Back to Top](#table-of-contents)**

6. ### Declare Arrays with const
    Declaring arrays with const will prevent any accidental change.

      **[⬆ Back to Top](#table-of-contents)**

7. ### Don't Use new Object
    - Use "" instead of new String()
    - Use 0 instead of new Number()
    - Use false instead of new Boolean()
    - Use {} instead of new Object()
    - Use [] instead of new Array()
    - Use /()/ instead of new RegExp()
    - Use function(){} instead of new Function()

      **[⬆ Back to Top](#table-of-contents)**
      
8. ### Beware of Automatic Type Conversions
    - JavaScript is loosely typed.
    A variable can contain all data types.

    - A variable can change its data type:
    Beware that numbers can accidentally be converted to strings or NaN (Not a Number).

    - When doing mathematical operations, JavaScript can convert numbers to strings:
    Subtracting a string from a string, does not generate an error but returns NaN (Not a Number).

      **[⬆ Back to Top](#table-of-contents)**
      
9. ### Use === Comparison
    The == comparison operator always converts (to matching types) before comparison.

      **[⬆ Back to Top](#table-of-contents)**
      
10. ### Use Parameter Defaults
    If a function is called with a missing argument, the value of the missing argument is set to undefined.

    Undefined values can break the code. It is a good habit to assign default values to arguments.

      **[⬆ Back to Top](#table-of-contents)**
      
11. ### End Your Switches with Defaults
    Always end your switch statements with a default. Even if you think there is no need for it.

      **[⬆ Back to Top](#table-of-contents)**
      
12. ### Avoid Number, String, and Boolean as Objects
    Always treat numbers, strings, or booleans as primitive values. Not as objects.

    Declaring these types as objects, slows down execution speed, and produces nasty side effects.

      **[⬆ Back to Top](#table-of-contents)**
      
13. ### Avoid Using eval()
    The eval() function is used to run text as code. In almost all cases, it should not be necessary to use it.

    Because it allows arbitrary code to be run, it also represents a security problem.

      **[⬆ Back to Top](#table-of-contents)**

14. ### Call things by their name
    Good variable and function names should be easy to understand and tell you what is going on — not more and not less. 

      **[⬆ Back to Top](#table-of-contents)**

15. ### Stick to a strict coding style
    Clean and valid code means less confusing bugs to fix, easier handover to other developers and better code security. When you rely on hacks to get your code to work it is likely that there is also a security exploit that uses the same hacks. In addition, as hacks get fixed in browsers, your code will cease to work in the next version of the browser.

    Valid code also means that it can be converted by scripts to other formats — hacky code will need a human to do that.

      **[⬆ Back to Top](#table-of-contents)**

16. ### Comment as much as needed but not more
    Comments are your messages to other developers (and yourself, if you come back to your code after several months working on something else). There’s been numerous battles raging over the years about whether to use comments at all, the main argument being that good code should explain itself.

    Again the trick is moderation. Comment when there is an important thing to say, and if you do comment use the /* */ notation. Single line comments using // can be problematic if people minify your code without stripping comments and in general are less versatile.

      **[⬆ Back to Top](#table-of-contents)**

17. ### Avoid mixing CSS or styling with other technologies
    Whilst it is possible to create everything you need in a document using JavaScript, CSS and manipulating the DOM, it is not necessarily the most effective way of doing so. 
    
    Adding the code to put a red border around every input field when its class is “mandatory” and there’s nothing in it through Javascript is possible, however it means that if you later need to make a change to these styles you need to go through the JavaScript and apply the changes there. By adding a class called “error” to the element when there is an error, you can ensure that the styling information is kept inside the CSS, which is more appropriate.

     **[⬆ Back to Top](#table-of-contents)**

18. ### Use shortcut notation when it makes sense
    Instead of repeating the object name for each property or method and assigning values through '.', make use of object literal and assign values through '{}'.
    
    Conditions can be shortened using “ternary notation”. Anything before the question mark is the condition, the value immediately after it is the true case and the one after the colon the false case. Ternary notation can be nested, but I’d avoid that to keep things readable.
    
    Another common situation in JavaScript is providing a preset value for a variable if it is not defined through '||' the double pipe character. For eg. x || 5 will capture value of x if x is present, otherwise it will take 5.
    
     **[⬆ Back to Top](#table-of-contents)**

19. ### Modularize — one function per task
    Create functions that fulfill one job at a time which makes it easy for other developers to debug and change the code without having to scan through all the code to work out what code block performs what function.

    This also applies to creating helper functions for common tasks. If you find yourself doing the same thing in several different functions then it is a good idea to create a more generic helper function instead, and reuse that functionality where it is needed.
    
     **[⬆ Back to Top](#table-of-contents)**

20. ### Enhance progressively
    Write code that works regardless of available technology. In the case of JavaScript, this means that when scripting is not available (say on a BlackBerry, or because of an over-zealous security policy) your web products should still allow users to reach a certain goal, not block them because of the lack of JavaScript which they can’t turn on, or don’t want to.

    **[⬆ Back to Top](#table-of-contents)**

21. ### Allow for configuration and translation
    To keep your code maintainable and clean is to create a configuration object that contains all the things that are likely to change over time. These include any text used in elements you create (including button values and alternative text for images), CSS class and ID names and general parameters of the interface you build.

    It is of utmost importance to keep code maintenance simple, avoiding the need for future maintainers having to read all your code and find where they need to change things. 
    
    **[⬆ Back to Top](#table-of-contents)**

22. ### Avoid heavy nesting
    Nesting code explains its logic and makes it much easier to read, however nesting it too far can also make it hard to follow what you are trying to do. Readers of your code shouldn’t have to scroll horizontally, or suffer confusion when their code editors wrap long lines (this makes your indentation efforts moot anyway).

    The other problem of nesting is variable names and loops. As you normally start your first loop with i as the iterator variable, you’ll go on with j,k,l and so on. This can become messy quite quickly.

    In case of using the generic — really throw-away — variable names ul and li here, I might nestedul and datali for the nested list items. If the list nesting were to go even deeper I would need more variable names, and so on and so on. It makes more sense to put the task of creating nested lists for each member in its own function and call this with the right data. This also prevents us from having a loop inside a loop. Something like the addMemberData() function is pretty generic and is very likely to come in handy at another time.
  
    **[⬆ Back to Top](#table-of-contents)**

23. ### Optimize loops
    Loops can become very slow if you don’t do them right. One of the most common mistake is to read the length attribute of an array at every iteration, such as
    for(var i=0;i<names.length;i++)
    
    This means that every time the loop runs, JavaScript needs to read the length of the array. You can avoid that by storing the length value in a different           variable
    var all = names.length; for(var i=0;i<all;i++)
    
    An even shorter way of achieving this is to create a second variable in the pre-loop statement
    for(var i=0,j=names.length;i<j;i++)
    
    Another thing to ensure is that you keep computation-heavy code outside loops. This includes regular expressions and — more importantly — DOM manipulation. You can create the DOM nodes in the loop but avoid inserting them into the document. You’ll find more on DOM best practices in the next section.
  
    **[⬆ Back to Top](#table-of-contents)**

24. ### Keep DOM access to a minimum
    Accessing the DOM in browsers is an expensive thing to do. The DOM is a very complex API and rendering in browsers can take up a lot of time. You can see this when running complex web applications when your computer is already maxed out with other work — changes take longer or get shown half way through and so on.

    To make sure that your code is fast and doesn’t slow down the browser to a halt try to keep DOM access to a bare minimum. Instead of constantly creating and applying elements, have a tool function that turns a string into DOM elements and call this function at the end of your generation process to disturb the browser rendering once rather than continually.

    **[⬆ Back to Top](#table-of-contents)**

25. ### Don’t yield to browser whims
    Writing code specific to a certain browser is a sure-fire way to keep your code hard to maintain and make it get dated really quickly. If you look around the web you’ll find a lot of scripts that expect a certain browser and stop working as soon as a new version or another browser comes around.

    This is wasted time and effort — we should build code based on agreed standards as outlined in this course of articles, not for one browser. The web is for everybody, not an elite group of users with a state-of-the-art configuration. As the browser market moves quickly you will have to go back to your code and keep fixing it. This is neither effective nor fun.

    If something amazing works in one browser only and you really have to use it, put that code in its own script document and name it with browser and version. This means that you can find and remove this functionality more easily, should this browser become obsolete.

    **[⬆ Back to Top](#table-of-contents)**

26. ### Don’t trust any data
    Make sure that all the data that goes into the systems is clean and exactly what is needed. This is most important on the back end when writing out parameters retrieved from the URL. In JavaScript, it is very important to test the type of parameters sent to your functions (using the typeof keyword). For eg. If the function expects an array as an input, it will still work if you pass string to it, but if were to iterate over elements of array, now it would iterating over characters of the string.
    In order to make this work, you need to check the type of input and make sure it is an array: 
    if(typeof members === 'object' && 
        typeof members.slice === 'function')
    Arrays are tricky as they tell you they are objects. To ensure that they are arrays, check one of the methods only arrays have.

    Another very insecure practice is to read information from the DOM and use it without comparison. For example, I once had to debug some code that caused the JavaScript functionality to break. The code that caused it was — for some reason beyond me — reading a user name out of the innerHTML from a page element and calling a function with the data as a parameter. As the user name could be any UTF-8 character this included quotation marks and single quotes. These would end any string and the remaining part would be erroneous data. In addition, any user changing the HTML using a tool like Firebug or Opera DragonFly could change the user name to anything and inject this data into your functions.

    The same applies to forms that validate only on the client side. I once signed up for an unavailable email address by rewriting a select to provide another option. As the form wasn’t checked on the back end the process went through without a hitch.

    For DOM access, check that the element you try to reach and alter is really available and what you expect it to be — otherwise your code may fail or cause strange rendering bugs.

    **[⬆ Back to Top](#table-of-contents)**

27. ### Add functionality with JavaScript, don’t create too much content
    Building a lot of HTML in JavaScript can be pretty daunting and flaky. Especially on Internet Explorer you can run into all kinds of trouble by altering the document while it is still loading and manipulating the content with innerHTML.

    In terms of page maintenance it is also a terribly bad idea to create a lot of markup with HTML as not every maintainer will have the same level of skill as you have and could potentially really mess with your code.

    I found that when I had to build an application that is very much dependent on JavaScript, using an HTML template and loading this template via Ajax made much more sense. That way maintainers can alter the HTML structure and most importantly text without having to interfere with your JavaScript code.

    For example, defining a script to load the template when the correct HTML container is available and apply the event handlers in the setupContent() method afterwards:

        if(playercontainer){

            ajax('template.html');

        };
        .
        .
        request.onreadystatechange = function(){

       if(request.readyState == 4){

          if(request.status){ 

            if(request.status === 200 || request.status === 304){

              if(url === 'template.html'){

                setupPlayer(request.responseText);

              }

            }

          } else {

            alert('Error: Could not find template...');

          }

        }
  
    This way people can translate and change the template any way they want to without having to alter the JavaScript code.

    **[⬆ Back to Top](#table-of-contents)**
    
28. ### Build on the shoulders of giants
    It’s a good idea to learn JavaScript without libraries first, to understand what’s going on, but it is better to make use of a JS library when starting to  develop web sites. There would be less issues to deal with and at least the bugs that appear will be ones that can be reproduced — not random browser issues.

    **[⬆ Back to Top](#table-of-contents)**

29. ### Development code is not live code
    Stop optimizing code for machines rather than other developers. A build script can remove whitespace, comments, replace strings with Array lookups (to avoid MSIE creating a string object for every single instance of a string — even in conditions) and do all the other small tweaks needed to make our JavaScript fly in browsers.

    If we concentrate more on making the initial code easy to understand and extend by other developers we can create the perfect build script. If we keep optimizing prematurely we’ll never get there. Do not build for yourself or the browser — build for the next developer who takes over from you.

    **[⬆ Back to Top](#table-of-contents)**

30. ### Don't Use Shorthand
    Technically, you can get away with omitting most curly braces and semi-colons. Most browsers will correctly interpret the following:
        
        if (someVariableExists)
           x = false
           
        However, consider this:
        if (someVariableExists)
           x = false
           anotherFunctionCall();
           
        You might think that the code above would be equivalent to:
        if (someVariableExists) {
           x = false;
           anotherFunctionCall();
        }
        
        Unfortunately, you'd be wrong. In reality, it means:
        if (someVariableExists) {
           x = false;
        }
        anotherFunctionCall();
        
        As you'll notice, the indentation mimics the functionality of the curly brace. Needless to say, this is a terrible practice that should be avoided at all costs. The only time that curly braces should be omitted is with one-liners, and even this is a highly debated topic.

        if(2 + 2 === 4) return 'nicely done';

    **[⬆ Back to Top](#table-of-contents)**

31. ### Place Scripts at the Bottom of Your Page
    Remember—the primary goal is to make the page load as quickly as possible for the user. When loading a script, the browser can't continue until the entire file has been loaded. Thus, the user will have to wait longer before noticing any progress.

    If you have JS files whose only purpose is to add functionality—for example, after a button is clicked—go ahead and place those files at the bottom, just before the closing body tag. This is absolutely a best practice.

    **[⬆ Back to Top](#table-of-contents)**

32. ### Declare Variables Outside of the Loops
    When executing lengthy for statements, don't make the engine work any harder than it must. For example:

    let container = document.getElementById('container');
    for(let i = 0, len = someArray.length; i < len;  i++) {
       container.innerHtml += 'my number: ' + i;
       console.log(i);
    }

    **[⬆ Back to Top](#table-of-contents)**

33. ### The Fastest Way to Build a String
    Don't always reach for your handy-dandy for statement when you need to loop through an array or object. Be creative and find the quickest solution for the job at hand.

    let arr = ['item 1', 'item 2', 'item 3', ...];
    let list = '<ul><li>' + arr.join('</li><li>') + '</li></ul>';
    I won’t bore you with benchmarks; you’ll just have to believe me (or test for yourself). This is by far the fastest method!

    Using native methods like join(), regardless of what’s going on behind the abstraction layer, is usually much faster than any non-native alternative. — James Padolsey, james.padolsey.com

    **[⬆ Back to Top](#table-of-contents)**

34. ### Use Template Literals
    Strings that we create with double or single quotes have a lot of limitations. You might want to replace some of your strings with template literals to make working with them a lot easier. Template literals are created using the backtick character (`), and they offer many advantages. You can put expressions inside them or create multi-line strings.

    let person = 'Monty';
    let fruits = 'apples';
    let activity = 'playing games';
    let day = 'Monday';
    let sentence1 = person + ' will be eating ' + fruits + ' and ' + activity + ' on ' + day + '.';
    console.log(sentence1);
    // Output: Monty will be eating apples and playing games on Monday. 
    let sentence2 = `${person} will be eating ${fruits} and ${activity} on ${day}.`;
    console.log(sentence2);
    // Output: Monty will be eating apples and playing games on Monday.
    As you can see, we did not have to constantly move in and out of our template literal, as we had to with a regular string literal created with single or double quotes. This reduces the chances of any typing-related errors and helps us write cleaner code.

    **[⬆ Back to Top](#table-of-contents)**

35. ### Don't Pass a String to setInterval or setTimeOut
    Consider the following code:

    setInterval(
    "document.getElementById('container').innerHTML += 'My new number: ' + i", 3000
    );
    Not only is this code inefficient, but it also functions in the same way as the eval function would. Never pass a string to setInterval and setTimeOut. Instead, pass a function name.

    setInterval(someFunction, 3000); 

    **[⬆ Back to Top](#table-of-contents)**

36. ### Use {} Instead of new Object()
    There are multiple ways to create objects in JavaScript. Perhaps the more traditional method is to use the new constructor, like so:

    var o = new Object();
    o.name = 'Jeffrey';
    o.lastName = 'Way';
    o.someFunction = function() {
       console.log(this.name);
    }
    However, this method receives the "bad practice" stamp. It's not actually harmful, but it is a bit verbose and unusual. Instead, I recommend that you use the object literal method.

    Better
    var o = {
       name: 'Jeffrey',
       lastName = 'Way',
       someFunction : function() {
          console.log(this.name);
       }
    };
    Note that if you simply want to create an empty object, {} will do the trick.

    var o = {};
    "Object literals enable us to write code that supports lots of features yet still provide a relatively straightforward process for the implementers of our code. No need to invoke constructors directly or maintain the correct order of arguments passed to functions." — dyn-web.com


    **[⬆ Back to Top](#table-of-contents)**

37. ### Use [] Instead of new Array()
    The same applies for creating a new array.

    Okay
    var a = new Array();
    a[0] = "Joe";
    a[1] = 'Plumber';
    
    Better
    var a = ['Joe','Plumber'];
    "A common error in JavaScript programs is to use an object when an array is required or an array when an object is required. The rule is simple: when the property names are small sequential integers, you should use an array. Otherwise, use an object." — Douglas Crockford

    **[⬆ Back to Top](#table-of-contents)**

38. ### Use the Spread Operator
    Have you ever been in a situation where you wanted to pass all the items of an array as individual elements to some other function or you wanted to insert all the values from one array into another? The spread operator (...) allows us to do exactly that. Here is an example:

    let people = ["adam", "monty", "andrew"]
    let more_people = ["james", "jack", ...people, "sajal"]
    console.log(more_people)
    // Output: Array(6) [ "james", "jack", "adam", "monty", "andrew", "sajal" ]

    **[⬆ Back to Top](#table-of-contents)**

39. ### Be Careful With for ... in Statements
    When looping through items in an object, you might find that you retrieve method functions or other inherited properties as well. In order to work around this, always wrap your code in an if statement which filters with hasOwnProperty.

    for (key in object) {
       if (object.hasOwnProperty(key) {
          ...then do something...
       }
    }
    This tip is from JavaScript: The Good Parts, by Douglas Crockford.

    **[⬆ Back to Top](#table-of-contents)**
    
40. ### Self-Executing Functions
    Rather than calling a function, it's quite simple to make a function run automatically when a page loads or a parent function is called. Simply wrap your function in parentheses, and then append an additional set, which essentially calls the function.

    (function doSomething() {
       return {
          name: 'jeff',
          lastName: 'way'
       };
    })();

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
    Another essential feature added to JavaScript recently is arrow functions. They come with a slew of benefits. To begin with, they make the functional elements of JavaScript more appealing to the eye and easier to write.

    Take a look at how we would implement a filter without arrow functions:

    const nums = [1,2,3,4,5,6,7,8];
    const even_nums = nums.filter( function (num) { return num%2 == 0; } )
    Here, the callback function we pass to the filter returns true for any even number.

    Arrow functions make this much more readable and concise though: 

    const nums = [1,2,3,4,5,6,7,8];
    const even_nums = nums.filter(num => num%2 == 0)
    Another notable benefit of arrow functions is that they do not define a scope, instead being within the parent scope. This prevents many of the issues that can occur when using the this keyword. There are no bindings for this in the arrow functions. this has the same value inside the arrow function as it does in the parent scope. However, this means arrow functions can't be used as constructors or methods.

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
