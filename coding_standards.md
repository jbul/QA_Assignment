# Testing:

Testing can be a massive timesaver as you can automate repetetive tasks, removing the need to manually test new features every time you want to deploy code. 

***Guidelines***

*	Ensure tests are simple and readable.
*   One test should only test one thing. If you have more than one task being tested, create new tests for each task.
*	There should be a test for every feature.
*	Every new feature should have a new test implemented before it is deployed.
*	If a new feature changes how code works, each effected test must be updated.

***Examples***

Bad:

//This test is bad as it is testing two different methods

@Test

public void generalTest(){

    asertEquals(4, MainClass.multiply(2,2));
    assertEquals("1997", MainClass.getYear("Test User"));
}

Good:

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

https://code.tutsplus.com/tutorials/top-15-best-practices-for-writing-super-readable-code--net-8118

https://www.vogella.com/tutorials/JUnit/article.html