Doctest module python 

https://realpython.com/python-doctest/

You won’t have to install any third-party libraries or learn complex APIs to follow this tutorial. You only need to know the basics of Python programming and how to use the Python REPL or interactive shell.

The doctest framework searches for test cases in your documentation and the docstrings of packages, modules, functions, classes, and methods. It doesn’t search for test cases in any objects that you import.


The doctest framework is well suited for the quick automation of acceptance tests at the integration and system testing levels. Acceptance tests are those tests that you run to determine if the specifications of a given project are met, while integration tests are intended to guarantee that different components of a project work correctly as a group.

At the class, method, and function level, doctest tests are a powerful tool for testing your code as you write it. You can gradually add test cases to your docstrings while you’re writing the code itself. This practice will allow you to generate more reliable and robust code, especially if you stick to the test-driven development principles.

In practice, doctest is very strict when matching expected output with actual results. For example, using integers instead of floating-point numbers will break the test cases for your add() function
Other tiny details like using spaces or tabs, wrapping returned strings in double quotes, or inserting blank lines can also cause tests to break.

To summarize, you must guarantee a perfect match between the actual test output and the expected output. So, make sure that the line immediately after every test case perfectly matches what you need your code to return or print.

The doctest module follows mostly the same rules when catching return values and exceptions. It searches for text that looks like a Python exception report or traceback and checks it against any exception that your code raises.

When dealing with exception tracebacks, doctest completely ignores the traceback body because it can change unexpectedly. In practice, doctest is only concerned about the first line, which reads Traceback (most recent call last):, and the last line. As you already know, the first line is common to all exception tracebacks, while the last line shows information about the raised exception.

When you have a failing test, doctest displays the failing test and the failure’s cause. You’ll have a line at the end of the test report that summarizes the successful and failing tests.

The differences between the expected and the actual outputs can be pretty subtle, such as having no quotes, using double quotes instead of single quotes, or even accidentally inserting leading or trailing whitespaces.
