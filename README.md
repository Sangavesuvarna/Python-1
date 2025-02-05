# Python

* Python is an interpreted high-level general-purpose programming language.
* Its design philosophy emphasizes code readability with its use of significant indentation. 
* Python is dynamically-typed and garbage-collected.
* It supports multiple programming paradigms, including structured (particularly, procedural), object-oriented and functional programming.
* It is often described as a "batteries included" language due to its comprehensive standard library.

## Python statements and control flow

Python's statements include (among others):

* The assignment statement, using a single equals sign `=`.
* The `if` statement, which conditionally executes a block of code, along with else and elif (a contraction of else-if).
* The `for` statement, which iterates over an iterable object, capturing each element to a local variable for use by the attached block.
* The `while` statement, which executes a block of code as long as its condition is true.
* The `try` statement, which allows exceptions raised in its attached code block to be caught and handled by except clauses; it also ensures that clean-up code in a finally block will always be run regardless of how the block exits.
* The `raise` statement, used to raise a specified exception or re-raise a caught exception.
* The `class` statement, which executes a block of code and attaches its local namespace to a class, for use in object-oriented programming.
* The `def` statement, which defines a function or method.
* The `with` statement, which encloses a code block within a context manager (for example, acquiring a lock before the block of code is run and releasing the lock afterwards, or opening a file and then closing it), allowing resource-acquisition-is-initialization (RAII)-like behavior and replaces a common try/finally idiom.
* The `break` statement, exits from a loop.
* The `continue` statement, skips this iteration and continues with the next item.
* The `del` statement, removes a variable, which means the reference from the name to the value is deleted and trying to use that variable will cause an error. A deleted variable can be reassigned.
* The `pass` statement, which serves as a NOP. It is syntactically needed to create an empty code block.
* The `assert` statement, used during debugging to check for conditions that should apply.
* The `yield` statement, which returns a value from a generator function and yield is also an operator. This form is used to implement coroutines.
* The `return` statement, used to return a value from a function.
* The `import` statement, which is used to import modules whose functions or variables can be used in the current program.


## Expressions

Some Python expressions are similar to those found in languages such as C and Java, while some are not:

* Addition, subtraction, and multiplication are the same, but the behavior of division differs. There are two types of divisions in Python. They are floor division (or integer division) // and floating-point/division. Python also uses the ** operator for exponentiation.
* From Python 3.5, the new @ infix operator was introduced. It is intended to be used by libraries such as NumPy for matrix multiplication.
* From Python 3.8, the syntax :=, called the 'walrus operator' was introduced. It assigns values to variables as part of a larger expression.
* In Python, == compares by value, versus Java, which compares numerics by value and objects by reference.(Value comparisons in Java on objects can be performed with the equals() method.) Python's is operator may be used to compare object identities (comparison by reference). In Python, comparisons may be chained, for example a <= b <= c.
* Python uses the words and, or, not for its boolean operators rather than the symbolic &&, ||, ! used in Java and C.
* Python has a type of expression termed a list comprehension as well as a more general expression termed a generator expression.
* Anonymous functions are implemented using lambda expressions; however, these are limited in that the body can only be one expression.
* Conditional expressions in Python are written as x if c else y (different in order of operands from the c ? x : y operator common to many other languages).
* Python makes a distinction between lists and tuples. Lists are written as [1, 2, 3], are mutable, and cannot be used as the keys of dictionaries (dictionary keys must be immutable in Python). Tuples are written as (1, 2, 3), are immutable and thus can be used as the keys of dictionaries, provided all elements of the tuple are immutable. The + operator can be used to concatenate two tuples, which does not directly modify their contents, but rather produces a new tuple containing the elements of both provided tuples. Thus, given the variable t initially equal to (1, 2, 3), executing t = t + (4, 5) first evaluates t + (4, 5), which yields (1, 2, 3, 4, 5), which is then assigned back to t, thereby effectively "modifying the contents" of t, while conforming to the immutable nature of tuple objects. Parentheses are optional for tuples in unambiguous contexts.
* Python features sequence unpacking wherein multiple expressions, each evaluating to anything that can be assigned to (a variable, a writable property, etc.), are associated in an identical manner to that forming tuple literals and, as a whole, are put on the left-hand side of the equal sign in an assignment statement. The statement expects an iterable object on the right-hand side of the equal sign that produces the same number of values as the provided writable expressions when iterated through and will iterate through it, assigning each of the produced values to the corresponding expression on the left.
* Python has a "string format" operator %. This functions analogously to printf format strings in C, e.g. "spam=%s eggs=%d" % ("blah", 2) evaluates to "spam=blah eggs=2". In Python 3 and 2.6+, this was supplemented by the format() method of the str class, e.g. "spam={0} eggs={1}".format("blah", 2). Python 3.6 added "f-strings": blah = "blah"; eggs = 2; f'spam={blah} eggs={eggs}'.
* Strings in Python can be concatenated, by "adding" them (same operator as for adding integers and floats). E.g. "spam" + "eggs" returns "spameggs". Even if your strings contain numbers, they are still added as strings rather than integers. E.g. "2" + "2" returns "22".
* Python has various kinds of string literals:
* Strings delimited by single or double quote marks. Unlike in Unix shells, Perl and Perl-influenced languages, single quote marks and double quote marks function identically. Both kinds of string use the backslash (\) as an escape character. String interpolation became available in Python 3.6 as "formatted string literals".
* Triple-quoted strings, which begin and end with a series of three single or double quote marks. They may span multiple lines and function like here documents in shells, Perl and Ruby.
* Raw string varieties, denoted by prefixing the string literal with an r. Escape sequences are not interpreted; hence raw strings are useful where literal backslashes are common, such as regular expressions and Windows-style paths. Compare "@-quoting" in C#.
* Python has array index and array slicing expressions on lists, denoted as a[key], a[start:stop] or a[start:stop:step]. Indexes are zero-based, and negative indexes are relative to the end. Slices take elements from the start index up to, but not including, the stop index. The third slice parameter, called step or stride, allows elements to be skipped and reversed. Slice indexes may be omitted, for example a[:] returns a copy of the entire list. Each element of a slice is a shallow copy.
* In Python, a distinction between expressions and statements is rigidly enforced, in contrast to languages such as Common Lisp, Scheme, or Ruby. This leads to duplicating some functionality. For example:

* List comprehensions vs. for-loops
* Conditional expressions vs. if blocks
* The eval() vs. exec() built-in functions (in Python 2, exec is a statement); the former is for expressions, the latter is for statements.

Statements cannot be a part of an expression, so list and other comprehensions or lambda expressions, all being expressions, cannot contain statements. A particular case of this is that an assignment statement such as a = 1 cannot form part of the conditional expression of a conditional statement. This has the advantage of avoiding a classic C error of mistaking an assignment operator = for an equality operator == in conditions: if (c = 1) { ... } is syntactically valid (but probably unintended) C code but if c = 1: ... causes a syntax error in Python.

## Methods

* Methods on objects are functions attached to the object's class; 
* the syntax instance.method(argument) is, for normal methods and functions, syntactic sugar for Class.method(instance, argument). 
* Python methods have an explicit self parameter to access instance data, in contrast to the implicit self (or this) in some other object-oriented programming languages (e.g., C++, Java, Objective-C, or Ruby).
* Apart from this Python also provides methods, sometimes called dunder methods due to their names beginning and ending with double-underscores, to extend the functionality of custom class to support native functions such as print, length, comparison, support for arithmetic operations, type conversion, and many more.

## Typing

![image](https://user-images.githubusercontent.com/11299574/131167952-10c95d10-762c-4a73-9a55-ba9ca1289708.png)

The standard type hierarchy in Python 3

* Python uses duck typing and has typed objects but untyped variable names. 
* Type constraints are not checked at compile time; rather, operations on an object may fail, signifying that the given object is not of a suitable type. 
* Despite being dynamically-typed, Python is strongly-typed, forbidding operations that are not well-defined (for example, adding a number to a string) rather than silently attempting to make sense of them.

* Python allows programmers to define their own types using classes, which are most often used for object-oriented programming. 
New instances of classes are constructed by calling the class (for example, SpamClass() or EggsClass()), and the classes are instances of the metaclass type (itself an instance of itself), allowing metaprogramming and reflection.

## Code Examples

Hello world program:
```py
print('Hello, world!')
```

Program to calculate the factorial of a positive integer:
```py
n = int(input('Type a number, and its factorial will be printed: '))

if n < 0:
    raise ValueError('You must enter a non negative integer')

factorial = 1
for i in range(2, n + 1):
    factorial *= i

print(factorial)
```

## Development environments


* Most Python implementations (including CPython) include a read–eval–print loop (REPL), permitting them to function as a command line interpreter for which the user enters statements sequentially and receives results immediately.

* Other shells, including IDLE and IPython, add further abilities such as improved auto-completion, session state retention and syntax highlighting.

* As well as standard desktop integrated development environments, there are Web browser-based IDEs; SageMath (intended for developing science and math-related Python programs); PythonAnywhere, a browser-based IDE and hosting environment; and Canopy IDE, a commercial Python IDE emphasizing scientific computing.


## Languages influenced by Python

Python's design and philosophy have influenced many other programming language
* Boo uses indentation, a similar syntax, and a similar object model.
* Cobra uses indentation and a similar syntax, and its Acknowledgements document lists Python first among languages that influenced it.
* CoffeeScript, a programming language that cross-compiles to JavaScript, has Python-inspired syntax.
* ECMAScript/JavaScript borrowed iterators and generators from Python.
* GDScript, a scripting language very similar to Python, built-in to the Godot game engine.
* Go is designed for the "speed of working in a dynamic language like Python" and shares the same syntax for slicing arrays.
* Groovy was motivated by the desire to bring the Python design philosophy to Java.
* Julia was designed to be "as usable for general programming as Python".
* Nim uses indentation and similar syntax.
* Ruby's creator, Yukihiro Matsumoto, has said: "I wanted a scripting language that was more powerful than Perl, and more object-oriented than Python. That's why I decided to design my own language."
* Swift, a programming language developed by Apple, has some Python-inspired syntax.

Python's development practices have also been emulated by other languages. For example, the practice of requiring a document describing the rationale for, and issues surrounding, a change to the language (in Python, a PEP) is also used in Tcl, Erlang, and Swift.

## Start a Python virtual environment 

```
> python -m venv env
> .\env\Scripts\activate
> (env) C:\drive\cd .\app\ 
```
