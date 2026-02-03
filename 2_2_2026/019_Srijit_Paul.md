# ASSIGNMENT – 2  
## MongoDB Compass (CLI – mongosh)

---

## Question 1  

In MongoDB Compass, use the CLI to perform the following operations:

1. Add **5 student records**
   - a) Insert **1 record** using `insertOne`
   - b) Insert **4 records** using `insertMany`
2. Remove the **1st record**
3. Query all students in the **"Computer"** department
4. Update the **"Computer"** department to **"BCA"**

---

## SOLUTION  

### Database Selection

```js
use semVI
switched to db semVI
db.students
semVI.students
db.students.insertOne({
  name: "Rahul",
  roll: 1,
  department: "Computer"
});

OUTPUT : 
{
  acknowledged: true,
  insertedId: ObjectId('6981b1539338b523b62053b5')
}



db.students.insertMany([
  { name: "Anita", roll: 2, department: "Computer" },
  { name: "Sourav", roll: 3, department: "Mechanical" },
  { name: "Priya", roll: 4, department: "Computer" },
  { name: "Rohit", roll: 5, department: "Electrical" }
]);

OUTPUT :

{
  acknowledged: true,
  insertedIds: {
    '0': ObjectId('6981b15f9338b523b62053b6'),
    '1': ObjectId('6981b15f9338b523b62053b7'),
    '2': ObjectId('6981b15f9338b523b62053b8'),
    '3': ObjectId('6981b15f9338b523b62053b9')
  }
}



SOLUTION 2

db.students.deleteOne({});

OUTPUT :

{
  acknowledged: true,
  deletedCount: 1
}



SOLUTION 3

db.students.find({ department: "Computer" });


OUTPUT :

{
  _id: ObjectId('6981b15f9338b523b62053b6'),
  name: 'Anita',
  roll: 2,
  department: 'Computer'
}

{
  _id: ObjectId('6981b15f9338b523b62053b8'),
  name: 'Priya',
  roll: 4,
  department: 'Computer'
}



SOLUTION 4 

db.students.updateMany(
  { department: "Computer" },
  { $set: { department: "BCA" } }
);

OUTPUT :
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 2,
  modifiedCount: 2,
  upsertedCount: 0


OPTIONAL

db.students.find()

{
  _id: ObjectId('6981b15f9338b523b62053b6'),
  name: 'Anita',
  roll: 2,
  department: 'BCA'
}

{
  _id: ObjectId('6981b15f9338b523b62053b7'),
  name: 'Sourav',
  roll: 3,
  department: 'Mechanical'
}
{
  _id: ObjectId('6981b15f9338b523b62053b8'),
  name: 'Priya',
  roll: 4,
  department: 'BCA'
}
{
  _id: ObjectId('6981b15f9338b523b62053b9'),
  name: 'Rohit',
  roll: 5,
  department: 'Electrical'
}
