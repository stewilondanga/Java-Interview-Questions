# Java Technical Interview Questions
## Java
### What is the JVM?
* This stands for Java Virtual Machine and it enables a computer to run Java programs as well as programs written in other 
languages and compiled to java bytecode. It is detailed by a specification that formally describes what is required of a
JVM implementation

### Define code compilation?
* Compilation is the transforming of high-level source code that is written by a developer in a high-level programming
language into a low level object code (binary code) in machine language, which can be understood by the processor

### What is a constuctor?
* This is a block of code similar to a method that's called when an instance of an object is created. Unlike methods
constructors don't have return types and are not considered members of a class

### What is the naming convention of variables in java?
* A variable name should start with a lowercase letter e.g. firstName

### What is an annotation and give an example.
* An annotation is aform of syntatic metadata that can be added to Java source code. Classes, methods, variables, parameters
and packages may be annotated

### What is the difference between '==' and equals() when comparing Strings?
* '==' compares object references, .equals() compares the string values

### What are the 8 primitive types in Java?
* They are 1)int 2)byte 3)short 4)long 5)float 6)double 7)boolean 8)char

### What is the difference between primitives and wrapper classes and when can we use each?
* Primitives can only represent a very specific set of data and cannot have methods called on them. Wrapper classes can turn primitives into obejcts as they can have methods called upon them

### Define Encapsulation and outline its benefits.
* Encapsulation is the hiding of data members and members function its benefits are 1)It promotes maintenance 2)It increases usability 3)Code changes can be made independently

### Do objects get passed by reference or value in Java? Elaborate on that.
* Java manipulates objects by reference and all object variables are references. However Java passes methods by value

### Explain the four OOP principles.
* Abstraction - this means using simple things like objects, classes and variables to represent more complex underlying code and data
* Encapsulation - this is the practice of keeping fields withn a class private, then providing access to them via public methods
* Inheritance - This lets programmers create new classes that share some of the attributes of existing classes building on previous work without reinventing the wheel
* Polymorphism - Polymorphism lets programmers use the same word to mean different things in different contexts

### What is the difference between Abstract classes and Interfaces?
* 1)Methods of a Java interface are implicitly abstract and cannot have implementations. A java abstract class can have instance methods that implements a default behavior. 
* 2)Variables declared in a Java interface is by default final. An abstract class may contain non-final variables

### Is it possible to implement multiple inheritance in Java?
* This is ok because the interfaces are only declaring the methods and the actual implementation will be done by concrete classes implementing the interfaces. So there is no possibility of any kind of ambiguity in multiple inheritance in java interfaces

### What is serialization? How do you implement it?
* Serialization is a mechanism of converting the state of an object into a byte stream. Deserialization is the reverse process where the byte stream is used to recreate the actual Java object in memory. The byte stream created is platform independent. To make a Java object serializable you implement the java.io.Serializable interface. This is only a marker interface which tells the Java platform that the object is serializable.

### What are anonymous classes?
* It is an inner class without a name and for which only a single object is created. An anonymous inner class can be useful when making an instance of an object with certain "extras" such as overloading methods of a class or interface, without having to actually subclass a class

### What does it means to say that a String is immutable?
* String objects are immutable in Java because they provide no methods that modify the state of an existing String object. They only provide methods that create new String objects based on the content of existing ones

### What is the difference between method overloading and method overriding?
* They are both examples of Polymorphism the difference however is method overloading is when different meanings are implied by the code itself and method overriding is when different meanings are implied by the values of the supplied variables.

### What are the access modifiers you know? What does each one do?
* Access modifiers/access specifiers are keywords in object-oriented languages that set the accessibility of classes, methods and other members. They are
* 1)Default: Accessible to the classes in the same package only
* 2)Public: Can be accessed from anywhere
* 3)Private: Accessible only inside the same class
* 4)Protected: Accessible only to the classes in the same package and to the subclasses

### Do objects get passed by reference or value in Java? Elaborate on that.
* Java does manipulate objects by reference and all object variables are references
* Take the badSwap() method for example:

    public void badSwap(int var1, int var2){
      int temp = var1;
      var1 = var2;
      var2 = temp;
    }
* When badSwap() returns, the variables passed as arguments will still hold their original values. The method will also fail if we change the arguments type from int to Object, since Java passes object references by value as well. Now here is where it gets tricky:

    public void tricky(Point argl, Point arg2) {
      argl.x = 100;
      argl.y = 100;
      Point temp = argl;
      argl = arg2;
      arg2 = temp;
    }
    public static void main(String [] args)
    {
      Point pnt1 = new Point(0,0);
      Point pnt2 = new Point(0,0);
      System.out.println("X: " + pnt1.x + " Y: " +pnt1.y);
      System.out.println("X: " + pnt2.x + " Y: " +pnt2.y);
      System.out.println(" ");
      tricky(pnt1,pnt2);
      System.out.println("X: " + pnt1.x + " Y:" + pnt1.y);
      System.out.println("X: " + pnt2.x + " Y: " +pnt2.y);
    }
* If we execute this main() method, we see the following output:
       
       X: 0 Y: 0
       X: 0 Y: 0
       X: 100 Y: 100
       X: 0 Y: 0
* The method successfully alters the value of pnt1, even though it is passed by value; however, a swap of pnt1 and pnt2 fails! This is the major source of confusion. In the main() method, pnt1 and pnt2 fails! This is the major source of confusion. In the main() method, pnt1 and pnt2 are nothing more than object references. When you pass pnt1 and pnt2 to the tricky() method, Java passes the references by value just like any other parameter. This means the references passed to the method are actually copies of the original references.
      
### What's the difference between local, instance and class variables?
* The difference between instance variable and class variable also known as non-static vs variable in java is that instance variables are per instance(object) basis. On the other hand, Class variables are declared using static keyword and they have exact same value for every instance.
* Classic variables maintain a single shared value for all instances of the class, even if no instance object of that class exists. You would use the static keyword to change an instance variable into a class variable. both instance and class variables are declared at the class level, not within methods.

### What is Dependency Injection?
* Dependency injection is a technique whereby one object(or static method) supplies the dependencies of another object. A dependency is an object that can be used(a service). An injection is the passing of a dependency to a dependent object (a client) that would use it.

### What does the static word mean in Java? Can a static method be overridden in Java?
* The static keyword in Java means that the variable or function is shared between all instances of that class as it belongs to the type, not the actua; objects themselves. So if you have a variable: private static int i = 0; and you increment it (i++) in one instance, the change will be reflected in all instances
* Overriding is a feature of object oriented programming languages like Java that is related to run-time polymorphism. A subclass (or derived class) provides a specific implementation of a method in superclass (or base class)

### When is a static block run?
* The static initializer will be executed when the class is loaded. This normally occurs when you access the class in the class loading context for the first time. Static block is executed when a loaded class is initialized or referenced first.

### What is reflection?
* Java reflection makes it possible to inspect classes, interfaces, fields and methods at runtime, without knowing the names of the classes, methods etc at compile time. It is also possible to instantiate new objectss, invoke methods and get/set field values using reflection.

### How does the try{} catch{} finally{}
* The finally block always executes when the try block exits. this ensures that the finally block is executed even if an unexpected exception occurs. but finally is useful for more than just exception handling -- it allows the programmer to avoid having cleanup code accidentally bypassing by a return, continue, or break. If the JVM exits while the try or catch code is being executed, then the finally block may not execute. Likewise, if the thread executing the try or catch code is interrupted or killed, the finally block may not execute even though the application as a whole continues.

### What is garbage collection? How does it work?
* As long as an object is being referenced, the JVM considers it alive. Once an object is no longer referenced and therefore is not reachable by the application code, the garbage collector removes it and reclaims the unused memory

### What is memory leak and how does Java handle it?
* Java's automatic memory management relies on GC which periodically looks for unused objects and removes them. We can say that a memory leak in Java is a situation where some objects are not used by application any more, but GC fails to recognize them as unused.

### What does the keyword synchronized mean?
* Synchronized means that in a multi threaded environment, an object having synchronized method(s)/block(s) does not let two threads to access the synchronized method(s)/block(s) of code at the same time. This means that one thread can't read while another thread updates it.

### Explain Generics in Java
* Generics are a facility of generic programming that were added to the Java programming language in 2004 within version J2SE5.O. They were designed to extend Java's type system to allow "a type or method to operate on objects of various types while providing compile_time type safety".


## Web Development

### What is the difference between a GET and POST request?
* Post requests supply additional data from the client (browser) to the server in the message body. In contrast, GET requests include all required data in the URL. The method specified determines how form data is submitted to the server.

### What is a URI?
* A Uniform Resource Identifier (URI) is a string of characters designed for unambigous identification of resources and extensibility ia the URI scheme. Such identification enables interaction with representations of the resource over a network, typically the World Wide Web.

### Differenciate between a client and host.
* A host is any end device in a network. In that network, the host can either be a server, a client or both. A client on the other hand is a computer that has software that enables it to send requests to the server for a particular service. e.g. a computer has a web browser that enables you to access email.

### What is the difference between HTTP and HTTPS?
* Instead of HyperText Transfer Protocol(HTTP), this website uses HyperText Transfer Protocol Secure(HTTPS). Using HTTPS, the computers agree on a "code" between them, and then they scramble the messages using that "code" so that no one in between can read them. This keeps your information safe from hackers.

### Point out these components(query, host, port, protocol, path ) in the following URL https://127.0.0.1:4200/login/a=bx?c
* Query - All the stuff that comes after the ? (question mark)
* Host - 127.0.0.1
* Port - 4200
* Protocol - login
* Path - a=bx
* A scheme - https

### What is an Internet Protocol?
* The Internet Protocol(IP)is the method or protocol by which data is sent from one computer to another on the internet. Each computer (known as a host) on the Internet has at least one IP address that uniquely identifies it from all other comouters on the Internet.

## Android

### What are the four main components of an Android Application?
* Activities
* Services
* Content providers
* Broadcast receivers

### What is the purpose of a package name?
* This package name is the application ID and uniquely identifies your app on the device and in Google Play Store 

### What is the purpose of Android Virtual Device?
* An Android emulator is an Android Virtual Device (AVD) that represents a specific Android device. It is used as a target platform to run and test your Android applications on your PC.
