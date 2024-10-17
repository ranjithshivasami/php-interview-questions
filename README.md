
# php Interview Questions

### Table of Contents


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
      * 
**[⬆ Back to Top](#table-of-contents)**

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
      |$x = "false";| string| false	|false|	true	|true|

**[⬆ Back to Top](#table-of-contents)**

13. ### What is stdClass in PHP?
      **stdClass** is just a generic **'empty'** class that's used when casting other types to objects. **stdClass** is not the base class for objects in PHP. This can be demonstrated fairly

      ```
      class Foo{}
      $foo = new Foo();
      echo ($foo instanceof stdClass)?'Y':'N'; // outputs 'N'
      ```
**[⬆ Back to Top](#table-of-contents)**

14. ### What's the difference between isset() and array_key_exists()?

* array_key_exists will tell you if a key exists in an array and complains when $a does not exist.
* isset will only return true if the key/variable exists and is not null. isset doesn't complain when $a does not exist.

```
$a = array('key1' => 'Foo Bar', 'key2' => null);

isset($a['key1']);             // true
array_key_exists('key1', $a);  // true

isset($a['key2']);             // false
array_key_exists('key2', $a);  // true
```

**[⬆ Back to Top](#table-of-contents)**

15. ### What is the difference between var_dump() and print_r()?

* The var_dump function displays structured information about variables/expressions including its type and value. Arrays are explored recursively with values indented to show structure. It also shows which array values and object properties are references.

* The print_r() displays information about a variable in a way that's readable by humans. array values will be presented in a format that shows keys and elements. Similar notation is used for objects.

   ```
   $obj = (object) array('qualitypoint', 'technologies', 'India');
   ```
   var_dump($obj)will display below output in the screen:

   ```
   object(stdClass)#1 (3) {
   [0]=> string(12) "qualitypoint"
   [1]=> string(12) "technologies"
   [2]=> string(5) "India"
   }
   ```
   And, print_r($obj) will display below output in the screen.

   ```
   stdClass Object ( 
   [0] => qualitypoint
   [1] => technologies
   [2] => India
   )
   ```

**[⬆ Back to Top](#table-of-contents)**

16. ### Give me some real life examples when you had to use __destruct in your classes

   We know that __destruct is called when the object is destroyed. Logically, what happens if the object is destroyed? Well, it means it's no longer available. So if it has resources open, it makes sense to close those resources as it's being destroyed or cleaning up after itself. Also because PHP will close resources on termination for you doesn't mean that it's bad to explicitly close them when you no longer need them (or good to not close them).

   Some real examples are:

* Closing custom database connector/wrapper connection
* Deletion of temporary folders
* Cleaning up caching
* Spooling the queue of logging messages to db/file

**[⬆ Back to Top](#table-of-contents)**

17. ### What is a class?

   A class is a template for an object, a user-defined datatype that contains variables, properties, and methods.

   Class represents all properties and behaviors of object.

   ```
   class Person{
    public $name;
    public $age;
    function __construct($name, $age){
        $this->name = $name;
        $this->age = $age;
    }
    function getUserDetails(){
        return "Hi, My Name is ".$this->name." and I'm ". $this->age ." old 
   ";
      }
   }
   //To create php object we have to use a new operator. 

   $obj = new Person("Ajay", 23);
   echo $obj->getUserDetails();

   //Output:
   Hi, My Name is Ajay and I'm 23 old 
   ```

18. ### What is an object?

   Objects are created from Classes, is an instance of a class that is created dynamically.

   Object in programming is similar to real word object. Every programming object has some properties and behaviors.

   You can create object of class with the help of new keyword

   ```
      //Create an object of MyClas 
   $obj = new MyClass();
   OR
   $obj = new MyClass;
   ```
19. ### What is Constructor and Destructor?

   **Constructor:**

   Constructor is a special type of function which will be called automatically whenever there is any object created from a class.

   ```
   class myClass{
      function __construct(){
         // Define logic in constructor
      }
   }
   ```

 **Destructor:**

   Destructor is a special type of function which will be called automatically whenever any object is deleted or goes out of scope.

   ```
   class myClass{
      function __construct(){
      // Define logic in constructor
      }
      function __destruct(){
      // this is destructor 
      }
   }
   ```
20. ### What is Member Variable and Member function?

   **Member Variable** − These are the variables defined inside a class. This data will be invisible to the outside of the class and can be accessed via member functions. These variables are called attribute of the object once an object is created.

   **Member function** − These are the function defined inside a class and are used to access object data.

   ```
   <?php
   class Books {
      /* Member variables */
      public $price;
      public $title;
      
      /* Member functions */
      function setPrice($par){
         $this->price = $par;
      }
      
      function getPrice(){
         echo $this->price ."<br/>";
      }
      
      function setTitle($par){
         $this->title = $par;
      }
      
      function getTitle(){
         echo $this->title ." <br/>";
      }
   }
   ```
21. ### What is different types of Visibility? OR What are access modifiers?

   Each method and property has its visibility. There are three types of visibility in PHP.

   Types of visibility:

1. **public:** Public method or variable can be accessible from anywhere, Means a public method or variable of a class can be called outside of the class or in a subclass.
1. **protected:** A protected method or variable can only be called in that class & it's subclass.
1. **private:** A private method or variable of a class can only be called inside that class only in which it is declared.

NOTE: By default, in PHP, a class member is public unless declared private or protected.

22. ### What is Encapsulation?

   ```Wrapping up member variables and methods together into a single unit (i.e. Class) is called Encapsulation.```

1. Encapsulation is used to hide the values or state of a structured data object inside a class, preventing unauthorized parties' direct access to them.
1. Visibility is the mechanism for encapsulation.

```
class Person {
	private $name;

	public function setName($name) {
		$this->name = $name;
	}

	public function getName($name) {
		return $this->name;
	}
}

$personObj = new Person();
$personObj->setName('Full Stack Tutorials');
$personObj->getName();
```
23. ### What is Abstraction?

   ```Abstraction is a concept in which implementation details are hidden.```

   **Abstract Class:**

   ```Abstract class are class which contains atleast one or more abstract method.```

   **Abstract Method:**

   ```Abstract method is a method which is declared, but not defined.```

1. PHP 5 introduces abstract classes and methods.
1. Classes defined as abstract may not be instantiated
1. Classes that contains at least one abstract method must also be abstract.
1. Methods defined as abstract simply declare the method's signature - they cannot define the implementation. Abstract methods cannot be defined as private.
1. Classes which are inheriting it's parent class must provides implementations for the abstract methods.

24. ### PHP Namespaces

   Namespaces are qualifiers that solve two different problems:

1. They allow for better organization by grouping classes that work together to perform a task
2. They allow the same name to be used for more than one class

## Best Practices for Securing API endpoints
<details>
  <summary>HTTPS always</summary>  
   If your API endpoints allow API consumers to talk over http or other non-secure protocols, you’re putting them at a big risk. Passwords, secret keys, and credit card information can easily get stolen as any man-in-the-middle attack, or packet sniffer tool can read them as plain text.

   So, always make https the only option available. No matter how trivial an endpoint might seem, connecting over http shouldn’t even be an option
</details>
<details>
  <summary>One-way password hashing</summary> 
  Passwords should never be stored as plain text, as in the event that a security breach occurs, all the user accounts will be compromised. At the same time, symmetric encryption should be strictly avoided, as any attacker ingenious and persistent enough will be able to break them.

   The only suggested option is asymmetric (or “one-way”) encryption algorithms for storing passwords. That way, neither an attacker nor any developer or sysadmin within the company will get to read customer passwords.
</details>
<details>
  <summary>Strong authentication</summary> 
 Now, almost every API has a form of authentication, but in my opinion, the OAuth2 system works the best. As opposed to other authentication methods, it divides your account into resources and allows only limited access to the auth token bearer.

At the same time, another very good practice to set tokens to expire every, say, 24 hours, so that they need to be refreshed. This way, even if your token gets leaked, there’s a chance that the 24-hour deadline will reduce the impact of the breach.
</details>
<details>
  <summary>Apply rate limiting</summary> 
Unless you have an API that’s used by millions of people every minute, it’s a very good idea to enforce a limit of how many calls a client can make to the API in a given time window.

This is mostly to discourage bots, which can keep sending hundreds of simultaneous requests every second and make your API eat up system resources for no good reason. All web development frameworks come with a rate-limiting middleware (and if not, it’s fairly easy to add it via a library) that takes just a minute or so to set up.
</details>
<details>
  <summary>Validate input</summary> 
This sounds like a no-brainer, but you’ll be surprised how many APIs fall for this. Validating input not just means checking that the incoming data is in a correct format, but also that no surprises are possible. A simple example is SQL injection, which can wipe out your databases if you let the query strings go by with little or no checking.

Another example is to validate the POST request size and return a proper error code and message to the client. Trying to accept and parse ridiculously large inputs will only serve to blow up the API.
</details>
<details>
  <summary>Enforce IP address filtering, if applicable</summary> 
If you’re into B2B services and your APIs are used by businesses from set locations, considering adding an extra layer of security that restricts IP addresses that can access your API. For every new location and new clients, the IP address will need to be checked against the incoming request.

Yes, it adds nuisance to onboarding, but the end result is much tighter security than can be otherwise achieved.
</details>
<details>
  <summary>Remove information that’s not meant to be shared</summary> 
Because APIs are essentially a developer’s tool, they often contain keys, passwords, and other information that should be removed before they’re made publicly available. But sometimes this step is overlooked. Organizations should incorporate scanning tools into their DevSecOps processes to limit accidental exposure of secret information.
</details>
<details>
  <summary>Don’t expose more data than necessary. </summary> 
Some APIs reveal far too much information, whether it’s the volume of extraneous data that’s returned through the API or information that reveals too much about the API endpoint. This typically occurs when an API leaves the task of filtering data to the user interface instead of the endpoint. Ensure that APIs only return as much information as is necessary to fulfill their function. In addition, enforce data access controls at the API level, monitor data, and obfuscate if the response contains confidential data.
</details>




---

### 1. **Describe how sessions work in PHP. What are some security best practices when managing sessions?**
   - **Sessions in PHP:** 
     - Sessions store user data across multiple page requests by using a unique session ID (stored in a cookie or passed via URL).
     - Data is stored on the server, and the session ID links the user to their data.
   - **Security Best Practices:**
     - Use `session_regenerate_id()` to prevent session fixation.
     - Set a short session timeout and use `session.cookie_secure` and `session.cookie_httponly` to enhance cookie security.
     - Implement HTTPS to encrypt session data.
     - Store minimal and non-sensitive data in session variables.

---

### 2. **How does PHP handle error reporting, and what are the different types of error levels?**
   - PHP has a built-in error reporting mechanism controlled via `error_reporting()` and `ini_set()`.
   - **Error Levels:**
     - `E_ERROR`: Fatal runtime errors.
     - `E_WARNING`: Non-fatal runtime warnings.
     - `E_NOTICE`: Minor issues, often non-critical.
     - `E_PARSE`: Compile-time parsing errors.
     - `E_STRICT`: Recommends improvements in code.
     - `E_DEPRECATED`: Warnings about deprecated code.

---

### 3. **What is the difference between interfaces and abstract classes in PHP? Provide examples of when to use each.**
   - **Interfaces:** Define method signatures but no implementation. Classes must implement all methods.
     - Use when multiple classes share behavior without inheriting the same structure.
   - **Abstract Classes:** Can have both defined methods and method signatures.
     - Use when there is a common base class but with shared behavior, allowing subclasses to provide specific implementations.

   ```php
   interface LoggerInterface {
       public function log($message);
   }

   abstract class AbstractLogger {
       public function log($message) {
           // Default implementation
       }
       abstract public function formatMessage($message);
   }
   ```

---

### 4. **What is SOLID in object-oriented programming, and how do you apply these principles in PHP?**
   - **SOLID Principles:**
     - **S**ingle Responsibility Principle: A class should have one responsibility.
     - **O**pen/Closed Principle: Classes should be open for extension but closed for modification.
     - **L**iskov Substitution Principle: Subtypes should be replaceable with their base types.
     - **I**nterface Segregation Principle: No client should be forced to depend on methods it does not use.
     - **D**ependency Inversion Principle: Depend on abstractions, not concretions.

   - **Application in PHP:**
     - Implement interfaces to follow the Dependency Inversion Principle.
     - Keep classes focused on single tasks.
     - Use design patterns (e.g., Factory, Strategy) to ensure adherence to OOP principles.

---

### 5. **Explain dependency injection in PHP. How does it contribute to better application design?**
   - **Dependency Injection (DI):** Passing dependencies (e.g., services, repositories) into an object instead of hard-coding them.
   - **Benefits:**
     - Promotes loose coupling and high testability.
     - Allows easy swapping of dependencies (e.g., swapping a database layer).

   ```php
   class UserController {
       private $userService;

       public function __construct(UserService $userService) {
           $this->userService = $userService;
       }
   }
   ```

---

### 6. **What are some common vulnerabilities in PHP applications (e.g., SQL Injection, XSS)? How do you mitigate them?**
   - **Common Vulnerabilities:**
     - **SQL Injection:** Use prepared statements or ORM (e.g., PDO).
     - **Cross-Site Scripting (XSS):** Sanitize and escape all user inputs using `htmlspecialchars()`.
     - **Cross-Site Request Forgery (CSRF):** Use anti-CSRF tokens for forms.
     - **File Inclusion Vulnerabilities:** Avoid direct user input in file paths.

---

### 7. **How do you build database queries in terms of security and performance?**
   - **Security:** 
     - Use prepared statements with bound parameters to prevent SQL injection.
     - Sanitize inputs and outputs properly.
   - **Performance:**
     - Optimize queries with indexes.
     - Avoid SELECT * and limit the number of rows fetched.
     - Use database caching and profiling tools.

---

### 8. **Importance of database indexing. How would you optimize a query using indexes in PHP?**
   - **Importance:** 
     - Indexes speed up data retrieval by creating efficient data structures.
   - **Optimization:**
     - Identify frequent query columns and apply indexes.
     - Use `EXPLAIN` to analyze query performance and optimize with compound indexes where necessary.

---

### 9. **How do you manage dependencies in large-scale PHP applications? What tools or patterns do you use?**
   - Use dependency injection with service containers (e.g., Laravel’s IoC container).
   - Utilize Composer for package management.
   - Implement modular design patterns (e.g., Repository, Factory, Service) to separate concerns and promote scalability.

---

### 10. **How would you approach a large-scale, high-concurrency application in PHP? What are the key areas to focus on?**
   - Focus Areas:
     - **Caching:** Use Redis or Memcached for caching data and sessions.
     - **Load Balancing:** Distribute traffic across multiple servers.
     - **Database Optimization:** Use master-slave replication or sharding for scalability.
     - **Queueing:** Use message queues (e.g., RabbitMQ) for task offloading.
     - **Asynchronous Processing:** Implement event-driven architecture with workers for background processing.

---

### 11. **How do you ensure that code reviews are effective in your code and peers? What tools and techniques do you use?**
   - **Techniques:** 
     - Establish clear guidelines for code quality (PSR standards).
     - Use static analysis tools (e.g., PHPStan, PHPCS).
     - Ensure code is covered with unit and integration tests.
     - Review small, focused changes to maintain clarity.

---

### 12. **As a lead developer, how would you balance meeting deadlines with ensuring code quality?**
   - Set realistic timelines and avoid feature creep.
   - Prioritize critical features while refactoring and improving code incrementally.
   - Use continuous integration to detect issues early and ensure code is always production-ready.

---

### 13. **How do you use Git to manage branching strategies in a development team? What are some best practices?**
   - **Branching Strategy:**
     - Use **Git Flow** or **GitHub Flow** for clear workflows.
     - Feature branches for new developments, hotfix branches for urgent fixes, and release branches for staging.
   - **Best Practices:**
     - Regularly merge and rebase to avoid large merges.
     - Write clear commit messages and document code changes.

---


 ## Video link for Namespaces
[<img src="./images/thumb.png" width="170" height="100">](https://www.youtube.com/watch?v=JIfNaqA4STg)


 # Video link for Object Oriented PHP Tutorial 
[<img src="https://i.ytimg.com/vi/Anz0ArcQ5kI/maxresdefault.jpg" width="170" height="100">](https://www.youtube.com/watch?v=Anz0ArcQ5kI&list=PL0eyrZgxdwhypQiZnYXM7z7-OTkcMgGPh)

