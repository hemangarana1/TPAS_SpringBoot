## Project Setup

This project uses the following dependencies:
- Spring Web
- Spring Data JPA
- PostgreSQL

## Book Entity

The `Book` entity has the following fields:
- `id` (Long): Auto-generated identifier.
- `title` (String): Title of the book.
- `author` (String): Author of the book.
- `isbn` (String): ISBN of the book.

## Repository

The `BookRepository` interface extends `JpaRepository<Book, Long>`.

## Service

The `BookService` class provides the following methods:
- `List<Book> getAllBooks()`: Retrieves all books.
- `Optional<Book> getBookById(Long id)`: Retrieves a book by its ID.
- `Book saveBook(Book book)`: Saves a new book or updates an existing one.
- `void deleteBook(Long id)`: Deletes a book by its ID.

## Controller

The `BookController` class exposes the following endpoints:
- `GET /books`: Retrieve all books.
- `GET /books/{id}`: Retrieve a book by its ID.
- `POST /books`: Create a new book.
- `PUT /books/{id}`: Update an existing book.
- `DELETE /books/{id}`: Delete a book by its ID.