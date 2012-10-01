Embedded Unit
=============

Clone of [Embedded Unit](https://sourceforge.net/projects/embunit/) project.

Embedded Unit is unit testing framework for Embedded C System. It's design was
copied from JUnit and CUnit and more, and then adapted somewhat for Embedded C
System. Embedded Unit does not require std C libs. All objects are allocated
to const area.

Development environment and Execution environment
-------------------------------------------------

Required execution environment

	- The ROM more than 2KB
	- The Stack more than 128b

Required development environment

	- C Compiler

Development of Embedded Unit is performed in the following environment

	- Microsoft Windows XP Professional
	- VC++.NET or cygwin 1.3.22 + gcc 3.2
	- Microsoft Windows 98
	- VC++6.0
	- Apple Computer MacOS X 10.1.5
	- Project Builder 1.1.1 (gcc 2.95.2)

Compile
-------

Embedded Unit is using stdio print function for the output of a test
result message. Implement the following function, if you do not want
to use stdio print function.

	void stdimpl_print(const char *string)
	// * this function does not output a new-line in the end of a string.

And then add compile-option `'-DNO_STDIO_PRINTF'`, or release the following
comments of a `embUnit/config.h`.

	/*#define NO_STDIO_PRINTF*/

License
-------

Licensed under original project MIT/X Consortium License.