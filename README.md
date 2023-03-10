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
| 19   | [Modularize ??? one function per task](#modularize--one-function-per-task)                                         |
| 20   | [Enhance progressively](#enhance-progressively)                                         |
| 21   | [Allow for configuration and translation](#allow-for-configuration-and-translation)                                         |
| 22   | [Avoid heavy nesting](#avoid-heavy-nesting)                                         |
| 23   | [Optimize loops](#optimize-loops)                                         |
| 24   | [Keep DOM access to a minimum](#keep-DOM-access-to-a-minimum)                                         |
| 25   | [Don???t yield to browser whims](#dont-yield-to-browser-whims)                                         |
| 26   | [Don???t trust any data](#dont-trust-any-data)                                         |
| 27   | [Add functionality with JavaScript, don???t create too much content](#add-functionality-with-javaScript-dont-create-too-much-content)                                         |

1. ### Avoid Global Variables

    Minimize the use of global variables.

    This includes all data types, objects, and functions.

    Global variables and functions can be overwritten by other scripts.

    Use local variables or closures instead.

      **[??? Back to Top](#table-of-contents)**

2. ### Always Declare Local Variables

    All variables used in a function should be declared as local variables.
    
    Local variables must be declared with the let or const keyword, otherwise they will become global variables.

      **[??? Back to Top](#table-of-contents)**
      
3. ### Declarations on Top

    All declarations should be at the top of each script or function.

    This will:
    - Provide a single place to look for local variables
    - Make it easier to avoid unwanted (implied) global variables
    - Reduce the possibility of unwanted re-declarations

      **[??? Back to Top](#table-of-contents)**
      
4. ### Initialize Variables

     All variables should be initialized at the time of declaration.

     This will:
      - Provide a single place to initialize variables
      - Avoid undefined values

      **[??? Back to Top](#table-of-contents)**

5. ### Declare Objects with const
      Declaring objects with const will prevent any accidental change.

      **[??? Back to Top](#table-of-contents)**

6. ### Declare Arrays with const
    Declaring arrays with const will prevent any accidental change.

      **[??? Back to Top](#table-of-contents)**

7. ### Don't Use new Object
    - Use "" instead of new String()
    - Use 0 instead of new Number()
    - Use false instead of new Boolean()
    - Use {} instead of new Object()
    - Use [] instead of new Array()
    - Use /()/ instead of new RegExp()
    - Use function(){} instead of new Function()

      **[??? Back to Top](#table-of-contents)**
      
8. ### Beware of Automatic Type Conversions
    - JavaScript is loosely typed.
    A variable can contain all data types.

    - A variable can change its data type:
    Beware that numbers can accidentally be converted to strings or NaN (Not a Number).

    - When doing mathematical operations, JavaScript can convert numbers to strings:
    Subtracting a string from a string, does not generate an error but returns NaN (Not a Number).

      **[??? Back to Top](#table-of-contents)**
      
9. ### Use === Comparison
    The == comparison operator always converts (to matching types) before comparison.

      **[??? Back to Top](#table-of-contents)**
      
10. ### Use Parameter Defaults
    If a function is called with a missing argument, the value of the missing argument is set to undefined.

    Undefined values can break the code. It is a good habit to assign default values to arguments.

      **[??? Back to Top](#table-of-contents)**
      
11. ### End Your Switches with Defaults
    Always end your switch statements with a default. Even if you think there is no need for it.

      **[??? Back to Top](#table-of-contents)**
      
12. ### Avoid Number, String, and Boolean as Objects
    Always treat numbers, strings, or booleans as primitive values. Not as objects.

    Declaring these types as objects, slows down execution speed, and produces nasty side effects.

      **[??? Back to Top](#table-of-contents)**
      
13. ### Avoid Using eval()
    The eval() function is used to run text as code. In almost all cases, it should not be necessary to use it.

    Because it allows arbitrary code to be run, it also represents a security problem.

      **[??? Back to Top](#table-of-contents)**

14. ### Call things by their name
    Good variable and function names should be easy to understand and tell you what is going on ??? not more and not less. 

      **[??? Back to Top](#table-of-contents)**

15. ### Stick to a strict coding style
    Clean and valid code means less confusing bugs to fix, easier handover to other developers and better code security. When you rely on hacks to get your code to work it is likely that there is also a security exploit that uses the same hacks. In addition, as hacks get fixed in browsers, your code will cease to work in the next version of the browser.

    Valid code also means that it can be converted by scripts to other formats ??? hacky code will need a human to do that.

      **[??? Back to Top](#table-of-contents)**

16. ### Comment as much as needed but not more
    Comments are your messages to other developers (and yourself, if you come back to your code after several months working on something else). There???s been numerous battles raging over the years about whether to use comments at all, the main argument being that good code should explain itself.

    Again the trick is moderation. Comment when there is an important thing to say, and if you do comment use the /* */ notation. Single line comments using // can be problematic if people minify your code without stripping comments and in general are less versatile.

      **[??? Back to Top](#table-of-contents)**

17. ### Avoid mixing CSS or styling with other technologies
    Whilst it is possible to create everything you need in a document using JavaScript, CSS and manipulating the DOM, it is not necessarily the most effective way of doing so. 
    
    Adding the code to put a red border around every input field when its class is ???mandatory??? and there???s nothing in it through Javascript is possible, however it means that if you later need to make a change to these styles you need to go through the JavaScript and apply the changes there. By adding a class called ???error??? to the element when there is an error, you can ensure that the styling information is kept inside the CSS, which is more appropriate.

     **[??? Back to Top](#table-of-contents)**

18. ### Use shortcut notation when it makes sense
    Instead of repeating the object name for each property or method and assigning values through '.', make use of object literal and assign values through '{}'.
    
    Conditions can be shortened using ???ternary notation???. Anything before the question mark is the condition, the value immediately after it is the true case and the one after the colon the false case. Ternary notation can be nested, but I???d avoid that to keep things readable.
    
    Another common situation in JavaScript is providing a preset value for a variable if it is not defined through '||' the double pipe character. For eg. x || 5 will capture value of x if x is present, otherwise it will take 5.
    
     **[??? Back to Top](#table-of-contents)**

19. ### Modularize ??? one function per task
    Create functions that fulfill one job at a time which makes it easy for other developers to debug and change the code without having to scan through all the code to work out what code block performs what function.

    This also applies to creating helper functions for common tasks. If you find yourself doing the same thing in several different functions then it is a good idea to create a more generic helper function instead, and reuse that functionality where it is needed.
    
     **[??? Back to Top](#table-of-contents)**

20. ### Enhance progressively
    Write code that works regardless of available technology. In the case of JavaScript, this means that when scripting is not available (say on a BlackBerry, or because of an over-zealous security policy) your web products should still allow users to reach a certain goal, not block them because of the lack of JavaScript which they can???t turn on, or don???t want to.

    **[??? Back to Top](#table-of-contents)**

21. ### Allow for configuration and translation
    To keep your code maintainable and clean is to create a configuration object that contains all the things that are likely to change over time. These include any text used in elements you create (including button values and alternative text for images), CSS class and ID names and general parameters of the interface you build.

    It is of utmost importance to keep code maintenance simple, avoiding the need for future maintainers having to read all your code and find where they need to change things. 
    
    **[??? Back to Top](#table-of-contents)**

22. ### Avoid heavy nesting
    Nesting code explains its logic and makes it much easier to read, however nesting it too far can also make it hard to follow what you are trying to do. Readers of your code shouldn???t have to scroll horizontally, or suffer confusion when their code editors wrap long lines (this makes your indentation efforts moot anyway).

The other problem of nesting is variable names and loops. As you normally start your first loop with i as the iterator variable, you???ll go on with j,k,l and so on. This can become messy quite quickly.

    In case of using the generic ??? really throw-away ??? variable names ul and li here, I might nestedul and datali for the nested list items. If the list nesting were to go even deeper I would need more variable names, and so on and so on. It makes more sense to put the task of creating nested lists for each member in its own function and call this with the right data. This also prevents us from having a loop inside a loop. Something like the addMemberData() function is pretty generic and is very likely to come in handy at another time.
  
    **[??? Back to Top](#table-of-contents)**

23. ### Optimize loops
    Loops can become very slow if you don???t do them right. One of the most common mistake is to read the length attribute of an array at every iteration, such as
    for(var i=0;i<names.length;i++)
    
    This means that every time the loop runs, JavaScript needs to read the length of the array. You can avoid that by storing the length value in a different           variable
    var all = names.length; for(var i=0;i<all;i++)
    
    An even shorter way of achieving this is to create a second variable in the pre-loop statement
    for(var i=0,j=names.length;i<j;i++)
    
    Another thing to ensure is that you keep computation-heavy code outside loops. This includes regular expressions and ??? more importantly ??? DOM manipulation. You can create the DOM nodes in the loop but avoid inserting them into the document. You???ll find more on DOM best practices in the next section.
  
    **[??? Back to Top](#table-of-contents)**

24. ### Keep DOM access to a minimum
    Accessing the DOM in browsers is an expensive thing to do. The DOM is a very complex API and rendering in browsers can take up a lot of time. You can see this when running complex web applications when your computer is already maxed out with other work ??? changes take longer or get shown half way through and so on.

    To make sure that your code is fast and doesn???t slow down the browser to a halt try to keep DOM access to a bare minimum. Instead of constantly creating and applying elements, have a tool function that turns a string into DOM elements and call this function at the end of your generation process to disturb the browser rendering once rather than continually.

    **[??? Back to Top](#table-of-contents)**

25. ### Don???t yield to browser whims
    Writing code specific to a certain browser is a sure-fire way to keep your code hard to maintain and make it get dated really quickly. If you look around the web you???ll find a lot of scripts that expect a certain browser and stop working as soon as a new version or another browser comes around.

    This is wasted time and effort ??? we should build code based on agreed standards as outlined in this course of articles, not for one browser. The web is for everybody, not an elite group of users with a state-of-the-art configuration. As the browser market moves quickly you will have to go back to your code and keep fixing it. This is neither effective nor fun.

    If something amazing works in one browser only and you really have to use it, put that code in its own script document and name it with browser and version. This means that you can find and remove this functionality more easily, should this browser become obsolete.

    **[??? Back to Top](#table-of-contents)**

26. ### Don???t trust any data
    One of the main points to bear in mind when talking about code and data security is not to trust any data. This is not only about evil people wanting to hack your systems; it starts with plain usability. Users will enter incorrect data, all the time. Not because they are stupid, but because they are busy, distracted or the wording on your instructions is confusing them. For example, Booking a hotel room for a month rather than six days beacuse of entering a wrong number 

    In short, make sure that all the data that goes into your systems is clean and exactly what you need. This is most important on the back end when writing out parameters retrieved from the URL. In JavaScript, it is very important to test the type of parameters sent to your functions (using the typeof keyword). For eg. If the function expects an array as an input, it will still work if you pass string to it, but if were to iterate over elements of array, now it would iterating over characters of the string.
In order to make this work, you need to check the type of input and make sure it is an array: 
if(typeof members === 'object' && 
     typeof members.slice === 'function')
Arrays are tricky as they tell you they are objects. To ensure that they are arrays, check one of the methods only arrays have.

    Another very insecure practice is to read information from the DOM and use it without comparison. For example, I once had to debug some code that caused the JavaScript functionality to break. The code that caused it was ??? for some reason beyond me ??? reading a user name out of the innerHTML from a page element and calling a function with the data as a parameter. As the user name could be any UTF-8 character this included quotation marks and single quotes. These would end any string and the remaining part would be erroneous data. In addition, any user changing the HTML using a tool like Firebug or Opera DragonFly could change the user name to anything and inject this data into your functions.

    The same applies to forms that validate only on the client side. I once signed up for an unavailable email address by rewriting a select to provide another option. As the form wasn???t checked on the back end the process went through without a hitch.

    For DOM access, check that the element you try to reach and alter is really available and what you expect it to be ??? otherwise your code may fail or cause strange rendering bugs.

    **[??? Back to Top](#table-of-contents)**

27. ### Add functionality with JavaScript, don???t create too much content
    Building a lot of HTML in JavaScript can be pretty daunting and flaky. Especially on Internet Explorer you can run into all kinds of trouble by altering the document while it is still loading and manipulating the content (look up ???operation aborted error??? on Google for a tale of woe and misery) with innerHTML.

    In terms of page maintenance it is also a terribly bad idea to create a lot of markup with HTML as not every maintainer will have the same level of skill as you have and could potentially really mess with your code.

    I found that when I had to build an application that is very much dependent on JavaScript using an HTML template and loading this template via Ajax made much more sense. That way maintainers can alter the HTML structure and most importantly text without having to interfere with your JavaScript code. The only snag is to tell them which IDs are needed and if there are certain HTML constructs that need to be in the order you defined. You can do that with inline HTML comments (and then strip the comments out when you load the template. Check the source of the Easy YouTube template as an example.

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
      }else{
        alert('Error: Could not find template...');
      }
    }
  
    This way people can translate and change the template any way they want to without having to alter the JavaScript code.



    **[??? Back to Top](#table-of-contents)**
