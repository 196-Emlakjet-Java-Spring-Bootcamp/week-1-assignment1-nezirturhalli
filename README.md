
#  Java 11 New Features
#### Java is one of the most popular including in programming languages in the world. Java has enhanced since its introduction in 1995. It takes a slightly longer work to keep up with the latest versions frequent social media release cycle in recent years.
We'll begin by discussing the changes in Java 11.
Let's get started.



![image](https://user-images.githubusercontent.com/32534565/170483483-19bede1f-8c33-4239-b01b-61945b01e757.png)

## Overview of New Features
## 1- HTTP API
 - The HTTP API is a Java package that allows you to make HTTP queries.
### purpose
HttpURLConnection, which was introduced with Java 1.1 in 1997 and is difficult to use and maintain, has been replaced.
### features
- HTTP/1.1 and HTTP/2 protocols are supported.
- Common HTTP methods such as GET, POST, PUT, and DELETE are supported.
- Can communicate in both synchronous and asynchronous modes
- ways to make advantage of
- HttpClient is created, initialized, and configured.
- Initiate and create HttpRequest
- HttpRequest is passed to HttpClient, which executes the request and returns HttpResponse.
- Handle HttpResponse according to your needs.
## 2- Launching Single-File Java Program
- Java 11 allows you to run a single Java program from a single command.
### details
- Allows for novice-friendly Java development and rapid prototyping.
- It must be a single-file application (with one or more classes).
- External dependencies aren't an option.
### how to use
- Let's say our file is called MyProgram.java, and all we have to do to run it is type java MyProgram.java.
## 3- New Library Methods for Strings, Collections and Files
- For the sake of convenience, Java 11 provided some handy methods for the aforementioned libraries.

### strings api
- Repeat a string: Repeat a string n times with String.repeat(Integer). Example: " ".repeat(10)
- Check empty/whitespace: Check if string is empty or whitespace only. String.isBlank(). It’ll throw NullPointerExceptionif the string is blank.
- Remove whitespaces: Remove leading String.stripLeading(), trailing String.stripTrailing() or both whitespaces String.strip()
- Process multiline string: Convert multiline /n string to stream of lines with String.lines()
### collections api
Convert collection to an array: This process made easier with Java 11. For example, converting a list of students to string array would be performed with students.toArray(String[]::new)
### Optional and predicate.
Negating a predicate : We can filter out the elements not having a certain condition with Predicate.not(myCustomPredicate).
### files api
Easier file read/write: Thanks to Files.readString(path) and Files.writeString(path, charSequence, options) we can achieve this operations.
## 4- Performance and Security Improvements
### performance Improvements
- G1 Garbage Collector Improvements: G1 was introduced in Java 7 and became the default GC in Java 9. With Java 11, G1 is improved for high performance. Java 11 improves pause times (client waiting for application response caused by GC) by up to 60% (source).
- ZGC: An experimental but scalable and low-latency GC. It guarantees maximum pause time of 10 ms. ZGC is great for applications memory consuming applications that handle a lot of data.
- Epsilon: An experimental but low-overhead GC. It’s a good fit for short living applications (executing a single command then closing).
security Improvements
- The recent Transport Layer Security (TLS) improved HTTPS performance and security. Java 11 supports the TLS 1.3 protocol.
## 5- Other Enhancements
- Using var in lambdas: We've met var with Java 10, now we can use it in lambdas. Advantage of this feature is now we can annotate lambda variables (eg. @NotNull)
- Adoption of Unicode 10: Java 11 uses Unicode 10, an upgrade from Java 10 with Unicode 8. That includes 16,018 new characters and 10 new scripts.
- Nested access control: Inner class can access all private variables and methods of Outer class (eg. Outer.name).
- Java Flight Recorder: JFR is a profiling and diagnostics (resource usage etc.) tool. We can also use Java Mission Control to visualize data provided by JFR.
## 6- Removed and Deprecated Features
### removed features
- Java 11 is backwards compatible with Java 8. So you can swiftly change from Java 8 to 11. If you use some of the packages below, all you need to do is add the replacement dependency to your project.
### deprecated features
- Nashorn JavaScript Engine: Since it’s hard to maintain compatibility with rapid changing of ECMAScript, it’s now deprecated.



