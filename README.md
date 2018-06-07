# Java Technical Interview Questions
## Java
### What is the JVM?
* This stands for Java Virtual Machine and it enables a computer to run Java programs as well as programs written in other 
languages and compiled to java bytecode. It is detailed by a specification that formally describes what is required of a
JVM implementation

### Define code compilation?
*Compilation is the transforming of high-level source code that is written by a developer in a high-level programming
language into a low level object code (binary code) in machine language, which can be understood by the processor

### What is a constuctor?
*This is a block of code similar to a method that's called when an instance of an object is created. Unlike methods
constructors don't have return types and are not considered members of a class

### What is the naming convention of variables in java?
*a variable name should start with a lowercase letter e.g. firstName

### What is an annotation and give an example.
*An annotation is aform of syntatic metadata that can be added to Java source code. Classes, methods, variables, parameters
and packages may be annotated

### What is the difference between '==' and equals() when comparing Strings?
*'==' compares object references, .equals() compares the string values

### What are the 8 primitive types in Java?
*They are 1)int 2)byte 3)short 4)long 5)float 6)double 7)boolean 8)char

### What is the difference between primitives and wrapper classes and when can we use each?
*Primitives can only represent a very specific set of data and cannot have methods called on them. Wrapper classes can turn primitives into obejcts as they can have methods called upon them

### Define Encapsulation and outline its benefits.
*Encapsulation is the hiding of data members and members function its benefits are 1)It promotes maintenance 2)It increases usability 3)Code changes can be made independently

### Do objects get passed by reference or value in Java? Elaborate on that.
*Java manipulates objects by reference and all object variables are references. However Java passes methods by value

### Explain the four OOP principles.
*Abstraction - this means using simple things like objects, classes and variables to represent more complex underlying code and data
*Encapsulation - this is the practice of keeping fields withn a class private, then providing access to them via public methods
*Inheritance - This lets programmers create new classes that share some of the attributes of existing classes building on previous work without reinventing the wheel
*Polymorphism - Polymorphism lets programmers use the same word to mean different things in different contexts

### What is the difference between Abstract classes and Interfaces?
*1)Methods of a Java interface are implicitly abstract and cannot have implementations. A java abstract class can have instance methods that implements a default behavior. 
*2)Variables declared in a Java interface is by default final. An abstract class may contain non-final variables

### Is it possible to implement multiple inheritance in Java?
*This is ok because the interfaces are only declaring the methods and the actual implementation will be done by concrete classes implementing the interfaces. So there is no possibility of any kind of ambiguity in multiple inheritance in java interfaces

### What is serialization? How do you implement it?
*Serialization is a mechanism of converting the state of an object into a byte stream. Deserialization is the reverse process where the byte stream is used to recreate the actual Java object in memory. The byte stream created is platform independent. To make a Java object serializable you implement the java.io.Serializable interface. This is only a marker interface which tells the Java platform that the object is serializable.

### What are anonymous classes?
*It is an inner class without a name and for which only a single object is created. An anonymous inner class can be useful when making an instance of an object with certain "extras" such as overloading methods of a class or interface, without having to actually subclass a class

### What does it means to say that a String is immutable?
*String objects are immutable in Java because they provide no methods that modify the state of an existing String object. They only provide methods that create new String objects based on the content of existing ones

### What is the difference between method overloading and method overriding?
*They are both examples of Polymorphism the difference however is method overloading is when different meanings are implied by the code itself and method overriding is when different meanings are implied by the values of the supplied variables.

### What are the access modifiers you know? What does each one do?
*Access modifiers/access specifiers are keywords in object-oriented languages that set the accessibility of classes, methods and other members. They are
*1)Default: Accessible to the classes in the same package only
*2)Public: Can be accessed from anywhere
*3)Private: Accessible only inside the same class
*4)Protected: Accessible only to the classes in the same package and to the subclasses

### Do objects get passed by reference or value in Java? Elaborate on that.
*Java does manipulate objects by reference and all object variables are references

* What the difference between local, instance and class variables?
* What is Dependency Injection?
* What does the static word mean in Java? Can a static method be overridden in Java?
* When is a static block run?
* What is reflection?
* How does the try{} catch{} finally{}
* What is garbage collection? How does it work?
* What is memory leak and how does Java handle it?
* What does the keyword synchronized mean?
* Explain Generics in Java


## Web Development
* What is the difference between a GET and POST request?
* What is a URI?
* Differenciate between a client and host.
* What is the difference between HTTP and HTTPS?
* Point out these components(query, host, port, protocol, path ) in the following URL https://127.0.0.1:4200/login/a=bx?c
* What is an Internet Protocol?
## Android
* What are the four main components of an Android Application?
* What is the purpose of a package name?
* What is the purpose of Android Virtual Device?
