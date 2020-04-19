## Writing Comments in Java: Everything You Need to Know
Commenting is an integral part of any programming language for it is a guide that helps in better understanding and functionality of a program. Good programmers tend to comment as they go while writing the code. Many times, when you write the code, you will need to go back and make the changes. Without Java comments, one can be lost. I specifically make sure that comments are made as I moved forward with the code. Not only does it help me keep track of the code as it gets complicated, it also makes the code more understandable for those who have no experience with coding.
Comments in Java are the statements in the Java code that are not executed when the program is run. Think of them as markers that guide the reader. They provide information about the code. Some programmers can also use it to hide certain portion of code for some time. In this article, I will discuss the types of Java comments and what are some best ways to use them. 
## Types of Comments in Java
In Java, the role of comments is to make it more human readable. It makes finding errors in the program easy. Here are different types of comments in Java:
### 1. Single-line Comments
As the name suggests, these comments end in single line. They begin with two forward slashes (//). They can also be used to make in-line comments.

Syntax:
```java
// this is a single-line comment in Java
```

Example:
```java
//my first comment
public class HelloWorld {
  public static void main(String[] args) {
   System.out.println("Hello World!");
  }
}
```
Output:
```
Hello World!
```
### 2. Multi-line Comments
When comment has to be longer than one line, multi-line comments come in. They can also be made by putting ‘//’ at the beginning of each line, but that becomes quite tedious when comments are longer.  Multi-line comments in Java are wrapped in ‘/*’ and ‘*/’.

Syntax:
```java
/* this is a multi-line
comment in Java
and it continues up to
here */	
```
Example:
```java
/* This is the beginning of a
multi-line comment
this is the end for Hello World Program */
public class HelloWorld {
  public static void main(String[] args) {
   System.out.println("Hello World!");
  }
}
```
Output:
```
Hello World!
```

### 3. Documentation Comments 
These types of comments are use when the code is written for a project or a software package. Documentation comments help generate a documentation page for reference, which is useful in getting details about methods, parameters and more. The JDK Javadoc tool makes the use of documentation comments. 
The doc comments are wrapped in ‘/**’ and ‘*/’.

Syntax:
```java
/**Documentation Comment begins here
*
*tags are used in order to specify a parameter
*or method or heading
*HTML tags can also be used
*such as <h1>
*
*comment ends here*/	
```

Javadoc is a tool that comes with JDK and is used for generating Java code documentation in HTML from java source code. 
Here is the table of tags that can be used in Java:

| TAG           | DESCRIPTION                                                                                                                                                           | SYNTAX                                               |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| @author       | This tag adds the author of a class.                                                                                                                                  | @author name-text                                    |
| {@code}       | This tag displays text in code font without interpreting the text as HTML markup or nested javadoc tags.                                                              | {@code text}                                         |
| {@docRoot}    | This tag represents the relative path to the generated document’s root directory from any generated page.                                                             | {@docRoot}                                           |
| @deprecated   | This tag adds a comment indicating that this API should no longer be used.                                                                                            | @deprecated deprecatedtext                           |
| @exception    | This tag adds a Throws subheading to the generated documentation, with the classname and description text.                                                            | @exception class-name description                    |
| {@inheritDoc} | This tag inherits a comment from the nearest inheritable class or implementable interface.                                                                            | Inherits a comment from the immediate surperclass.   |
| {@link}       | This tag inserts an in-line link with the visible text label that points to the documentation for the specified package, class, or member name of a referenced class. | {@link package.class#member label}                   |
| {@linkplain}  | This tag identical to {@link}, except the link’s label is displayed in plain text than code font.                                                                     | {@linkplain package.class#member label}              |
| @param        | This tag adds a parameter with the specified parameter-name followed by the specified description to the “Parameters” section.                                        | @param parameter-name description                    |
| @return       | This tag adds a “Returns” section with the description text.                                                                                                          | @return description                                  |
| @see          | This tag adds a “See Also” heading with a link or text entry that points to reference.                                                                                | @see reference                                       |
| @serial       | This tag is used in the doc comment for a default serializable field.                                                                                                 | @serial field-description | include | exclude        |
| @serialData   | This tag documents the data written by the writeObject( ) or writeExternal( ) methods.                                                                                | @serialData data-description                         |
| @serialField  | This tag documents an ObjectStreamField component.                                                                                                                    | @serialField field-name field-type field-description |
| @since        | This tag adds a “Since” heading with the specified since-text to the generated documentation.                                                                         | @since release                                       |
| @throws       | The @throws and @exception tags are synonyms.                                                                                                                         | @throws class-name description                       |
| {@value}      | When {@value} is used in the doc comment of a static field, it displays the value of that constant.                                                                   | {@value package.class#field}                         |
| @version      | This tag adds a “Version” subheading with the specified version-text to the generated docs when the -version option is used.                                          | @version version-text                                |

Example:
```java

//Java program to illustrate frequently used  
// Comment tags or Documentation comments
  
/** 
* <h1>Program to find average of three numbers!</h1> 
* The FindAvg program implements an application that 
* simply calculates average of three integers and Prints 
* the output on the screen. 
* 
* @author Nick McCullum 
* 
*/
public class FindAvg  
{ 
    /** 
    * This method is used to find average of three numbers. 
    * @param numX This is the first parameter 
    * @param numY  This is the second parameter 
    * @param numZ  This is the second parameter to 
    * @return int This returns average of numA, numB and numC. 
    */
    public int findAvg(int numX, int numY, int numZ)  
    { 
        return (numX + numY + numZ)/3; 
    } 
  
    /** 
    * This is the main method which makes use of findAvg method. 
    * @param args Unused. 
    * @return Nothing. 
    */
  
    public static void main(String args[])  
    { 
        FindAvg obj = new FindAvg(); 
        int avg = obj.findAvg(30, 60, 90); 
  
        System.out.println("Average of 30, 60 and 90 is : " + avg); 
    } 
}
```
Output:

```
Average of 30, 60 and 90 is : 60
```
  The documentation for the above given code can be generated using a ‘javadoc’ tool by running the following command:
```java

javadoc FindAvg.java
```

## More Ways of Using Different Java Comments in the Code
### 1. Nested Single-line Comments
A single-line comment that is written inside a block of code is called a nested single-line comment. Nesting is a term that refers to placing of a comment or an additional block of code inside another block of code. The compiler will skip the comment and continue to process the rest of the code.
```java
public class HelloWorld {
  //this is illustration of a nested comment
  public static void main(String[] args) {
   System.out.println("Hello World!");
  }
}
```

### 2. Nested Multi-line Comments
A multi-line comment placed inside a block of code is called a nested multi-line code. The example of it is given below:
```java
public class HelloWorld {
  /* This is an example of a nested
multi-line comment in java */
  public static void main(String[] args) {
   System.out.println("Hello World!");
  }
}
```

### 3. Single-line Comments Nested Inside Multi-line Comments
For some purposes, a single-line comment can be placed in a multi-line comment. As shown in the example below:
```java
public class HelloWorld {
  /* This is the beginning
  of a multi-line comment
  // This is a nested single line comment
   this is the end of the entire comment */
  public static void main(String[] args) {
   System.out.println("Hello World!");
  }
}
```
However, a multi-line comment cannot be nested inside another multi-line comment.
  
## Best Practices for Writing Java Comments
1. Remember that the comments are not subtitles and therefore, should not translate each line of code into simple language. That means, the comments are supposed to support the code so that when you or anybody comes back to it, they can make sense of it. Explaining the code in detail will only look silly and also make your code bulky.
2. Do not just repeat what you code is able to explain clearly. There are certain commands that are clear enough and do not need explanation. 
```java
System.out.println("Hello World!"); //prints Hello World! to //console.
```
   Above code is simple and clear. The comment in it is redundant and not required.

3. Smelly comments  need to be avoided at all cost. When you try to explain a code in detail so as to make sure the reader is not confused, it is a signal that something is wrong with your code and no comment can fix that.
4. Write your comments as you go and do not make it a habit of going back and commenting after code completion.
5. Keep the comments short and precise.
6. When you place comments inline, make sure they are separated from the main code with at least two spaces.
## Conclusion
A good program finally comes down to how concise and comprehendible it is. Java comments form a fundamental part of coding as codes generally tend to go on for thousands of lines. There can be multiple programmers contributing to it. In such cases, comments are very instrumental in consistent flow of information. The final code is as good as your comments are.

