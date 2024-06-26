# HBV202G Assignment8
This project develops a comprehensive library management system designed to facilitate the efficient handling of library resources and user interactions. The system uses the Singleton design pattern for the librarySystem class to ensure that there is only one instance of the system throughout the application. This design choice is crucial for maintaining a coherent and consistent state across the entire library system with no duplicate entities or conflicting states. The system caters to different user roles, namely students and faculty members, and supports operations such as book lending and returns.

# Implementation
Both the implementation and the tests are in the Java package `is.hi.hbv202g.assignment8`, 
but in the usual separate Maven `src` directories:

- `src/main/java/is/hi/hbv202g/assignment8`:
  - `Author.java`: Implementation of an author.
  - `Book.java`: Implementation of a book that has a name and a list of authors.
  - `EmptyAuthorListException.java`: An exception that is thrown if a list of authors is empty.
  - `FacultyMember.java`: Implementation of a faculty member that is a user.
  - `Lending.java`: Implementation of lending a book. 
  - `LibrarySystem.java`: Implementation of a single library system that keeps track of all books, all users, and all lendings.
  - `Main.java`: A class with a simple text UI.
  - `Student.java`: Implementation of a student that is a user.
  - `User.java`: Implementation of a user.
  - `UserOrBookDoesNotExistException.java`: An exception that is thrown if a book or user does not exist.

- `src/test/java/is/hi/hbv202g/assignment8`:
  - `AllTests.java`: A class that runs all the test classes.
  - `BookTest.java`: A skeleton for a class containing JUnit4 test cases for the `Book` class.
  - `LendingTest.java`: A skeleton for a class containing JUnit4 test cases for the `Lending` class.
  - `LibrarySystemTest.java`: A skeleton for a class containing JUnit4 test cases for the `LibrarySystem` class.
  - `StudentTest.java`: A skeleton for a class containing JUnit4 test cases for the `Student` class.

# Run the Program

## Maven
- `mvn compile` compiles all implementation classes.
- `mvn exec:java` executes the main method of the implementation. Ensure the main class is specified in your `pom.xml` or this command.
- `mvn test` runs all test cases.

## Jar
Open your terminal and type `bash` to switch to the Bash shell if it's not already the default.

- `./package.sh` creates a fat jar file.
- `./run.sh` executes the main method of the implementation.

# Generating the Project Site
- `mvn site` generates the project's website documentation and makes it viewable.

# Design
UML: [UML](src/site/markdown/uml.md)

# License
MIT license: [License](LICENSE)

# Design
 
 UML: [UML](src/site/markdown/uml.md)

## Design Pattern
This project implements the Singleton design pattern, ensuring that only one instance of the Library System is created. As demonstrated in the `LibrarySystem.java class`, a `private static LibrarySystem instance` is defined. Whenever the system needs to access items from the Library System, it utilizes `LibrarySystem.getInstance()`.