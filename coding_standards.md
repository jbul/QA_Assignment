## Commenting:

Comments are the most simple way of explaining to both technically knowledgable and non-knowledgable poeple what your code is doing. For this reason, comments must be added in a number of situations. 

***Guidelines***

*	At the top of each class, add a breif comment about what the function of the class is and who created it.
*	For each method, add a comment briefly explaining what the method is doing.
*	If you believe a section of code does not appear to be obvious, add comments to briefly explain what it is for
*	Avoid obvious comments
*	Comments should typically be no longer than 1 or 2 lines

***Examples***

Bad:

/* This method was created to add a new user to the database, 
depending on if the user already exists in the database */
 public void addNewUser(){

}

Good:
/*Create new user with unique details*/
 public void addNewUser(){

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
