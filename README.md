# Library-System
A simple library system developed for MPP class using JavaFX

Library System developed for a Java course project.
Verry simple, work done in tree days, there a lot of problems and mistakes done.
But the system overall works.

Here is the problem requirements:

Library Problem Statement
Create the first iteration of a system that a librarian can use to check out books for library members, and
that an administrator can use to add new books to the collection, create new library members, and edit
library member information.
Most books may be borrowed for 21 days, but some books only for 7 days.
All members of the library are assigned a unique member number. First and last names, address (street,
city, state, zip) and phone number of every member are also stored as member data.
Books have a title, ISBN number, list of authors, and availability. Authors have first and last names,
address (street, city, state, zip), phone number, credentials, and a short bio.
The library has multiple copies for some popular books. Every copy of a book has its own unique copy
number. (Note: A “copy” of a book is an instance of the book. For every book in a library, there is at least
one copy; for popular books, there may be more than one copy. In this context, a “copy” of a book is not
a reproduction of an original; this is a different meaning of “copy,” not used here.)
Also, for each library member, the system will keep a record of his/her checkout activities in a checkout
record. A checkout record consists of a collection of checkout entries. Each entry records each item
checked out, the date of checkout, and the due date. The checkout record for a library member is
therefore a complete record of every book that the member has ever checked out. We expect that in
later phases of the library system, the checkout record will also include a record of fines for later returns
and dates paid.
In order to access the system, a librarian or administrator must login. Administrators are able to
add/edit member info and add books to the collection, but they are not allowed to checkout books for a
member (unless they also have Librarian access). Librarians are allowed to checkout books but not
allowed to add/edit members or add books (unless they also have Administrator access). 
Functional Requirements
The system you design should support the following statements:
1. Login
 The first screen a user of the system sees is the login screen, which requests ID and
password. When the Submit button is clicked, the ID is looked up in the data store. If this ID
can be found, and if the password for this ID matches the password submitted, the
authorization level is returned. Authorization levels are LIBRARIAN, ADMIN, and BOTH. If
login is successful, UI features are made available according to the authorization level of the
user.
2. Add a new library member to the system.
 When an Administrator selects the option to add a new member, is presented with a form
with the following fields: member id, first name, last name, street, city, state, zip, telephone
number.
3. Checkout a book for a library member.
 A librarian can enter in a form a member ID and see a list of the books that member
checkout records. The librarian can enter the ISBN number for a book and ask the system
whether the requested item is available for checkout. If ID is not found, the system will
display a message indicating this, or if the requested book is not found or if none of the
copies of the book are available, the system will return a message indicating that the item is
not available. If both member ID and book ID are found and a copy is available, a new
checkout record entry is created, containing the copy of the requested book and the
checkout date and due date. This checkout entry is then added to the member’s checkout
record. The copy that is checked out is marked as unavailable. The updated checkout
record is displayed on the UI. The display of the checkout record should use a TableView.
The librarian can continue cheking out more books for that member or start the process
with another member.
4. Add a copy of an existing book to the library collection.
 An administrator can look up a book by ISBN and add a copy to the collection.
5. Add a book to the library collection.
 An Administrator can add a book by selecting an “add book” option. The system responds by
displaying a screen with the necessary fields (ISBN, title, authors, maximum checkout length,
number of copies).
6. [Groups with more than 4 members] Given a library member id, print (to console) the checkout
record of that library member
 The Librarian can search for a library member by ID, and then select an option to print the
checkout record. When this is done, the checkout record appears in the console with
aligned columns.
