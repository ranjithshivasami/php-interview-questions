
# php Interview Questions

### Table of Contents

| No. | Questions |
|-----|-----------|
| 1 | [How can you pass a variable by reference?](#How-can-you-pass-a-variable-by-reference) |
| 2 | [What does $GLOBALS mean?](#what-does-GLOBALS-mean)|
| 3 | [What is the difference between \== and \=== \?](#what-is-the-difference-between-and)|
| 4 | [What is the use of ini_set()?](#what-is-the-use-of-ini_set)|
| 5 | [Is multiple inheritance supported in PHP?](#is-multiple-inheritance-supported-in-PHP)
| 6 | [Differentiate between echo and print()](#differentiate-between-echo-and-print)
| 7 | [Explain how we handle exceptions in PHP?](#explain-how-we-handle-exceptions-in-PHP)|
| 8 |[What is PDO in PHP?](#What-is-PDO-in-PHP)|
| 9 |[What does the 'var' keyword mean in PHP?](#What-does-the-var-keyword-mean-in-PHP)|
| 10 |[Explain what the different PHP errors are](#Explain-what-the-different-PHP-errors-are)|
| 11 |[Is there a difference between isset and !empty?](#Is-there-a-difference-between-isset-and-!empty)|
| 12 |[When should I use require vs include?](#When-should-I-use-require-vs-include)|
| 15 |[What is stdClass in PHP?](#What-is-stdClass-in-PHP)|
| 16 |[What are PSRs? Choose 1 and briefly describe it.](#What-are-PSRs?-Choose-1-and-briefly-describe-it.)|
| 17 |[What's the difference between isset() and array_key_exists()? ](#What's-the-difference-between-isset()-and-array_key_exists())|
| 18 |[What is the difference between var_dump() and print_r()?](#What-is-the-difference-between-var_dump()-and-print_r())|
| 19 |[Give me some real life examples when you had to use __destruct in your classes](#Give-me-some-real-life-examples-when-you-had-to-use-__destruct-in-your-classes)|
| 20 |[Differentiate between echo and print()](#Differentiate-between-echo-and-print())|
| 21 |[Can you extend a Final defined class?](#Can-you-extend-a-Final-defined-class)|
| 22 |[What is the differences between $a != $b and $a !== $b?](#What-is-the-differences-between-\$a-!=-\$b-and-\$a-!==-\$b)|
| 23 |[What is the difference between single-quoted and double-quoted strings in PHP?](#What-is-the-difference-between-single-quoted-and-double-quoted-strings-in-PHP)|
| 24 |[What are the main differences between const vs define](#What-are-the-main-differences-between-const-vs-define)|
| 25 |[How is it possible to set an infinite execution time for PHP script?](#How-is-it-possible-to-set-an-infinite-execution-time-for-PHP-script)|
| 26 |[Explain usage of enumerations in PHP](#Explain-usage-of-enumerations-in-PHP)|
| 27 |[What are the differences between die() and exit() functions in PHP?](#What-are-the-differences-between-die()-and-exit()-functions-in-PHP)|
| 28 |[In PHP, objects are they passed by value or by reference?](#In-PHP,-objects-are-they-passed-by-value-or-by-reference)|
| 29 |[What are the different scopes of variables?](#What-are-the-different-scopes-of-variables)|
| 30 |[How can you enable error reporting in PHP?](#How-can-you-enable-error-reporting-in-PHP)|
| 31 |[Differentiate between exception and error](#Differentiate-between-exception-and-error)|
| 32 |[Explain function call by reference](#Explain-function-call-by-reference)|
| 33 |[Does PHP support method overloading?](#Does-PHP-support-method-overloading)|
| 34 |[What are some of the big changes PHP has gone through in the past few years?](#What-are-some-of-the-big-changes-PHP-has-gone-through-in-the-past-few-years)|
| 35 |[Why do we use extract()?](#Why-do-we-use-extract())|
| 36 |[Explain the difference between shell_exec() and exec()](#Explain-the-difference-between-shell_exec()-and-exec())|
| 37 |[Differentiate between parameterised and non parameterised functions](#Differentiate-between-parameterised-and-non-parameterised-functions)|
| 38 |[What is the difference between using self and $this?](#What-is-the-difference-between-using-self-and-\$this)|
| 39 |[What exactly is the the difference between array_map, array_walk and array_filter?](#What-exactly-is-the-the-difference-between-array_map,-array_walk-and-array_filter)|
| 40 |[Is there a function to make a copy of a PHP array to another?](#Is-there-a-function-to-make-a-copy-of-a-PHP-array-to-another)|
| 41 |[When should I use require_once vs require?](#When-should-I-use-require_once-vs-require)|
| 42 |[Are Parent constructors called implicitly inside a class constructor?](#Are-Parent-constructors-called-implicitly-inside-a-class-constructor)|
| 43 |[What is use of Null Coalesce Operator?](#What-is-use-of-Null-Coalesce-Operator)|
| 44 |[Maximum how many arguments are allowed in a function in PHP?](#Maximum-how-many-arguments-are-allowed-in-a-function-in-PHP)|
| 45 |[What is the difference between PDO's query() vs execute()?](#What-is-the-difference-between-PDO's-query()-vs-execute())|
| 46 |[Explain the difference between exec() vs system() vs passthru()?](#Explain-the-difference-between-exec()-vs-system()-vs-passthru())|
| 47 |[What is the difference between MySQL, MySQLi and PDO? ](#What-is-the-difference-between-MySQL,-MySQLi-and-PDO)|
| 48 |[What is autoloading classes in PHP?](#What-is-autoloading-classes-in-PHP)|
| 49 |[What are the exception class functions?](#What-are-the-exception-class-functions)|
| 50 |[Is there any reason to use strcmp() for strings comparison?](#Is-there-any-reason-to-use-strcmp()for-strings-comparison)|
| 51 |[What is the difference between a PHP interpreter and a PHP handler?](#What-is-the-difference-between-a-PHP-interpreter-and-a-PHP-handler)|
| 52 |[What does $$ mean?](#What-does-$$-mean)|
| 53 |[explain what is a closure in PHP and why does it use the â€œuseâ€ identifier?](#explain-what-is-a-closure-in-PHP-and-why-does-it-use-the-â€œuseâ€-identifier)|
| 54 |[What's better at freeing memory with PHP](#What's-better-at-freeing-memory-with-PHP)|
| 55 |[Compare MySQLi or PDO - what are the pros and cons?](#Compare-MySQLi-or-PDO---what-are-the-pros-and-cons)|
| 56 |[Does PHP have threading?](#Does-PHP-have-threading)|
| 57 |[Store an array as JSON or as a PHP serialized array?](#Store-an-array-as-JSON-or-as-a-PHP-serialized-array)|
| 58 |[What is use of Spaceship Operator?](#What-is-use-of-Spaceship-Operator)|
| 59 |[What are the disadvantages of using persistent connection in PDO?](#What-are-the-disadvantages-of-using-persistent-connection-in-PDO)|
| 60 |[What is the crucial difference between using traits versus interfaces?](#What-is-the-crucial-difference-between-using-traits-versus-interfaces)|
| 61 |[How to turn errors into exceptions in PHP?](#How-to-turn-errors-into-exceptions-in-PHP)|
| 62 |[What is the best method to merge two PHP objects?](#What-is-the-best-method-to-merge-two-PHP-objects)|
| 63 |[Explain the Exception Hierarchy introduced in PHP7](#Explain-the-Exception-Hierarchy-introduced-in-PHP7)|
| 64 |[What exactly are late static bindings in PHP?](#What-exactly-are-late-static-bindings-in-PHP)|
| 65 |[What does yield mean in PHP?](#What-does-yield-mean-in-PHP)|
| 66 |[Is PHP single or multi threaded?](#Is-PHP-single-or-multi-threaded)|
| 67 |[Explain the Order of Precedence for Traits in PHP](#Explain-the-Order-of-Precedence-for-Traits-in-PHP)|
| 68 |[What does a $$$ mean in PHP? ](#What-does-a-$$$-mean-in-PHP)|
| 69 |Are PDO prepared statements sufficient to prevent SQL injection?](#Are-PDO-prepared-statements-sufficient-to-prevent-SQL-injection)|

1. ### How can you pass a variable by reference
   To be able to pass a variable by reference, we use an ampersand in front of it, as follows:
```
$var1 = &$var2
```
 **[⬆ Back to Top](#table-of-contents)**

2. ### What does $GLOBALS mean
    $GLOBALS is associative array including references to all variables which are currently defined in the global scope of the script.

 **[⬆ Back to Top](#table-of-contents)**

3. ### What is the difference between == and === ?
   * The operator == casts between two different types if they are different
   * The === operator performs a 'typesafe comparison'
     
   That means that it will only return true if both operands have the same type and the same value.
   ```
   1 === 1: true
   1 == 1: true
   1 === "1": false // 1 is an integer, "1" is a string
   1 == "1": true // "1" gets casted to an integer, which is 1
   "foo" === "foo": true // both operands are strings and have the same value
   ```
 **[⬆ Back to Top](#table-of-contents)**

4. ### What is the use of ini_set()?
   PHP allows the user to modify some of its settings mentioned in php.ini using ini_set(). This function requires two string arguments. First one is the name of the setting to be modified and the second one is the new value to be assigned to it.

   Given line of code will enable the display_error setting for the script if it’s disabled.

   ```
   ini_set('display_errors', '1');
   ```

   We need to put the above statement, at the top of the script so that, the setting remains enabled till the end. Also, the values set via ini_set() are applicable, only to the current script. Thereafter, PHP will start using the original values from php.ini.

 **[⬆ Back to Top](#table-of-contents)**

5. ### Is multiple inheritance supported in PHP?
    PHP supports only single inheritance; it means that a class can be extended from only one single class using the keyword 'extended'.
 
 **[⬆ Back to Top](#table-of-contents)**

6. ### Differentiate between echo and print()
   echo and print are more or less the same. They are both used to output data to the screen.

    The differences are:
    * echo has no return value while print has a return value of 1 so it can be used in expressions.
    * echo can take multiple parameters (although such usage is rare) while print can take one argument.
    * echo is faster than print.
  
**[⬆ Back to Top](#table-of-contents)**

7. ### Explain how we handle exceptions in PHP

   When an exception is thrown, code following the statement will not be executed, and PHP will attempt to find the first matching catch block. If an exception is not caught, a PHP Fatal Error will be issued with an "Uncaught Exception". An exception can be thrown, and caught within PHP.

   To handle exceptions, code may be surrounded in a ```try``` block. Each try must have at least one corresponding ```catch block```. Multiple catch blocks can be used to catch different classes of exceptions. Exceptions can be thrown (or re-thrown) within a catch block.

   Consider

   ```
      try {
         print "this is our try block n";
         throw new Exception();
      } catch (Exception $e) {
         print "something went wrong, caught yah! n";
      } finally {
         print "this part is always executed n";
      }
   ```
**[⬆ Back to Top](#table-of-contents)**

8. ### What is PDO in PHP?
   PDO stands for PHP Data Object.

   It is a set of PHP extensions that provide a core PDO class and database, specific drivers. It provides a vendor-neutral, lightweight, data-access abstraction layer. Thus, no matter what database we use, the function to issue queries and fetch data will be same. It focuses on data access abstraction rather than database abstraction.

**[⬆ Back to Top](#table-of-contents)**

9. ### What does the 'var' keyword mean in PHP
   The var keyword creates a property in a class. Since PHP 5, it is equivalent to the public keyword.
   <p class="note"> <strong>Note </strong>: The var keyword is only used for compatibility reasons. Since PHP 5, the keywords private, protected and public should be used instead.</p>

   **[⬆ Back to Top](#table-of-contents)**

10. ### Explain what the different PHP errors are

      * A **notice** is a non-critical error saying something went wrong in execution, something minor like an undefined variable.
      * A **warning**  is given when a more critical error like if an include() command went to retrieve a non-existent file. In both this and the error above, the script would continue.
      * A **fatal error**  would terminate the code. Failure to satisfy a require() would generate this type of error, for example.

11. ### Is there a difference between isset and !empty

   ### Isset function
   ISSET checks the variable to see if it has been set. In other words, it checks to see if the variable is any value except NULL or not assigned a value. ISSET returns TRUE if the variable exists and has a value other than NULL. That means variables assigned a "", 0, "0", or FALSE are set, and therefore are TRUE for ISSET.

   **empty function**

   EMPTY checks to see if a variable is empty. Empty is interpreted as: "" (an empty string), 0 (integer), 0.0 (float)`, "0" (string), NULL, FALSE, array() (an empty array), and "$var;" (a variable declared, but without a value in a class.
   
|Expression|gettype()|empty()|is_null()|isset()|bool : if($x)|
|----------|---------|-------|---------|-------|-------------|
|$x = "";|string|true|false|true|false|
|$x = null;|NULL|true|true|false|false|
|var $x;|NULL|true|true|false|false|
|$x is undefined|NULL|true|true|false|false|
|$x = [];|array|true|false|true|false|
|$x = ['a', 'b'];|array|false|false|true|true|
|$x = false;|bool|true|false|true|false|
|$x = true;|bool|false|false|true|true|
|$x = 1;|int|false|false|true|true|
|$x = 42;|int|false|false|true|true|
|$x = 0;|int|true|false|true|false|
|$x = -1;|int|false|false|true|true|
|$x = "1";|string|false|false|true|true|
|$x = "0";|string|true|false|true|false|
|$x = "-1";|string|false|false|true|true|
|$x = "php";|string|false|false|true|true|
|$x = "true";|string|false|false|true|true|
|$x = "false";|string|false	false	true	true|