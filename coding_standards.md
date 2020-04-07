# Coding standards

**Follow naming conventions**  
Names are everywhere in the code. Whether it is variables, functions or packages. "Having irrelevant or contradicting names to your pages, variables, functions or arrays will only create troubles in the future."<br/>
Finding good names improves code maintainability and makes code more readable.

***Guildelines***
- The name of any variable, function or class should answer three big questions; why it exists, what it does and what it is used.
- The name of the variable or function should be understandable and meaningful. 
- Variables or functions naming should start with lowercase.
- Constant variable in capital lettters.
- Should follow language convention as well.<br/>
<b>For example</b>: Java recommend using camelCase convention ie. *firstName*, whereas Python recommend naming with underscore ie. *first_name*.

***Examples***

Bad:

<code>private long d; // elapsed time in days</code>

Good: 

<code>private long elapsedTimeInDays;</code>


**Indentation**  
"Imagine you go to a supermarket and there is no consistency over how the items are placed in the area. Some dairy products are at the clothing sections, others are at the cosmetics area, and bread products are placed with the vegetables."<br/> Indentation is the necessary arrangement that separate code blocks that belongs together.<br/>
Proper indentation is very important to increase the readability of the code.

***Guildelines***

- Indentation must be performed every time a code will be nested in another one.
- There should be a space after commas<br/>
- Code must use four spaces for indents, not the tab key.

***Examples***

Bad:

<code>
function myBadFunction (arg){<br/>
for(int i=0;i< 10;i++){<br/>
System.out.println ("I am the bad code"+i) ;<br/>    
}<br/>    
}<br/>
</code>

Good:

<code>
function myGoodFunction(args) {<br/>
&nbsp;&nbsp;&nbsp;&nbsp;for (int i=0; i < 10; i++) {<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;System.out.println("I am the bad code" + i);<br/>    
&nbsp;&nbsp;&nbsp;&nbsp;}<br/>    
}<br/>
</code>

**Code should be well documented**  
"Nothing can be more helpful than a well-placed comment. And nothing can be more damaging than comments that spread disinformation and lies".<br/>

***Guildelines***  
- Code changes, comments should evolve with code as well.
- Comments should state intent, not justify bad code
- Simple variables as well as getter / setters must not be commented
- Use language documentation (Javadoc, PHPDoc) on publicly accessible methods / classes

***Examples***  

Bad:

<code>
/**<br/>
&nbsp;The age of the person<br/>
*/<br/>
private int personAge;<br/>

/**  
Set the person age to the given integer personAge  
*/  
public void setPersonAge(int personAge) {  
&nbsp;&nbsp;&nbsp;&nbsp;this.personAge = personAge;   
}
</code>

Good:

<code>
/**<br/>
Do some business on the given param object<br/>
if param has this property, then do that
Given param must not be null.  <br/>
*/<br/>
public void apiMethod(Object param) { ... }
</code>

**A function/method should only do one thing**

***Guildelines***
- Method should be small. Ideal length of 15 lines.
- Maximum with 3 arguments.
- The indent level of a function should not be greater than one or two.

***Examples***  

Bad:  
<code>
private void myBadAddBookToShelf(String isbn, int yearPublished, String author, String title, String summary) {<br/>
&nbsp;&nbsp;if (isbn != null && isbn.length() > 10) {<br/>
&nbsp;&nbsp;&nbsp;&nbsp;if (author != null && author.contains(" ")) {<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;if (yearPublish > 0) {<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;shelf.add(new Book(isbn, yearPublished, author, title, summary));<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;} <br/>
&nbsp;&nbsp;&nbsp;&nbsp;}<br/>
&nbsp;&nbsp;}<br/>
}
</code>

Good:  
<code>
private void myGoodAddBookToShelf(Book bookToAdd) {<br/>
&nbsp;&nbsp;if (isValidBook(book)) {<br/>
&nbsp;&nbsp;&nbsp;&nbsp;shelf.add(book);<br/>
&nbsp;&nbsp;}<br/>
}
</code>  


***References***  
- https://www.geeksforgeeks.org/coding-standards-and-guidelines/
- https://towardsdatascience.com/how-to-write-clean-code-that-reduces-headaches-23ff6d933fdd
- https://www.codingdojo.com/blog/clean-code-techniques
- https://www.butterfly.com.au/blog/website-development/clean-high-quality-code-a-guide-on-how-to-become-a-better-programmer
- https://simpleprogrammer.com/clean-code-principles-better-programmer/
