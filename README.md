# php Interview Questions

### Table of Contents

| No. | Questions |
|-----|-----------|
| 1 | [How can you pass a variable by reference?](#How-can-you-pass-a-variable-by-reference) |
| 2 | [What does $GLOBALS mean?](#What-does-\$GLOBALS-mean)|
| 3 | [What is the difference between == and ===?](#What-is-the-difference-between-==-and===?)|
| 4 | [What is the use of ini_set()?](#What-is-the-use-of-ini_set()?)

1. ### How can you pass a variable by reference
   To be able to pass a variable by reference, we use an ampersand in front of it, as follows:
```
$var1 = &$var2
```
 **[⬆ Back to Top](#table-of-contents)**

2. ### What does $GLOBALS mean
    $GLOBALS is associative array including references to all variables which are currently defined in the global scope of the script.

 **[⬆ Back to Top](#table-of-contents)**

3. ### What is the difference between == and ===?
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