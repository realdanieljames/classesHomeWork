//Create a Student and a Classroom Class
//
class Student {
    //  class is instantiated it should have a name, favoriteSubject, and gpa variable
    constructor(name, favoriteSubject, gpa) {
        this.name = name;
        this.favoriteSubject = favoriteSubject;
        this.gpa = gpa;
    }

    //   create a studentDescribe method
    //  if name is 'Joe' favoriteSubject is 'science' and gpa is 4.0' 
    //  the method should log: 'Joe favorite subject is science. Joe has a gpa of 4.0.
    studentDescribe() {
        return `${this.name} favorite subject is ${this.favoriteSubject}. ${this.name} has a gpa of ${this.gpa}`
    }
}


class Classroom {
    //  Create an empty array where we can add students
    constructor(professor, roomNumber) {
        this.students = [];

        //  Create a professor and roomNumber property
        this.professor = professor;
        this.roomNumber = roomNumber
    }
    //  Create a classDescribe method
    //  If the arguments for a new instance of Classroom are ‘Professor Johnson’ for professor, 
    //  417 for the roomNumber 
    //  and the number of students is 12
    //  should log: "Professor Johnson's class is in room 417. Professor Johnson has 12 students
    classDescribe() {
        return `${this.professor}'s class is in room ${this.roomNumber}. ${this.professor} has ${this.students.length} students`
    };

    //  create a method called addStudent that can add a student to the students array
    addStudent(studentName) {
        return this.students.push(studentName)
    };

    //  create a studentCount method
    //  for example, there are 5 students, will log: 'There are 5 students in the class'
    studentCount() {
        return `There are ${this.students.length} students in the class`
    }

    //  create a method called studentNames in the Classroom class. 
    //  It should log each name of the students in the classroom one by one.
    studentNames() {
        for (const student of this.students){
            console.log(student.name)
        }
    }
}





//  Create two new Student instances and give them values. 
//  They should be called called student1 and student2
let student1 = new Student('Daniel', 'coding', 100)
let student2 = new Student('James', 'investing', 100)

//  Describe each student by logging them with your method.
console.log(student1.studentDescribe())
console.log(student2.studentDescribe())

//  Create a new Classroom instance called firstClass and add values.
let firstClass = new Classroom('Professor Johnson', 417);


//  Add the two students to the new classroom
firstClass.addStudent(student1)
firstClass.addStudent(student2)

//   Use your method to describe the class
firstClass.classDescribe()


//   change the name of student one to Peter using your instantiated student2
student1.name = 'Peter'


//  Call firstClass and chain the studentCount and studentNames methods
// firstClass.studentCount.studentName
console.log(firstClass.studentCount.studentNames)

