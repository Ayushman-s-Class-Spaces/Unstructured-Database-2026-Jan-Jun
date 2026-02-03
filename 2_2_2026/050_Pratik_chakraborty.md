ASSIGNMENT 2
QUESTION:
In mongoDb compass use the CLI to 
1.Add 5 student records 
a. 1 using insertOne
b. 4 using insertMany
2. Remove the 1st record
3. Query for all the students in “computer” department
4. update “computer” department to “BCA”

db["sectiond"].insertOne({Roll : 001 , name : "Pratik Chakraborty" , department : "computer science"})
{
  acknowledged: true,
  insertedId: ObjectId('698034cf632dd840f74c75a2')
}

db["sectiond"].insertOne({Roll : 002 , name : "Aneesh Das" , department : "computer science"})

{
  acknowledged: true,
  insertedId: ObjectId('69803516632dd840f74c75a3')
}
db["sectiond"].insertMany([{Roll : 003 , name : "rony mukherjee" , department : "computer science"},{Roll : 004 , name : "tarun roy" , department : "computer science"},{Roll : 005 , name : "rohan mondal" , department : "computer science"},{Roll : 006 , name : "rahul roy" , department : "computer science"}])

{
  acknowledged: true,
  insertedIds: {
    '0': ObjectId('69803730632dd840f74c75a4'),
    '1': ObjectId('69803730632dd840f74c75a5'),
    '2': ObjectId('69803730632dd840f74c75a6'),
    '3': ObjectId('69803730632dd840f74c75a7')
  }
}

db["sectiond"].deleteOne({Roll : 2})

{
  acknowledged: true,
  deletedCount: 1
}

db["sectiond"].find({department : "computer science"})


  _id: ObjectId('698034cf632dd840f74c75a2'),
  Roll: 1,
  name: 'Abhishek Mukherjee',
  department: 'computer science'
}
{
  _id: ObjectId('69803730632dd840f74c75a4'),
  Roll: 3,
  name: 'rony mukherjee',
  department: 'computer science'
}
{
  _id: ObjectId('69803730632dd840f74c75a4'),
  Roll: 3,
  name: 'rony mukherjee',
  department: 'computer science'
}
{
  _id: ObjectId('69803730632dd840f74c75a5'),
  Roll: 4,
  name: 'tarun roy',
  department: 'computer science'
}
{
  _id: ObjectId('69803730632dd840f74c75a6'),
  Roll: 5,
  name: 'rohan mondal',
  department: 'computer science'
}
{
  _id: ObjectId('69803730632dd840f74c75a7'),
  Roll: 6,
  name: 'rahul roy',
  department: 'computer science'
}
db["sectiond"].updateMany({department : "computer science"},{$set:{department: "BCA"}})

{
  acknowledged: true,
  insertedId: null,
  matchedCount: 5,
  modifiedCount: 5,
  upsertedCount: 0
}
db["sectiond"].find({department : "BCA"})

{
  _id: ObjectId('698034cf632dd840f74c75a2'),
  Roll: 1,
  name: 'Abhishek Mukherjee',
  department: 'BCA'
}
{
  _id: ObjectId('69803730632dd840f74c75a4'),
  Roll: 3,
  name: 'rony mukherjee',
  department: 'BCA'
}
{
  _id: ObjectId('69803730632dd840f74c75a5'),
  Roll: 4,
  name: 'tarun roy',
  department: 'BCA'
}
{
  _id: ObjectId('69803730632dd840f74c75a6'),
  Roll: 5,
  name: 'rohan mondal',
  department: 'BCA'
}
{
  _id: ObjectId('69803730632dd840f74c75a7'),
  Roll: 6,
  name: 'rahul roy',
  department: 'BCA'
}
