LIBRARY MANAGEMENT SYSTEM
README DOCUMENTATION

1. SYSTEM OVERVIEW
The Library Management System is a C++ console application designed to manage book inventory, member registrations, and borrowing/returning transactions in a library. It implements object-oriented programming principles with classes for books, members, transactions, and library operations.

2. FEATURES
- Book Management:
  • Add new books (Fiction, Non-Fiction, Reference)
  • Display all available books
  • Search books by ID, title, author, or type
  • Sort books by ID or title

- Member Management:
  • Register new members
  • Track borrowed books
  • Display member information
  • Enforce borrowing limits (max 5 books per member)

- Transaction Processing:
  • Borrow books with date tracking
  • Return books with automatic availability update
  • View recent transactions
  • Process returns queue

3. CLASS STRUCTURE

3.1 BOOK CLASSES
• Book (Base Class)
  - Attributes: bookID, title, author, isAvailable
  - Methods: getters/setters, displayDetails(), getType()

• FictionBook (Derived)
  - Additional: genre

• NonFictionBook (Derived)
  - Additional: subject

• ReferenceBook (Derived)
  - Special: Cannot be borrowed

3.2 MEMBER CLASS
- Attributes: memberID, name, borrowedBooks list
- Methods: borrowBook(), returnBook(), displayDetails()

3.3 TRANSACTION CLASS
- Attributes: transactionID, memberID, bookID, type, date
- Methods: displayDetails()

3.4 LIBRARIAN CLASS
- Handles: processBorrow(), processReturn()

3.5 BOOKSEARCHER CLASS
- Static methods for searching: by ID, title, author, type

3.6 LIBRARY CLASS (Main Controller)
- Manages collections of books and members
- Processes all transactions
- Maintains transaction log and return queue

4. HOW TO USE

4.1 COMPILATION
1. Save all code in a single .cpp file (e.g., LibrarySystem.cpp)
2. Compile using: g++ LibrarySystem.cpp -o LibrarySystem
3. Run the executable: ./LibrarySystem

4.2 MENU OPTIONS
1. Add Book - Register new books with details
2. Add Member - Create new library members
3. Borrow Book - Check out books to members
4. Return Book - Check in returned books
5. Display Books - Show all available books
6. Display Members - List all registered members
7. Search Books - Find books by various criteria
8. View Transactions - See recent borrowing history
9. Process Returns - Update availability of returned books
10. Sort Books - Organize books by ID or title
0. Exit - Close the application

5. SAMPLE DATA
The system comes pre-loaded with sample data:
- Books:
  • Fiction: The Great Gatsby, Dune
  • Non-Fiction: Sapiens
  • Reference: Oxford Dictionary
- Members: Shashwat Anand (ID: 113)

6. ERROR HANDLING
The system includes validation for:
- Duplicate book borrowing
- Exceeding borrowing limits
- Invalid member/book IDs
- Attempting to borrow unavailable books

7. TECHNICAL NOTES
- Uses STL containers: vector, stack, queue
- Implements polymorphism for book types
- Follows OOP principles with encapsulation
- Includes proper memory management

8. LIMITATIONS
- Console-based interface (no GUI)
- Data not persistent between runs
- Basic error handling with C-strings

9. FUTURE ENHANCEMENTS
- Database integration for persistent storage
- Graphical user interface
- Advanced reporting features
- Fine management for late returns
- User authentication system

10. AUTHOR
Shashwat Anand


