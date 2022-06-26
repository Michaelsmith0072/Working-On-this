# Working-On-this
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="styles.css">
    </head>
    <body>
      <main id="main-doc">
        <section class="main-section" id="introduction"><header>Introduction</header>
        <article>
          <p>JavaScript is a cross-platform, object-oriented scripting language. It is a small and lightweight language. Inside a host environment (for example, a web browser), JavaScript can be connected to the objects of its environment to provide programmatic control over them.</P>
          <p>JavaScript contains a standard library of objects, such as Array, Date, and Math, and a core set of language elements such as operators, control structures, and statements. Core JavaScript can be extended for a variety of purposes by supplementing it with additional objects; for example:</p>
          <ul>
            <li>Client-side JavaScript extends the core language by supplying objects to control a browser and its Document Object Model (DOM). For example, client-side extensions allow an application to place elements on an HTML form and respond to user events such as mouse clicks, form input, and page navigation.</li>
            <li>
              Server-side JavaScript extends the core language by supplying objects relevant to running JavaScript on a server. For example, server-side extensions allow an application to communicate with a database, provide continuity of information from one invocation to another of the application, or perform file manipulations on a server.
            </li>
            </ul>
 </article>
        </section>
        <section class="main-section" id="what_you_should_already_know"><header>What You Should Already Know</header>
        <article><p>This guide assumes you have the following basic background:</p>
        <ul>
          <li>A general understanding of the Internet and the World Wide Web (WWW).</li>
          <li>Good working knowledge of HyperText Markup Language (HTML)</li>
          <li>Some programming experience. If you are new to programming, try one of the tutorials linked on the main page about JavaScript.
</li>
        </ul>
        </article>
         </section>
        <section class="main-section" id="javascript_and_java"><header>JavaScript And Java</header>
       <article>
           <p>JavaScript and Java are similar in some ways but fundamentally different in some others. The JavaScript language resembles Java but does not have Java's static typing and strong type checking. JavaScript follows most Java expression syntax, naming conventions and basic control-flow constructs which was the reason why it was renamed from LiveScript to JavaScript.</p>
    <p>In contrast to Java's compile-time system of classes built by declarations, JavaScript supports a runtime system based on a small number of data types representing numeric, Boolean, and string values. JavaScript has a prototype-based object model instead of the more common class-based object model. The prototype-based model provides dynamic inheritance; that is, what is inherited can vary for individual objects. JavaScript also supports functions without any special declarative requirements. Functions can be properties of objects, executing as loosely typed methods.</p>
<p>JavaScript is a very free-form language compared to Java. You do not have to declare all variables, classes, and methods. You do not have to be concerned with whether methods are public, private, or protected, and you do not have to implement interfaces. Variables, parameters, and function return types are not explicitly typed.</p>
</article> 
</section>
        <section class="main-section" id="hello_world"><header>Hello World</header>
        <article>To get started with writing JavaScript, open the Scratchpad and write your first "Hello world" JavaScript code:
            <code>function greetMe(yourName) { alert("Hello " + yourName); }
                greetMe("World"); </code><br/>
                Select the code in the pad and hit Ctrl+R to watch it unfold in your browser!
        </article>
    </section>


        <section class="main-section" id="variables"><header>Variables</header>
        <p>

            You use variables as symbolic names for values in your application. The names of variables, called identifiers, conform to certain rules.
        </p>
    <p>A JavaScript identifier must start with a letter, underscore (_), or dollar sign ($); subsequent characters can also be digits (0-9). Because JavaScript is case sensitive, letters include the characters "A" through "Z" (uppercase) and the characters "a" through "z" (lowercase).


    </p>
<p>
    You can use ISO 8859-1 or Unicode letters such as å and ü in identifiers. You can also use the Unicode escape sequences as characters in identifiers. Some examples of legal names are Number_hits, temp99, and _name.


</p>
</section>

        <section class="main-section" id="declaring_variables"><header>Declaring Variables</header>
            <article>You can declare a variable in three ways:
                <p>With the keyword var. For example,<code>var x = 42.</code>This syntax can be used to declare both local and global variables.</p>
<p>By simply assigning it a value. For example,

    <code>x = 42.</code>
    This always declares a global variable. It generates a strict JavaScript warning. You shouldn't use this variant.
</p>
<p>With the keyword let. For example,
    <code>let y = 13.</code>
</p>
</article>
        </section>

      <section class="main-section" id="variable_scope"><header>Variable Scope</header>
        <article>
         <p>
          When you declare a variable outside of any function, it is called a global variable, because it is available to any other code in the current document. When you declare a variable within a function, it is called a local variable, because it is available only within that function.</p>
         <p>JavaScript before ECMAScript 2015 does not have block statement scope; rather, a variable declared within a block is local to the function (or global scope) that the block resides within. For example the following code will log 5, because the scope of x is the function (or global context) within which x is declared, not the block, which in this case is an if statement.<code>if (true) { var x = 5; } console.log(x); // 5</code></p>
         <p>
           
This behavior changes, when using the let declaration introduced in ECMAScript 2015.
         </p>
         <code>if (true) { let y = 5; } console.log(y); // ReferenceError: y is
          not defined</code>
</article>

     </section>
       <section class="main-section" id="global_variables"><header>Global Variables</header>
        <article>
          <p>
            Global variables are in fact properties of the global object. In web pages the global object is window, so you can set and access global variables using the window.variable syntax.</p>
          <p>Consequently, you can access global variables declared in one window or frame from another window or frame by specifying the window or frame name. For example, if a variable called phoneNumber is declared in a document, you can refer to this variable from an iframe as parent.phoneNumber.</p>
         </article>
       </section>

      <section class="main-section" id="constants"><header>Constants</header>
        <article>
          <p>
            You can create a read-only, named constant with the const keyword. The syntax of a constant identifier is the same as for a variable identifier: it must start with a letter, underscore or dollar sign and can contain alphabetic, numeric, or underscore characters.</p>
          <code>const PI = 3.14;</code>
          <p>
            A constant cannot change value through assignment or be re-declared while the script is running. It has to be initialized to a value.</p>
          <p>The scope rules for constants are the same as those for let block scope variables. If the const keyword is omitted, the identifier is assumed to represent a variable.</p>
          <p>
            You cannot declare a constant with the same name as a function or variable in the same scope. For example</p>
          <code>// THIS WILL CAUSE AN ERROR function f() {}; const f = 5; // THIS
            WILL CAUSE AN ERROR ALSO function f() { const g = 5; var g;
            //statements }
</code>"However, object attributes are not protected, so the following statement is executed without problems.""
<code>const MY_OBJECT = {"key": "value"}; MY_OBJECT.key =
  "otherValue";</code>
</article>
      </section>

      <section class="main-section" id="data_types"><header>Data Types</header>
        <article>
        <p></p>
      <ul>
        <li> 
          <p>Six Data Types That Are Primitives</p>
          <ul>
            <li>Boolean. true and false</li>
            <li>null. A special keyword denoting a null value. Because JavaScript is case-sensitive, null is not the same as Null, NULL, or any other variant.</li>
            <li>undefined. A top-level property whose value is undefined.</li>
            <li>Number. 42 or 3.14159.
            </li>
            <li>String. "Howdy"</li>
            <li>Symbol (new in ECMAScript 2015). A data type whose instances are unique and immutable.
            </li>
          </ul></li>
        <li>
          "and Object"
        </li>
      </ul>
      "Although these data types are a relatively small amount, they enable you to perform useful functions with your applications. Objects and functions are the other fundamental elements in the language. You can think of objects as named containers for values, and functions as procedures that your application can perform."
    </article>
       </section>

      <section class="main-section" id="if..._else_statement"><header>If...Else Statement</header>
        <article>Use the if statement to execute a statement if a logical condition is true. Use the optional else clause to execute a statement if the condition is false. An if statement looks as follows:
<code>if (condition) { statement_1; } else { statement_2; }</code>
condition can be any expression that evaluates to true or false. See Boolean for an explanation of what evaluates to true and false. If condition evaluates to true, statement_1 is executed; otherwise, statement_2 is executed. statement_1 and statement_2 can be any statement, including further nested if statements.
<p>You may also compound the statements using else if to have multiple conditions tested in sequence, as follows:</p>
<code>if (condition_1) { statement_1; } else if (condition_2) {
  statement_2; } else if (condition_n) { statement_n; } else {
  statement_last; }t</code>
</article>
      
      
      
      
      </section>
      <section class="main-section" id="while_statement"><header>While Statement</header></section>
      <section class="main-section" id="function_declaration"><header>Function Declaration</header></section>
      <section class="main-section" id="reference"><header>Reference</header></section>
       </main>
</body>
      </html>
