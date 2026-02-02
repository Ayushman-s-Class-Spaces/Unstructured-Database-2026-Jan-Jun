# In Mongodb Compass Use The CLI to
## Add 5 students records 
- 1 using insertOne
- 4 using insertMany
### code:
**use college**
<br>
**switched to db college**
<br>
### 1 using insertOne
**db.students.insertOne({
<br>
  studentId: 1,
  <br>
  name: "Amit Sharma",
  <br>
  age: 20,
  <br>
  department: "CSE",
  <br>
  cgpa: 8.5
<br>
})**
### output:
<img width="431" height="94" alt="image" src="https://github.com/user-attachments/assets/ce8c14a1-a652-4dde-844b-749d3e946239" />

### 4 using insertMany:
**db.students.insertMany([
<br>
  {<br>
    studentId: 2,
    <br>
    name: "Priya Singh",
    <br>
    age: 21,
    <br>
    department: "IT",
    <br>
    cgpa: 8.1
    <br>
  },
  <br>
  {<br>
    studentId: 3,
    <br>
    name: "Rahul Verma",
    <br>
    age: 22,
    <br>
    department: "ECE",
    <br>
    cgpa: 7.9
    <br>
  },
<br>
  {<br>
    studentId: 4,
    <br>
    name: "Neha Gupta",
    <br>
    age: 20,<br>
    department: "CSE",
    <br>
    cgpa: 8.8
    <br>
  },
  <br>
  {<br>
    studentId: 5,
    <br>
    name: "Karan Mehta",<br>
    age: 21,<br>
    department: "ME",<br>
    cgpa: 7.5<br>
  }
  <br>
])**

### output:
<img width="427" height="202" alt="image" src="https://github.com/user-attachments/assets/c9f2f03f-d494-432a-8c92-099e0b15aef4" />

## Remove the 1st record:

### code:
**db.students.deleteOne({ studentId: 1 })**

### output:
<img width="323" height="84" alt="image" src="https://github.com/user-attachments/assets/88ff7057-97f5-4ee2-ac77-22c83b256e34" />

## Query for all students in "computer" depertment

### code:
**db.students.find({ department: "CSE" }).pretty()**

### output:
<img width="379" height="183" alt="image" src="https://github.com/user-attachments/assets/17e5b351-ba17-49b7-8779-c1e2f6c00ae5" />

## Update "computer" depertment to "BCA":

### code:
**db.students.updateMany(
<br>
  { department: "CSE" },
  <br>
  { $set: { department: "BCA" } }
  <br>
)**

### output:
<img width="259" height="158" alt="image" src="https://github.com/user-attachments/assets/e19249ed-7a8f-427a-a91a-cba468d02a25" />

## To check the update:

### code:
**db.students.find().pretty()**

### output:
<img width="484" height="738" alt="image" src="https://github.com/user-attachments/assets/44567fca-1629-491c-aa21-6a666d6677ca" />

# Final output

### Before:
<img width="1920" height="1020" alt="Screenshot 2026-02-02 110306" src="https://github.com/user-attachments/assets/115db8d2-82b3-4142-816d-92a9068f33ee" />

### After:
<img width="1266" height="1020" alt="image" src="https://github.com/user-attachments/assets/d632a89a-c43f-4395-95e5-c53ed6e2e720" />




