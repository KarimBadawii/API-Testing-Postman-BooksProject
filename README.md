# 📘 Books API Testing with Postman

This project demonstrates API testing using **Postman** for a simple Book Management system.  
It covers core CRUD operations with automated test scripts to validate API responses.

---

## 🔍 Overview

The collection includes the following endpoints:

| Method | Endpoint | Description |
|:-------|:----------|:-------------|
| **POST** | `/AddBook` | Add a new book to the system |
| **GET** | `/GetBook.php?ID={id}` | Retrieve a book by ID |
| **GET** | `/GetBook.php?AuthorName={name}` | Retrieve books by author name |
| **DELETE** | `/DeleteBook` | Delete a book by ID |

---

## 🧠 Features

- All requests built and validated in **Postman**
- Dynamic **JavaScript test scripts** for response validation
- Assertions for status codes, response content, and structure
- Focused on real-world API testing scenarios

---

## ⚙️ Tools & Technologies

- Postman  
- JavaScript (for test scripts)  
- RESTful API concepts  
- JSON  

---

## 📂 Repository Structure
├── Books_API_Testing.postman_collection.json

└──Library.postman_test_run.json

└── README.md

---

## 🧾 Sample Test Script

```javascript
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});

pm.test("Response has book ID", function () {
    const jsonData = pm.response.json();
    pm.expect(jsonData.ID).to.exist;
});
