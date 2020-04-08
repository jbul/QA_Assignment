# Coding standards

## Follow naming conventions  
Names are everywhere in the code. Whether it is variables, functions or packages. "Having irrelevant or contradicting names to your pages, variables, functions or arrays will only create troubles in the future."<br/>
Finding good names improves code maintainability and makes code more readable.



***Guidelines***
- The name of any variable, function or class should answer three big questions; why it exists, what it does and what it is used.
- The name of the variable or function should be understandable and meaningful. 
- Variables or functions naming should start with lowercase.
- Constant variable in capital letters.
- Should follow language convention as well.<br/>
<b>For example</b>: Java recommend using camelCase convention ie. *firstName*, whereas Python recommend naming with underscore ie. *first_name*.

***Examples***

Bad:

```java
private long d; // elapsed time in days
```

Good: 

```java
private long elapsedTimeInDays;
```

## Indentation  
"Imagine you go to a supermarket and there is no consistency over how the items are placed in the area. Some dairy products are at the clothing sections, others are at the cosmetics area, and bread products are placed with the vegetables."<br/> Indentation is the necessary arrangement that separate code blocks that belongs together.<br/>
Proper indentation is very important to increase the readability of the code.

***Guidelines***

- Indentation must be performed every time a code will be nested in another one.
- There should be a space after commas<br/>
- Code must use four spaces for indents, not the tab key.

***Examples***

Bad:

```java
public void myBadFunction (arg){
for(int i=0;i< 10;i++){
System.out.println ("I am the bad code"+i) ;   
}    
}
```

Good:

```java
public void myGoodFunction(args) {
    for (int i=0; i < 10; i++) {
        System.out.println("I am the good code" + i);  
    }   
}
```

## Code should be well documented  
"Nothing can be more helpful than a well-placed comment. And nothing can be more damaging than comments that spread disinformation and lies".<br/>

***Guidelines***  
- Code changes, comments should evolve with code as well.
- Comments should state intent, not justify bad code
- Simple variables as well as getter / setters must not be commented
- Use language documentation (Javadoc, PHPDoc) on publicly accessible methods / classes

***Examples***  


Bad:

```java
/**<br/>
 * The age of the person<br/>
*/
private int personAge;

/**  
Set the person age to the given integer personAge  
*/  
public void setPersonAge(int personAge) {  
    this.personAge = personAge;   
}
```

Good:

```java
/**
 * Do some business on the given param object<br/>
 * if param has this property, then do that
 * Given param must not be null.  <br/>
*/
public void apiMethod(Object param) { ... }
```

**A function/method should only do one thing**

***Guidelines***
- Method should be small. Ideal length of 15 lines.
- Maximum with 3 arguments.
- The indent level of a function should not be greater than one or two.

***Examples***  

Bad:  
```java
private void myBadAddBookToShelf(String isbn, int yearPublished, String author, String title, String summary) {
    if (isbn != null && isbn.length() > 10) {
        if (author != null && author.contains(" ")) {
            if (yearPublish > 0) {
                shelf.add(new Book(isbn, yearPublished, author, title, summary));
            }
        }
    }
}
```

Good:  
```java
private void myGoodAddBookToShelf(Book bookToAdd) {
    if (isValidBook(book)) {
        shelf.add(book);
    }
}
```  

## Testing:

Testing can be a massive timesaver as you can automate repetetive tasks, removing the need to manually test new features every time you want to deploy code. 

***Guidelines***

*	Ensure tests are simple and readable.
*   One test should only test one thing. If you have more than one task being tested, create new tests for each task.
*	There should be a test for every feature.
*	Every new feature should have a new test implemented before it is deployed.
*	If a new feature changes how code works, each effected test must be updated.

***Examples***

Bad:

```java
//This test is bad as it is testing two different methods

@Test
public void generalTest(){

    asertEquals(4, MainClass.multiply(2,2));
    assertEquals("1997", MainClass.getYear("Test User"));
}
```

Good:
```java
//These tests are good as they are each testing two different methods

@Test
public void multiplyTest(){

    asertEquals(4, MainClass.multiply(2,2));
    assertEquals(6, MainClass.multiply(2,3));
    assertEquals(70, MainClass.multiply(10,7));

}

@Test

public void getYearTest(){

    assertEquals("1997", MainClass.getYear("Test User"));
    assertEquals("1997", MainClass.getYear("John Smith"));
    assertEquals("1997", MainClass.getYear("Jack Johnson"));
}
```
## File and Folder Organization
Using good file and folder organization can help to ensure that a project is easier to navigate around. Although this seems like a simple thing, having files organized can save a team a significant amount of time.

***Guidelines***

* Give files meaningful names
* Create folders for different class types *e.g. Objects, DAO's Resource files*
* Avoid having a large number of nested folders

***Examples***

Bad:

A long list of files with no organization

Good:

A well organized file structure that has folders for all file types


***References***  
- https://www.geeksforgeeks.org/coding-standards-and-guidelines/
- https://towardsdatascience.com/how-to-write-clean-code-that-reduces-headaches-23ff6d933fdd
- https://www.codingdojo.com/blog/clean-code-techniques
- https://www.butterfly.com.au/blog/website-development/clean-high-quality-code-a-guide-on-how-to-become-a-better-programmer
- https://simpleprogrammer.com/clean-code-principles-better-programmer/
