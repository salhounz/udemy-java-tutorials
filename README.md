## Udemy Java Course Project

- **Project Description**

		An ongoing unit-by-unit breakdown of the Udemy Java Tutorial for Complete Beginners.
		The project begins in the Core Programming Section of the tutorial, and begins with UnitOne
		with examples such as Hello World and Primitives. However, later units such as UnitSix provide
		examples and context to more complex concepts such as Polymorphism and Upcasting/Downcasting.


## Run examples from the command line

Install a Java Development Kit (JDK), which includes both the `javac` compiler
and the `java` launcher. Make sure its `bin` directory is on your `PATH`, then
check both commands:

```sh
java -version
javac -version
```

Open a terminal in this repository's root directory (the folder containing
this README and `tutorials`). These commands work in PowerShell, Command
Prompt, and common macOS/Linux shells. No IDE, Maven, or Gradle is required.

### Compile and run Hello World

```sh
javac -d out tutorials/UnitOne/HelloWorld.java
java -cp out UnitOne.HelloWorld
```

Expected output: `Hello World`.

- `javac` compiles the source into bytecode. `-d out` creates the output
  directory and places the class at `out/UnitOne/HelloWorld.class`.
- `java -cp out` uses that output directory as the classpath. The launch name
  is `UnitOne.HelloWorld` because the file declares `package UnitOne;`.
  Use a dot between package and class; do not append `.java` or `.class`.
- Rerun the compile command whenever you change the source, then launch again.

### Run another lesson

For a standalone example, substitute its actual source path and class name:

```sh
javac -d out tutorials/UnitTwo/GettingUserInput.java
java -cp out UnitTwo.GettingUserInput
```

This lesson waits for keyboard input; type your response and press Enter.

Some lessons depend on other source files. Set the source path so the compiler
can find those classes automatically, for example:

```sh
javac -d out -sourcepath tutorials tutorials/UnitEight/AbstractClasses.java
java -cp out UnitEight.AbstractClasses
```

Run classes that define `public static void main(String[] args)`. Supporting
classes such as `UnitEight.Machine` are not standalone programs. Compile lessons
individually: some examples declare helper classes with the same name in the
same package, so compiling every source together can produce duplicate-class
errors. For lessons with conflicting helpers, use a separate output directory
in both commands instead of sharing `out`.

File-reading lessons resolve relative filenames from the terminal's current
directory, not from the source file's folder. Inspect their paths before running;
some intentionally demonstrate exceptions, and `ScannerFileReading` currently
contains a machine-specific absolute path that must be changed for your computer.
If `java` or `javac` is not recognized, check your JDK installation and `PATH`.
If Java cannot find the main class, check that compilation succeeded and that
the classpath and package-qualified class name match the commands above.

## Core Java Programming Overview

- **Unit One**
	- Section 1-5 *includes challenges such as HelloWorld, and primitive types*
- **Unit Two**
	- Section 6-10 *includes Arrays, If Loops, Switch Statements, and user input*
- **Unit Three**
	- Section 11-15 *includes Classes, Objects, String Arrays, and Getters/Setters*
- **Unit Four**
	- Section 16-20 *includes Static and Final variables, StringBuilder, and Constructors*
- **Unit Five**
	- Section 21-25 *includes Public, Private, Protected, Interfaces, and Inheritance*
- **Unit Six**
	- Section 26-30 *includes Polymorphism, Generics, Upcasting/Downcasting, Encapsulation, and Casting*
- **Unit Seven**
	- Section 31-35 *includes Wildcards, Anonymous Classes, and Handling Multiple Exceptions*
- **Unit Eight**
	- Section 36-40 *includes Abstract to Equals method section 45*
- **Unit Nine**
	- Section 41-45 *includes inner class to seralizing arrays*
- **Unit Ten**
	- Section 46-52 *includes 51 and 52 from courses*








