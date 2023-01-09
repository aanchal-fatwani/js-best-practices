# JavaScript Best Practices

### Table of Contents

| No. | Title                                                                                                                                                         |
| --- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1   | [Avoid Global Variables](#avoid-global-variables)                                         |
| 2   | [Always Declare Local Variables](#always-declare-local-variables)                                         |
| 3   | [Declarations on Top](#declarations-on-top)                                         |
| 4   | [Initialize Variables](#initialize-variables)                                         |
| 5   | [Declare Objects with const](#declare-objects-with-const)                                         |

1. ### Avoid Global Variables

    Minimize the use of global variables.

    This includes all data types, objects, and functions.

    Global variables and functions can be overwritten by other scripts.

    Use local variables instead, and learn how to use closures.

      **[⬆ Back to Top](#table-of-contents)**

2. ### Always Declare Local Variables

    All variables used in a function should be declared as local variables.
    
    Local variables must be declared with the var, the let, or the const keyword, otherwise they will become global variables.

      **[⬆ Back to Top](#table-of-contents)**
      
3. ### Declarations on Top

    It is a good coding practice to put all declarations at the top of each script or function.

    This will:

    - Give cleaner code
    - Provide a single place to look for local variables
    - Make it easier to avoid unwanted (implied) global variables
    - Reduce the possibility of unwanted re-declarations

      **[⬆ Back to Top](#table-of-contents)**
      
4. ### Initialize Variables

     It is a good coding practice to initialize variables when you declare them.

     This will:

      - Give cleaner code
      - Provide a single place to initialize variables
      - Avoid undefined values

      **[⬆ Back to Top](#table-of-contents)**

5. ### Declare Objects with const
      Declaring objects with const will prevent any accidental change.

      **[⬆ Back to Top](#table-of-contents)**
