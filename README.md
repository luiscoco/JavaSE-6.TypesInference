# JavaSE-6.TypesInference

Type inference is a feature in programming languages that allows the compiler to deduce the type of a variable without explicit declaration by the programmer. 

In Java, type inference is closely associated with the introduction of the var keyword in Java 10.

Let me give you a simple example:

```java
// Without type inference
String message = "Hello, World!";
System.out.println(message);

// With type inference (Java 10 and later)
var anotherMessage = "Hello, Inferred World!";
System.out.println(anotherMessage);
```

In the first example, we explicitly declare the type of the variable message as String. 

In the second example, we use the var keyword, and the compiler infers that anotherMessage is of type String based on the assigned value.

It's important to note that while var is useful for enhancing code conciseness, it doesn't mean Java has become a dynamically typed language. 

The type is still known at compile-time; it's just inferred by the compiler based on the assigned value.

Here's another example using a more complex type:

```java
// Without type inference
List<String> names = new ArrayList<>();
names.add("Alice");
names.add("Bob");
System.out.println(names);

// With type inference
var otherNames = new ArrayList<String>();
otherNames.add("Charlie");
otherNames.add("David");
System.out.println(otherNames);
```

In this example, the type of the names and otherNames variables is List<String>, but in the second case, we use var for type inference.

Keep in mind that while type inference can improve code readability and reduce verbosity, it's important to use it judiciously. 

It's usually best suited for cases where the type is obvious from the assigned value.
