# Chapter 0--What do you need to know before starting to learn java reverse engineering?

## the term:

### 1. Qualified name:

Separate package names with ``.``. Functions such as `Class.forName(name)` require qualified names as arguments

Example:

- `java.lang.String`
- `com.example.MyClass.InnerClass`

Note: Only write the name of the last class, which is an unqualified name. For example

```java
import java.net.URL
URL a = new URL("www.baidu.com")//The URL here is an unqualified name, so it needs to be imported
java.net.URL b = new java.net.URL("www.baidu.com")//Same as above, but no need to import
```

<br/>
### 2. Internal name:

Separate package names with `/`. The `$` is followed by the inner class name. The internal name is the name of the class inside the `.class` class file

For example:

- `com/example/MyClass$InnerClass`

<br/>
### 3. Primitives:

Use a single character to represent primitives (primitives are types that cannot be subdivided)

| Primitives | Description in JVM |
| --------- | ----------- |
| `long` | `J` |
| `int` | `I` |
| `short` | `S` |
| `byte` | `B` |
| `boolean` | `Z` |
| `float` | `F` |
| `double` | `D` |
| `void` | `V` |

<br/>
### 4. Descriptor (Descriptor):

Descriptors are used to describe field and method types. Almost the same as the JVM internal type, but the class name is wrapped with `L` and `;`.

For example:

- `Ljava/lang/String;`
- `I` * (primitive same as above)*

Example method constructor format:

- `double method(int i, String s)` = `(ILjava/lang/String;)D`
- `void method()` = `()V`

Each level of array is marked with `[` prefix:

- `int[]` = `[I`

- `String[][]` = `[[Ljava/lang/String;`

**Wonderful thing: ** `double` and `long` type variables occupy two slots (whether on the operation stack or on the local variable table)

<br/>
### 5. Method (Method): a function member in a class (Class)

<br/>
### 6. Field (Field): variable members in the class (Class)

<br/>
### 7. Static debugging (static-analysis): refers to the analysis of Java bytecode

<br/>
### 8. Dynamic debugging (dynamic-analysis): refers to using the debugger to track the running JVM for analysis
