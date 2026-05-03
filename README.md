# MongoDB Library Database Operations

This project demonstrates basic MongoDB database operations using the Mongo Shell (`mongosh`).
The database used in this project is `library`, and the collection used is `books`.

## Features

* Insert documents into MongoDB collection
* Find specific documents
* Display all records
* Update multiple documents
* Sort records using published year
* Limit query results
* Use OR condition with regular expressions

---

## Technologies Used

* MongoDB
* Mongo Shell (mongosh)
* Command Prompt (CMD)

---

## Database Name

```bash
library
```

## Collection Name

```bash
books
```

---

## Operations Performed

### 1. Insert One Document

```javascript
db.books.insertOne({
  title:"Javascript Advanced",
  author:"Tom George",
  published_year:2025,
  genre:"Mystery"
})
```

---

### 2. Find Specific Document

```javascript
db.books.find({title:"Javascript Advanced"})
```

---

### 3. Display All Documents

```javascript
db.books.find()
```

---

### 4. Update Multiple Documents

```javascript
db.books.updateMany(
  {},
  {$set:{edition:"II"}}
)
```

---

### 5. Sort and Limit Results

```javascript
db.books.find()
.sort({published_year:-1})
.limit(3)
```

---

### 6. OR Condition with Regex

```javascript
db.books.find({
  $or:[
    {title:/MongoDB/i},
    {title:/NoAQL/i}
  ]
})
```

---

## Project Output

The project output screenshots are included in the PDF report.

---

## Author

Created for MongoDB practice and database operations learning.
