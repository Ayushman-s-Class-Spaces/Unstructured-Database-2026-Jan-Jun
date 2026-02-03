# LAB ASSIGNMENT - 2
**<br>**
## *1. Add 5 student records*

+ a. Using insertOne
  **<br>**
db.students.insertOne({ name: "Alice", dept: "Computer", age: 20 })

+ b. Using insertMany
  **<br>** 
db.students.insertMany([
 **<br>** { name: "Bob", dept: "Electrical", age: 21 }
   **<br>** { name: "Charlie", dept: "Computer", age: 22 },
   **<br>**{ name: "David", dept: "Mechanical", age: 20 },
   **<br>**{ name: "Eve", dept: "Computer", age: 21 } ])

## *2. Remove the first record* 
db.students.deleteOne({}) 
 **<br>**

## *3. Query for all students in "computer" department*
db.students.find({ dept: "Computer" })
 **<br>**

## *4. Update "computer" department to "bca"*
db.students.updateMany({ dept: "Computer" }, { $set: { dept: "BCA" } })
 **<br>**
