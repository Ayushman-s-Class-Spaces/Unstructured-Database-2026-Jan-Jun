# Assignment-2

# ADD 5 STUDENTS RECORDS:

db.students.insertOne({
<br>
  name: "John Doe",
  <br>
  department: "Computer",
  <br>
  age: 21
  <br>
});



# USING INSERTMANY:
db.students.insertMany([
<br>
  { name: "John Doe", department: "Computer", age: 21 },
  <br>
  { name: "Jane Smith", department: "Computer", age: 22 },
  <br>
  { name: "Sam Wilson", department: "Computer", age: 20 },
  <br>
  { name: "Lisa Brown", department: "Computer", age: 23 },
  <br>
  { name: "Mark Lee", department: "Computer", age: 21 }
  <br>
]);

# REMOVE FIRST RECORD:
db.students.deleteOne({ _id: db.students.find().limit(1).toArray()[0]._id });

# QUERY FOR ALL STUDENTS:
db.students.find({ department: "Computer" });

# UPDATE COMPUTER:
db.students.updateMany(
<br>
  { department: "Computer" },
  <br>
  { $set: { department: "BCA" } }
  <br>
);
