# CCRMP-Campus-Course-and-Records-Manager

## 1. Project Overview & Execution

This is a console-based Java SE application for managing students, courses, enrollment, and grades within a campus environment. It demonstrates core OOP principles (Inheritance, Polymorphism) and advanced Java features (Singleton, Builder, NIO.2, Streams, Lambdas).

### How to Run

1.  *Prerequisites:* Ensure *JDK 17 or higher* is installed.
2.  *Clone the Repository:*
    bash
    git clone [https://github.com/sidhigautam6-code/CCRMP-Campus-course-and-Records-Manager.git](https://github.com/sidhigautam6-code/CCRMP-Campus-course-and-Records-Manager.git)
    cd CCRMP-Campus-course-and-Records-Manager
    
3.  *Compile:* (From the root directory)
    bash
    javac -d bin src/edu/ccrm/cli/*.java src/edu/ccrm/config/*.java src/edu/ccrm/domain/*.java src/edu/ccrm/domain/enums/*.java src/edu/ccrm/exception/*.java src/edu/ccrm/service/*.java
    
4.  *Run:* **(Must use -ea to enable Assertions)**
    bash
    java -cp bin -ea edu.ccrm.cli.CcrMain
    

## 2. Technical Background

### Evolution of Java (Short Bullets)

* *1995: JDK 1.0 (Oak):* Initial release, defining the core language and VM.
* *1998: Java 2 (J2SE 1.2):* Introduced Collections Framework, Swing, and JIT Compiler.
* *2004: J2SE 5.0 (Tiger):* Major release introducing *Generics, Enums, Autoboxing*, and Annotations.
* *2014: Java SE 8:* Introduced *Lambda Expressions, **Stream API, and the **Date/Time API (java.time)*, essential for modern Java.
* *2017/2018: Java SE 9+:* Shift to a faster release cadence, introducing the *Module System (Jigsaw)* and further updates to the language.

### JDK vs JRE vs JVM

| Term | Full Name | Purpose |
| :--- | :--- | :--- |
| *JDK* | Java Development Kit | *Compiler + JRE.* Necessary for developing and compiling Java applications (javac). |
| *JRE* | Java Runtime Environment | *Libraries + JVM.* Necessary for running compiled Java applications. |
| *JVM* | Java Virtual Machine | *Specification/Runtime.* The abstract machine that executes Java bytecode, providing the platform independence ("Write once, run anywhere"). |

### Java ME vs SE vs EE Comparison

| Edition | Full Name | Focus | Example Use |
| :--- | :--- | :--- | :--- |
| *Java SE* | Standard Edition | Core APIs, desktop, server-side console apps. | This CCRM project, simple utilities. |
| *Java ME* | Micro Edition | Embedded systems, mobile devices (legacy). | Old mobile phone games, small industrial controls. |
| *Java EE* | Enterprise Edition | Large-scale, multi-tiered, distributed web systems. | Banking platforms, large e-commerce sites (now Jakarta EE). |

## 3. Syllabus Topic Mapping Table

| Syllabus Topic | File/Class/Method | Requirement Demonstration |
| :--- | :--- | :--- |
| *Inheritance* | Student.java | extends Person |
| *Abstraction/Polymorphism* | Person.java | abstract class and abstract String getRole() |
| *Singleton Pattern* | AppConfig.java | private constructor and getInstance() method |
| *Builder Pattern* | Course.java | public static class Builder nested class |
| *Custom Exception* | DataNotFoundException.java | extends RuntimeException |
| *Enums* | Grade.java | Enum with fields and a fromMarks() utility method |
| *NIO.2 (File I/O)* | BackupService.java | Files.walk(), Files.copy(), Files.createDirectories() |
| *Streams & Lambdas* | StudentService.java | students.stream().filter(s -> ...) |
| *Recursion* | BackupService.java | calculateDirectorySizeRecursively() (via Files.walk) |
| *Date/Time API* | CcrMain.java, Person.java | Uses LocalDateTime.now() and DateTimeFormatter |
| *Assertions* | CcrMain.java | assert (assertionsEnabled = true) check and runtime warning |
