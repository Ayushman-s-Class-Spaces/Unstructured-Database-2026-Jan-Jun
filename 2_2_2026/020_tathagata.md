LAB ASSIGNMENT-02: MongoDB CLI (CRUD)
In MongoDB Compass use CLI to:
1.ADD 5 students records 
 a.1 using insertOne
 b. 4 using insertMany
2. Remove the 1st Record
3. Query for all students in “Computer” department
4. Update “Computer” department to “BCA”

1a.  db["stu"].insertOne ({Roll:001, Name:"Tathagata Ghosh", Department: "Computer Science"})
{
  acknowledged: true,
  insertedId: ObjectId('69804015cb55a593f3f9b756')
}

1b. db["stu"].insertMany ([{Roll:011, Name:"Tathagata Ghosh", Department: "Computer Science"},{Roll:002, Name:"Tam Ghosh", Department: "Computer Science"},{Roll:031, Name:"Helen OF Troy", Department: "History"},{Roll:200, Name:"W.H.Haley", Department: "English"}])
{
  acknowledged: true,
  insertedIds: {
    '0': ObjectId('69804127cb55a593f3f9b757'),
    '1': ObjectId('69804127cb55a593f3f9b758'),
    '2': ObjectId('69804127cb55a593f3f9b759'),
    '3': ObjectId('69804127cb55a593f3f9b75a')
  }
}

2. db["stu"].deleteOne({Name:"Tam Ghosh"})
{
  acknowledged: true,
  deletedCount: 1
}

3.  db["stu"].find({Department :"Computer Science"})
{
  _id: ObjectId('69804127cb55a593f3f9b757'),
  Roll: 9,
  Name: 'Tathagata Ghosh',
  Department: 'Computer Science'
}

4. db["stu"].update({Department :"Computer Science"},{$set:{Department: "BCA"}})
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 1,
  modifiedCount: 1,
  upsertedCount: 0
}




