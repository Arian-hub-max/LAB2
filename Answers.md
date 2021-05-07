# Student Details

Name: Arian Eskandarinejad

ID: s3884975


<br />

# Activity 2

## Question 1:

Write your answere here. Leave a blank space between paragraphs.

No return value for searchbyAuthor() method in Catalog object so that the student can recognize the VISIBLE output (whether the book is available or not). In other words, when the student put search and enter, he can not see the list of result to submit . so we add a method for submitReuquest() for student.

There is no method for the student to search the book, we then add search() for student object.
the system can not update account, update the catalog and print receipt all at the exact same time , so there should be little distance between them (diagonally) 

For the alternative option, there should be two conditions, the first one can have an initial status of ‘rejected’ which is for isAvailable() method (in case the book and loan is not available) and the second condition starts with  'else' which referes to the acceptance of it. Hence for solution.we need to divide the alt frame for 2 condtions and also delete methods searchByAuthor(), isAvailable(bookID) and their time activation.

Also we don't need to repeat any methods after isAvailable(bookID) before the alt frame , as the alt frame already mention them in 'else' condition, so we just delete them


## Question 2:

Write your answere here. Leave a blank space between paragraphs.

No, when the book is in onHold state it means it is waiting to be either ‘available’ or ‘unavailable’ which is not related to the presentation level for the customer and should not be recorded in the database


## Question 3:

Write your answere here. Leave a blank space between paragraphs.
You can find the modified sequence diagram in https://lucid.app/lucidchart/aa8767a6-9ad5-46a8-9dad-497d6177dfc5/edit?page=0_0#


<br />


# Activity 3

## Question 4:

Write your answere here. Leave a blank space between paragraphs.

I’ve made a couple of assumptions : 
1. The association multiplicity: there is a 0..* - 1..* relationship between Book and Loan, which means that for one loan, a book may not be available (as we see in the alternative frame of sequence diagram) and same for one book as well. The second association is between catalog and student. I assume there is one catalog (act as system operator or system boundary) exists which can have 0 to many users (students).  Plus this catalog may don’t have any books available (so 0 to many books for catalog).

2 . Methods: For catalog, the author’s name is probably searched by name, so I put the parameter as string. For class Book, bookID is an integer which can be available or not (hence the function is Boolean). For loan , all the methods are void but checkFines() and payFines() are private (with – sign) because they are self-methods and are only accessible by themselves. 

3. Attributes: I assume that each student needs to be identified or contacted with certain (with at least one unique) details including student ID and full name. For catalog, according to searchByAuthor() method, I assume that we need Author details like ID and name as attributes. For book, plus bookID (which used to link to the specific loan), other details like title, publish date and summary are used to be presented to the student on presentation layer. For loan, as it does check and pay fines, we need to include amount. We use ID to identify each loan case for each specific student ID. We also include title for each loan program so that it is easy for the student to recognize

## Question 5:
For searchByAuthor in Catalog, I could out authorName as string parameter but because authorID is unique for each author and no duplicates show up, then I chose authorID
For newSearch() method in Student, it can include a keyword (String) which is entered by the student as input but I interpreted it as the action of renewal of search function so I made it a void method



