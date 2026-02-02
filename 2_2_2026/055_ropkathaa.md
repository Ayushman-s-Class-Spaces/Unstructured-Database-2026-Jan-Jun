# Unstructured Databases Lab
**Date:** 02-02-2026  
**Course:** Unstructured Databases Lab

**Student Name:** Ropkathaa Choudhury  
**Roll No:** 055  

## Objective
To perform basic MongoDB CRUD operations using MongoDB Compass CLI.

## Step 1: Switch to Database
```js
use Record
```
**Output**
```
switched to db Record
```

## Step 2: Insert One Student Record (insertOne)
```js
db.student.insertOne({
  roll_no: "UG/02/CSE/001",
  name: "Promit Kumar",
  department: "Computer",
  course: "B.Tech",
  address: "Kolkata",
  dob: "2003-01-12"
})
```
**Output**
```
acknowledged: true
```

## Step 3: Insert Multiple Student Records (insertMany)
```js
db.student.insertMany([
  {
    roll_no: "UG/02/CSE/002",
    name: "Riya Sharma",
    department: "Computer",
    course: "B.Tech",
    address: "Howrah",
    dob: "2003-02-18"
  },
  {
    roll_no: "UG/02/CSE/003",
    name: "Suman Patra",
    department: "Computer",
    course: "B.Tech",
    address: "Midnapore",
    dob: "2002-05-20"
  },
  {
    roll_no: "UG/02/CSE/004",
    name: "Monalisa Dey",
    department: "Computer",
    course: "B.Tech",
    address: "Alipurduar",
    dob: "2003-03-02"
  },
  {
    roll_no: "UG/02/CSE/005",
    name: "Abhishek Paul",
    department: "Computer",
    course: "B.Tech",
    address: "Kharagpur",
    dob: "2002-10-16"
  }
])
```
**Output**
```
acknowledged: true
```

## Step 4: Delete the First Student Record
```js
db.student.deleteOne({ roll_no: "UG/02/CSE/001" })

**Output**
deletedCount: 1
```

## Step 5: Query Students from Computer Department
```js
db.student.find({ department: "Computer" })
```
**Output**
```
Displays all students belonging to the Computer department
```

## Step 6: Update Department from Computer to BCA
```js
db.student.updateMany(
  { department: "Computer" },
  { $set: { department: "BCA" } }
)
```
**Output**
```
matchedCount > 0
modifiedCount > 0
```

## Conclusion
MongoDB CRUD operations were successfully performed using MongoDB Compass CLI.

