# Day 7

## 1. Write a JavaScript program to list the properties of a JavaScript object. 
``` javascript
Sample object: var student = { name : "David Rayy", sclass : "VI", rollno : 12 }; 
Sample Output: name,sclass,rollno
```
### Ans:
``` javascript
var student = {
    name: "David Rayy",
    sclass: "VI",
    rollno: 12
  };
  for(var key in student){
    console.log(key)
  };
```
## 2. Write a JavaScript program to delete the rollno property from the following object. Also print the object before or after deleting the property. 
``` javascript
Sample object: var student = { name : "David Rayy", sclass : "VI", rollno : 12 }; 
```
### Ans:
``` javascript
  var student = {
    name : "David Rayy", sclass : "VI", rollno : 12 };
    console.log(student);
    delete student.rollno;
    console.log(student);
```
## 3. Write a JavaScript program to get the length of a JavaScript object.  
``` javascript
Sample object : var student = { name : "David Rayy", sclass : "VI", rollno : 12 }; 
```
### Ans:
``` javascript
    var student = { name : "David Rayy", sclass : "VI", rollno : 12 };
    var a = [];
    for(var i in student){
    a.push(i);
    };

    console.log(a.length);
```
## 4. Write a JavaScript program to display the reading status (i.e. display book name, author name and reading status) of the following books. 
``` javascript
var library = [ { author: 'Bill Gates', title: 'The Road Ahead', readingStatus: true }, { author: 'Steve Jobs', title: 'Walter Isaacson', readingStatus: true }, { author: 'Suzanne Collins', title: 'Mockingjay: The Final Book of The Hunger Games', readingStatus: false }]; 
```
### Ans:
``` javascript
   var library = [ { 
        author: 'Bill Gates', title: 'The Road Ahead', readingStatus: true },
        { author: 'Steve Jobs', title: 'Walter Isaacson', readingStatus: true },
        { author: 'Suzanne Collins', title: 'Mockingjay: The Final Book of The Hunger Games', readingStatus: false }];

        library.forEach((value) => {
        console.log(value.author);
        console.log(value.title);
        console.log(value.readingStatus);
        });
```
## 5. Write a JavaScript program to get the volume of a Cylinder with four decimal places using object classes. Volume of a cylinder : V = πr2h where r is the radius and h is the height of the cylinder. Try To Attempt : Difficult Level Increased 
### Ans:
``` javascript
    const volCylender = (h,r)=>{
        let vol=Math.PI*h*r*2
        return vol
      }
      let h=Number(prompt("height:?"));
      let r=Number(prompt("radius:?"));
      console.log(volCylender(h,r).toFixed(4));
```
## 6. Write a JavaScript program to sort an array of JavaScript objects.  
``` javascript
Sample Object : var library = [ { title: 'The Road Ahead', author: 'Bill Gates', libraryID: 1254 }, 
{ title: 'Walter Isaacson', author: 'Steve Jobs', libraryID: 4264 }, 
{ title: 'Mockingjay: The Final Book of The Hunger Games', author: 'Suzanne Collins', libraryID: 3245 }]; 
Expected Output: [[object Object] { author: "Walter Isaacson", libraryID: 4264, title: "Steve Jobs" }, 
[object Object] { author: "Suzanne Collins", libraryID: 3245, title: "Mockingjay: The Final Book of The Hunger Games" }, [object Object] { author: "The Road Ahead", libraryID: 1254, title: "Bill Gates" }]
```
### Ans:
``` javascript
      var library = [ { title: 'The Road Ahead', author: 'Bill Gates', libraryID: 1254 }, 
      { title: 'Walter Isaacson', author: 'Steve Jobs', libraryID: 4264 }, 
      { title: 'Mockingjay: The Final Book of The Hunger Games', author: 'Suzanne Collins', libraryID: 3245 }];

        // library.sort((a,b)=>a.libraryID.localeCompare(b.libraryID))
        library.sort((a,b)=>b.libraryID-a.libraryID)
        console.log(library);
```