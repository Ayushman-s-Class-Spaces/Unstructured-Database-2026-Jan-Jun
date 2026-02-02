// Insert one record
db.students.insertOne({
  name: "Anita",
  age: 19,
  department: "Computer",
  roll: 102
})

// Insert many records
db.students.insertMany([
  { name: "Suman", age: 21, department: "IT", roll: 103 },
  { name: "Riya", age: 20, department: "Computer", roll: 104 },
  { name: "Aman", age: 22, department: "Civil", roll: 105 }
])

// Find Computer department students
db.students.find({ department: "Computer" })

// Update Computer to BCA
db.students.updateMany(
  { department: "Computer" },
  { $set: { department: "BCA" } }
)

// Delete first record
db.students.deleteOne({ roll: 102 })
