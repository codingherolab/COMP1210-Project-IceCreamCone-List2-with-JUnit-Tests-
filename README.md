# COMP1210-Project-IceCreamCone-List2-with-JUnit-Tests-

Download Here: [COMP1210 Project: IceCreamCone List2 with JUnit Tests ](https://codingherolab.com/product/comp1210-project-icecreamcone-list2-with-junit-tests/)

For Custom/Original Work email codingprolab@gmail.com/whatsapp +1(541)423-7793

Overview: This project consists of four classes: (1) IceCreamCone is a class representing an
IceCreamCone object; (2) IceCreamConeTest class is a JUnit test class which contains one or more
test methods for each method in the IceCreamCone class; (3) IceCreamConeList2 is a class
representing an IceCreamCone list object; and (4) IceCreamConeList2Test class is a JUnit test class
which contains one or more test methods for each method in the IceCreamConeList2 class. Note that
there is no requirement for a class with a main method in this project.
Since you will be modifying classes from the previous project, I strongly recommend that you
create a new folder for this project with a copy of your IceCreamCone class and
IceCreamConeList2 class from the previous project.
You should create a jGRASP project and add your IceCreamCone class and
IceCreamConeList2 class. With this project open, your test files will be automatically added to
the project when they are created. You will be able to run all test files by clicking the JUnit run
button on the Open Projects toolbar.
• IceCreamCone.java (a modification of the IceCreamCone class from the previous project; new
requirements are underlined below)
Requirements: Create an IceCreamCone class that stores the label, radius, and height. The
radius and height must be greater than zero. The IceCreamCone class also includes methods to set
and get each of these fields, as well as methods to calculate the surface area and volume of an
IceCreamCone object, and a method to provide a String value of an IceCreamCone object (i.e., a
class instance).
Project: IceCreamCone List2 with JUnit Tests Page 2 of 8
Page 2 of 8
An ice cream cone is a cone with a hemisphere on top as depicted below with cone height h
and cone radius r, where r is also the radius of the hemisphere. The formulas are provided to
assist you in computing return values for the respective methods in the IceCreamCone class
described in this project.
radius (r)
height (h)
Cone Side Area (cA)
Hemisphere Area (hA)
Surface Area (A)
Cone Volume (cV)
Hemisphere Volume (hV)
Volume (V)
�� = � � ‘ℎ) + �)
ℎ� = 2 ��)
� = �� + ℎ�
�� = ℎ��)⁄3
ℎ� = 2��/⁄3
� = �� + ℎ�
Design: The IceCreamCone class has fields, a constructor, and methods as outlined below.
(1) Fields (three instance variables and one class variable):
Instance Variables – label of type String, radius of type double, and height of type double.
Initialize the String to “” and the double to 0 in their respective declarations. These instance
variables should be private so that they are not directly accessible from outside of the
IceCreamCone class, and these should be the only instance variables in the class.
Class Variable – count of type int should be private and static, and it should be initialized to
zero. This class variable is used to count the number of IceCreamCone objects created, and
it should be the only class variable.
(2) Constructor: Your IceCreamCone class must contain a public constructor that accepts three
parameters (see types of above) representing the label, radius, height. Instead of assigning
the parameters directly to the fields, the respective set method for each field (described
below) should be called. For example, instead of the statement label = labelIn; use
the statement setLabel(labelIn); Below are examples of how the constructor could
be used to create IceCreamCone objects. Note that although String and numeric literals are
used for the actual parameters (or arguments) in these examples, variables of the required
type could have been used instead of the literals.
The constructor should increment the class variable count each time an IceCreamCone is
constructed.
IceCreamCone ex1 = new IceCreamCone(“Ex 1″, 1, 2);
IceCreamCone ex2 = new IceCreamCone(” Ex 2 “, 12.3, 25.5);
IceCreamCone ex3 = new IceCreamCone(“Ex 3”, 123.4, 900);
Project: IceCreamCone List2 with JUnit Tests Page 3 of 8
Page 3 of 8
(3) Methods: Usually a class provides methods to access and modify each of its instance
variables (known as get and set methods) along with any other required methods. The
methods for IceCreamCone, which should each be public, are described below. See formulas
in Code and Test below.
o getLabel: Accepts no parameters and returns a String representing the label field.
o setLabel: Takes a String parameter and returns a boolean. If the string parameter is
not null, then the label field is set to the “trimmed” String and the method returns true.
Otherwise, the method returns false and the label field is not set.
o getRadius: Accepts no parameters and returns a double representing the radius field.
o setRadius: Accepts a double parameter and returns a boolean as follows. If the
double is greater than zero, sets the radius field to the double passed in and returns true.
Otherwise, the method returns false and does not set the radius field.
o getHeight: Accepts no parameters and returns a double representing the height field.
o setHeight: Accepts a double parameter and returns a boolean as follows. If the
double is greater than zero, sets the height field to the double passed in and returns true.
Otherwise, the method returns false and does not set the height field.
o surfaceArea: Accepts no parameters and returns the double value for the total
surface area calculated using formula above and the values of the radius and height fields.
See code and test below regarding the Math.tan(x) method.
o volume: Accepts no parameters and returns the double value for the volume calculated
using formula above and the values of the radius and height fields.
o toString: Returns a String containing the information about the IceCreamCone object
formatted as shown below, including decimal formatting (“#,##0.0######”) for the
double values. Newline and tab escape sequences should be used to achieve the proper
layout. In addition to the field values (or corresponding “get” methods), the following
methods should be used to compute appropriate values in the toString method:
surfaceArea() and volume(). Each line should have no trailing spaces (e.g., there
should be no spaces before a newline (\n) character). The toString value for ex1, ex2,
and ex3 respectively are shown below (the blank lines are not part of the toString
values).
IceCreamCone “Ex 1” with radius = 1.0 and height = 2.0 units has:
surface area = 13.308 square units
volume = 4.1887902 cubic units
IceCreamCone “Ex 2” with radius = 12.3 and height = 25.5 units has:
surface area = 2,044.5837657 square units
volume = 7,937.3689278 cubic units
IceCreamCone “Ex 3” with radius = 123.4 and height = 900.0 units has:
surface area = 447,847.2056927 square units
volume = 18,287,175.0307675 cubic units
Project: IceCreamCone List2 with JUnit Tests Page 4 of 8
Page 4 of 8
New method for this project
o getCount: A static method that accepts no parameters and returns an int representing
the static count field.
o resetCount: A static method that returns nothing, accepts no parameters, and sets the
static count field to zero.
o equals: An instance method that accepts a parameter of type Object and returns false if
the Object is a not an IceCreamCone; otherwise, when cast to an IceCreamCone, if it has
the same field values as the IceCreamCone upon which the method was called.
Otherwise, it returns false. Note that this equals method with parameter type Object will
be called by the JUnit Assert.assertEquals method when two IceCreamCone objects are
checked for equality.
Below is a version you are free to use.
public boolean equals(Object obj) {
if (!(obj instanceof IceCreamCone)) {
return false;
}
else {
IceCreamCone icc = (IceCreamCone) obj;
return (label.equalsIgnoreCase(icc.getLabel())
&& Math.abs(radius – icc.getRadius()) < .000001
&& Math.abs(height – icc.getHeight()) < .000001);
}
}
o hashCode(): Accepts no parameters and returns zero of type int. This method is
required by Checkstyle if the equals method above is implemented.
Code and Test: As you implement the methods in your IceCreamCone class, you should compile
it and then create test methods as described below for the IceCreamConeTest class.
• IceCreamConeTest.java
Requirements: Create an IceCreamConeTest class that contains a set of test methods to test each
of the methods in IceCreamCone.
Design: Typically, in each test method, you will need to create an instance of IceCreamCone, call
the method you are testing, and then make an assertion about the expected result and the actual
result (note that the actual result is commonly the result of invoking the method unless it has a
void return type). You can think of a test method as simply formalizing or codifying what you
have been doing in interactions to make sure a method is working correctly. That is, the sequence
of statements that you would enter in interactions to test a method should be entered into a single
test method. You should have at least one test method for each method in IceCreamCone, except
for associated getters and setters which can be tested in the same method. However, if a method
contains conditional statements (e.g., an if statement) that results in more than one distinct
outcome, you need a test method for each outcome. For example, if the method returns boolean,
Project: IceCreamCone List2 with JUnit Tests Page 5 of 8
Page 5 of 8
you should have one test method where the expected return value is false and another test method
that expects the return value to be true (also, each condition in boolean expression must be
exercised true and false). Collectively, these test methods are a set of test cases that can be
invoked with a single click to test all of the methods in your IceCreamCone class.
Code and Test: Since this is the first project requiring you to write JUnit test methods, a good
strategy would be to begin by writing test methods for those methods in IceCreamCone that you
“know” are correct. By doing this, you will be able to concentrate on the getting the test methods
correct. That is, if the test method fails, it is most likely due to a defect in the test method itself
rather the IceCreamCone method being testing. As you become more familiar with the process of
writing test methods, you will be better prepared to write the test methods for the new methods in
IceCreamCone. Be sure to call the IceCreamCone toString method in one of your test cases so
that Web-CAT will consider the toString method to be “covered” in its coverage analysis.
Remember that you can set a breakpoint in a JUnit test method and run the test file in Debug
mode. Then, when you have an instance in the Debug tab, you can unfold it to see its values or
you can open a canvas window and drag items from the Debug tab onto the canvas.
• IceCreamConeList2.java (a modification of the IceCreamConeList2 class in the previous
project; new requirements are underlined below.)
Requirements: Create an IceCreamConeList2 class that stores the name of the list, an array of
IceCreamCone objects, and the number of IceCreamCone objects in the array. It also includes
methods that return the name of the list, number of IceCreamCone objects in the
IceCreamConeList2, total surface area, total volume, average surface area, and average volume
for all IceCreamCone objects in the IceCreamConeList2. The toString method returns a String
containing the name of the list followed by each IceCreamCone in the array, and a summaryInfo
method returns summary information about the list (see below).
Design: The IceCreamConeList2 class has three fields, a constructor, and methods as outlined
below.
(1) Fields (instance variables): (1) a String representing the name of the list, (2) an array of
IceCreamCone objects, and (3) an int representing the number of IceCreamCone objects in
the IceCreamCone array. These are the only fields (or instance variables) that this class
should have.
(2) Constructor: Your IceCreamConeList2 class must contain a constructor that accepts (1) a
parameter of type String representing the name of the list, (2) a parameter of type
IceCreamCone[], representing the list of IceCreamCone objects, and (3) a parameter of
type int representing the number of IceCreamCone objects in the IceCreamCone array.
These parameters should be used to assign the fields described above (i.e., the instance
variables).
Project: IceCreamCone List2 with JUnit Tests Page 6 of 8
Page 6 of 8
(3) Methods: Methods: The methods for IceCreamConeList2 are described below.
o getName: Returns a String representing the name of the list.
o numberOfIceCreamCones: Returns an int representing the number of
IceCreamCone objects in the IceCreamConeList2. This essentially a getter for the third
field in the IceCreamConeList2 object.
o totalSurfaceArea: Returns a double representing the total surface areas for all
IceCreamCone objects in the list. If there are zero IceCreamCone objects in the list, zero
should be returned.
o totalVolume: Returns a double representing the total volumes for all IceCreamCone
objects in the list. If there are zero IceCreamCone objects in the list, zero should be
returned.
o averageSurfaceArea: Returns a double representing the average surface area for
all IceCreamCone objects in the list. If there are zero IceCreamCone objects in the list,
zero should be returned.
o averageVolume: Returns a double representing the average volume for all
IceCreamCone objects in the list. If there are zero IceCreamCone objects in the list, zero
should be returned.
o toString: Returns a String (does not begin with \n) containing the name of the list
followed by each IceCreamCone in the array. In the process of creating the return result,
this toString() method should include a while loop that calls the toString() method for
each IceCreamCone object in the list (adding a \n before and after each). Be sure to
include appropriate newline escape sequences. For an example, see lines 2 through 16 in
the output from IceCreamConeListApp for the IceCreamCone_data_1.txt input file.
[Note that the toString result should not include the summary items in lines 18 through
24 of the example. These lines represent the return value of the summaryInfo method.]
o summaryInfo: Returns a String (does not begin with \n) containing the name of the
list (which can change depending of the value read from the file) followed by various
summary items: number of IceCreamCone objects, total surface area, total volume,
average surface area, and average volume. Use “#,##0.0##” as the pattern to format the
double values. For an example, see lines 18 through 24 in the output from
IceCreamConeList2App for the IceCreamCone_data_1.txt input file. The second
example shows the output from IceCreamConeList2App for the
IceCreamCone_data_0.txt input file which contains a list name but no IceCreamCone
data.
o getList: Returns the array of IceCreamCone objects (the second field above).
o readFile: Takes a String parameter representing the file name, reads in the file,
storing the list name and creating an array of IceCreamCone objects, uses the list name,
the array, and number of IceCreamCone objects in the array to create an
IceCreamConeList2 object, and then returns the IceCreamConeList2 object.
o addIceCreamCone: Returns nothing but takes three parameters (label, radius, and
height), creates a new IceCreamCone object, and adds it to the IceCreamConeList2
object. Finally, the number of IceCreamCone objects field must be incremented.
o findIceCreamCone: Takes a label of an IceCreamCone as the String parameter and
returns the corresponding IceCreamCone object if found in the IceCreamConeList2
object; otherwise returns null. Case should be ignored when attempting to match the
label.
Project: IceCreamCone List2 with JUnit Tests Page 7 of 8
Page 7 of 8
o deleteIceCreamCone: Takes a String as a parameter that represents the label of the
IceCreamCone and returns the IceCreamCone if it is found in the IceCreamConeList2
object and deleted; otherwise returns null. Case should be ignored when attempting to
match the label; consider calling/using findIceCreamCone in this method. When an
element is deleted from an array, elements to the right of the deleted element must be
shifted to the left. After shifting the items to the left, the last IceCreamCone element in
the array should be set to null. Finally, the number of elements field must be
decremented.
o editIceCreamCone: Takes three parameters (label, radius, and height), uses the
label to find the corresponding the IceCreamCone object. If found, sets the radius and
height to the values passed in as parameters, and returns true. If not found, returns false.
This method should not change the label.
New methods for this project
o findIceCreamConeWithShortestRadius: Returns the IceCreamCone with the
shortest radius; if the list contains no IceCreamCone objects, returns null.
o findIceCreamConeWithLongestRadius: Returns the IceCreamCone with the
longest radius; if the list contains no IceCreamCone objects, returns null.
o findIceCreamConeWithSmallestVolume: Returns the IceCreamCone with the
smallest volume; if the list contains no IceCreamCone objects, returns null.
o findIceCreamConeWithLargestVolume: Returns the IceCreamCone with the
largest volume; if the list contains no IceCreamCone objects, returns null.
Code and Test: Remember to import java.util.Scanner, java.io.File, java.io.IOException. These
classes will be needed in the readFile method which will require a throws clause for IOException.
Some of the methods above require that you use a loop to go through the objects in the array.
You may want to implement the class below in parallel with this one to facilitate testing. That is,
after implementing one to the methods above, you can implement the corresponding test method
in the test file described below.
• IceCreamConeList2Test.java
Requirements: Create an IceCreamConeList2Test class that contains a set of test methods to test
each of the methods in IceCreamConeList2.
Design: Typically, in each test method, you will need to create an instance of
IceCreamConeList2, call the method you are testing, and then make an assertion about the
expected result and the actual result (note that the actual result is usually the result of invoking
the method unless it has a void return type). You can think of a test method as simply
formalizing or codifying what you have been doing in interactions to make sure a method is
working correctly. That is, the sequence of statements that you would enter in interactions to test
a method should be entered into a single test method. You should have at least one test method
for each method in IceCreamConeList2. However, if a method contains conditional statements
(e.g., an if statement) that results in more than one distinct outcome, you need a test method for
Project: IceCreamCone List2 with JUnit Tests Page 8 of 8
Page 8 of 8
each outcome. For example, if the method returns boolean, you should have one test method
where the expected return value is false and another test method that expects the return value to
be true. Collectively, these test methods are a set of test cases that can be invoked with a single
click to test all of the methods in your IceCreamConeList2 class.
Code and Test: Since this is the first project requiring you to write JUnit test methods, a good
strategy would be to begin by writing test methods for those methods in IceCreamConeList2 that
you “know” are correct. By doing this, you will be able to concentrate on the getting the test
methods correct. That is, if the test method fails, it is most likely due to a defect in the test
method itself rather the IceCreamConeList2 method being testing. As you become more familiar
with the process of writing test methods, you will be better prepared to write the test methods for
the new methods in IceCreamConeList2. Be sure to call the IceCreamConeList2 toString method
in one of your test cases so that Web-CAT will consider the toString method to be “covered” in
its coverage analysis. Remember that you can set a breakpoint in a JUnit test method and run the
test file in Debug mode. Then, when you have an instance in the Debug tab, you can unfold it to
see its values or you can open a canvas window and drag items from the Debug tab onto the
canvas.
Important: When comparing two arrays for equality in JUnit, be sure to use
Assert.assertArrayEquals rather than Assert.assertEquals. Assert.assertArrayEquals will return
true only if the two arrays are the same length and the elements are equal based on an element by
element comparison using the appropriate equals method.
Web-CAT
Assignment Part A – submit: IceCreamCone.java, IceCreamConeTest.java
Assignment Part B – submit: IceCreamCone.java, IceCreamConeTest.java, IceCreamConeList2.java,
and IceCreamConeList2Test.java.
Note that data files IceCreamCone_data_1.txt and IceCreamCone_data_0.txt are available in Web-CAT
for you to use in your test methods. If you want to use your own data files, they should have a .txt
extension, and they should be included with submission to Web-CAT (i.e., just add the .txt data file to
your jGRASP project in the Source Files category).
Web-CAT will use the results of your test methods and their level of coverage of your source files as
well as the results of our reference correctness tests to determine your grade.
