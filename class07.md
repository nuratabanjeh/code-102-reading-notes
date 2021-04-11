# class07

## domain modeling

 domain model is a visual representation of real situation objects in a domain. A domain is an area of concern. Its used to refer to the area you are dealing with.

 The Domain Model is your organized and structured knowledge of the problem. The Domain Model should represent the vocabulary and key concepts of the problem domain and it should identify the relationships among all of the entities within the scope of the domain.

 ## HTML Tables 

HTML tables allow web authors to arrange data into rows and columns.

Defining an HTML Table :

An HTML table is defined with the `<table>` tag.

Each table row is defined with the `<tr>` tag. A table header is defined with the `<th>` tag. By default, table headings are bold and centered. A table data/cell is defined with the `<td>` tag.

HTML Table - Adding a Border :

If you do not specify a border for the table, it will be displayed without borders.

A border is set using the CSS border property.


HTML Table - Collapsed Borders :
If you want the borders to collapse into one border, add the CSS border-collapse property

## Functions, Methods, and Objects”

Creating a JavaScript Object

Using the JavaScript Keyword new:

`var person = new Object();
person.firstName = "John";
person.lastName = "Doe";
person.age = 50;
person.eyeColor = "blue";`

Updating an object:

`var person = { firstName: "John", lastName: "Doe", age: 50, eyeColor: "blue" };

var x = person;
x.age = 10; // This will change both x.age and person.age
delete person lastname // this will delete the person lastname proberty`

Creatin many objects with constructor:

`function Vehicle(name, maker) {
   this.name = name;
   this.maker = maker;
}
let car1 = new Vehicle(’Fiesta’, 'Ford’);
let car2 = new Vehicle(’Santa Fe’, 'Hyundai’)
console.log(car1.name);    //Output: Fiesta
console.log(car2.name);    //Output: Santa Fe`

## Arrays are objects:

Objects are an unordered map from string keys to values, arrays are an ordered list of values (with integer keys). That's the main difference. They're both non-primitive, as they're composed of multiple values, which also implies pass-by-reference in JavaScript.

Arrays are also a kind of object, though, so you can attach extra properties to them, access their prototype and so on.

In your revised example, you're only taking advantage of the fact that an array is actually an object, i.e. you can set any property on them. You shouldn't do that. If you don't need an ordered list of values, use a plain object.

Browser object model:

The Browser Object Model (BOM) is used to interact with the browser.

The default object of browser is window means you can call all the functions of window by specifying window or directly.

Global object:

In JavaScript, there's always a global object defined. In a web browser, when scripts create global variables, they're created as members of the global object.

Strings Object:

The String object lets you work with a series of characters; it wraps Javascript's string primitive data type with a number of helper methods.

As JavaScript automatically converts between string primitives and String objects, you can call any of the helper methods of the String object on a string primitive.

Date Object:

The Date object is used to work with dates and times.

Date objects are created with new Date().

There are four ways of instantiating a date

`var d = new Date();

var d = new Date(milliseconds);

var d = new Date(dateString);

var d = new Date(year, month, day, hours, minutes, seconds, milliseconds);`

**Thank you**