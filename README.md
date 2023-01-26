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
| 14   | [Stick to a strict coding style](#stick-to-a-strict-coding-style)                                         |

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
