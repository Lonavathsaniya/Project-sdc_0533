Book Management System — Theory Explanation

Overview:
----------
This project implements a Book Management System using HTML, CSS, and JavaScript. It allows users to register, log in, and manage books (add, delete, borrow, return, search). Data is stored locally using browser's Local Storage to maintain persistence even after page reloads.

User Authentication System:
----------------------------
1. Registration:
   - Users enter username and password.
   - Data is saved in Local Storage as JSON under key "user".
   - After registration, user proceeds to login.
2. Login:
   - User inputs credentials.
   - Credentials are validated against stored data.
   - If valid, username is stored as "loggedInUser" in Local Storage to maintain session.

3. Logout:
   - Clears "loggedInUser" from Local Storage.
   - Displays login/register screen again.

Note: No encryption is used. Suitable for demo/educational purposes only.

Book Management Features:
-------------------------
- Adding Books:
  - Form collects Title, Author, Year, and Cover Image.
  - Image converted to Base64 using FileReader API.
  - Each book assigned unique ID and status "Available".

- Storing Books:
  - All books stored in an array (books[]).
  - Saved in Local Storage as JSON under "books" key.

- Deleting Books:
  - User can delete book using unique ID.

- Borrowing Books:
  - User inputs book title.
  - If available, status updated to "Borrowed".

- Returning Books:
  - User inputs book title.
  - If borrowed, status updated back to "Available".

- Searching Books:
  - Search supported by Title, Author, or Year.
  - Results displayed dynamically.

Application Navigation:
------------------------
- Uses showSection(id) function to dynamically hide/show sections.
- Main app displayed only after successful login.
- Menu provides access to:
  - Add Book
  - Show All Books
  - Show Available Books
  - Borrow Book
  - Return Book
  - Search by Title
  - Search by Author
  - Logout

CSS Design Highlights:
-----------------------
- Body styled with background image, Arial font, padding.
- Headings centered with color #2c3e50.
- Authentication buttons centered using flexbox.
- Forms have card-like design with shadows, rounded corners.
- Buttons styled with hover effects for interactivity.
- Book list displayed in styled tables with image thumbnails.
- Delete buttons styled in red for action clarity.

HTML Structure Overview:
-------------------------
- DOCTYPE HTML5, language set to English.
- Linked to external stylesheet (style.css).
- Authentication Menu:
  - Shows Register and Login buttons.
  - Forms hidden by default.
- Register & Login Forms:
  - Fields: Username and Password.
  - Form submission handled via JavaScript.
- Main App:
  - Displays only after login.
  - Contains book management features.
- Add Book Form:
  - Fields: Title, Author, Year, Image Upload.
- Book List Table:
  - Displays all books dynamically with actions.
- JavaScript linked at end (script.js) to control all functionality.

Security Considerations:
-------------------------
- Data stored in Local Storage as plain text.
- No encryption or password hashing.
- Not recommended for production use.
- Only for learning/demo purposes.

