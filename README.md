Download Link: https://assignmentchef.com/product/solved-cmsc203-assignment-4-property-management
<br>
A property management company manages individual properties they will build to rent, and charges them a management fee as the percentages of the monthly rental amount. The properties cannot overlap each other, and each property must be within the limits of the management company’s plot.  Write an application that lets the user create a management company and add the properties managed by the company to its list. Assume the maximum number of properties handled by the company is 5.

<table width="100%">

 <tbody>

  <tr>

   <td><strong>Concepts tested by this assignment</strong></td>

  </tr>

 </tbody>

</table>




<ul>

 <li>Aggregation</li>

 <li>Passing object to method</li>

 <li>Array Structure</li>

 <li>Objects as elements of the Array</li>

 <li>Processing array elements</li>

 <li>Copy Constructor</li>

 <li>Junit tes</li>

</ul>

<table width="100%">

 <tbody>

  <tr>

   <td><strong>Classes</strong></td>

  </tr>

 </tbody>

</table>




<strong>Data Element class </strong><strong>– Property.java</strong>

The class <em>Property</em> will contain:

<ol>

 <li>Instance variables for property name, city, rental amount, owner, and plot. Refer to JavaDoc for the data types of each instance variable.</li>

 <li>toString method to represent a Property object.</li>

 <li>Constructors (a copy constructor and parameterized constructor) and getter and setter methods. One parameterized constructor will have parameters for property name, city, rent amount, owner, x and y location of the upper left corner of the property’s plot, the plot’s width and its depth. A second constructor will only have parameters for name, city, rental amount, and owner, and will generate a default x, y, width, and depth.</li>

</ol>

<strong> </strong>

<strong>Data Element class </strong><strong>– Plot.java</strong>

The class <em>Plot </em>will contain:

<ol>

 <li>Instance variables to represent the x and y coordinates of the upper left corner of the location, and depth and width to represent the vertical and horizontal extents of the plot.</li>

 <li>A toString method to represent a Plot object</li>

 <li>Constructors (a no-arg constructor, a copy constructor and a parameterized constructor)</li>

 <li>A method named <em>overlaps</em> that takes a Plot instance and determines if it is overlapped by the current plot.</li>

 <li>A method named <em>encompasses</em> that takes a Plot instance and determines if the current plot contains it. Note that the determination should be inclusive, in other words, if an edge lies on the edge of the current plot, this is acceptable.</li>

</ol>

<strong>Data Structure</strong> – An Array of Property objects to hold the properties that the management company handles.

<strong> </strong>

<strong>Data Manager class – </strong><strong>ManagementCompany.java</strong>

This class should not have any output functionality (e.g., no GUI-related or printing related functionality), but should take input, operate on the data structure, and return values or set variables that may be accessed with getters.

The class <em>ManagementCompany</em> will contain the following methods in addition to get and set methods. It will contain instance variables of name, tax Id, management fee, MAX_PROPERTY (a constant set to 5) and an array named properties of Property objects of size MAX_PROPERTY, as well as two constants MGMT_WIDTH and MGMT_DEPTH, both set to 10;

<ol>

 <li>Constructor <strong>managementCompany </strong>– pass in arguments for the name of the management company, tax Id and management Fee, along with the X, Y, width, and depth of the overall plot that will be subdivided into plots for each property. A <em>ManagementCompany</em> object will be created.</li>

 <li>Constructor <strong>managementCompany </strong>– pass in arguments for the name of the management company, tax Id and management Fee to create a <em>ManagementCompany</em> A default plot will be created with programmer-determined values into which to subdivide the plots for each property.</li>

 <li>Method <strong>addProperty (3 versions) </strong>–

  <ol>

   <li>Pass in a parameter of type <em>Property</em> object (calls <em>Property</em> copy constructor). It will add the copy of the <em>Property</em> object to the <em>properties</em></li>

   <li>Pass in four parameters of types:

    <ol>

     <li>String propertyName,</li>

     <li>String city,</li>

    </ol></li>

  </ol></li>

</ol>

<ul>

 <li>double rent, and</li>

</ul>

<ol>

 <li>String ownerName.</li>

</ol>

Calls <em>Property</em> 4-arg constructor.

<ol>

 <li>Pass in eight parameters of types:

  <ol>

   <li>String propertyName,</li>

   <li>String city,</li>

  </ol></li>

</ol>

<ul>

 <li>double rent,</li>

</ul>

<ol>

 <li>String ownerName,</li>

 <li>int x,</li>

 <li>int y,</li>

</ol>

<ul>

 <li>int width, and</li>

</ul>

int depth. Calls <em>Property</em> 8-arg constructor.

<ol>

 <li></li>

</ol>

addProperty methods will return the index of the array where the property is added.  If there is a general problem adding the property (other than the next three) this method will return -1; if the property is null returns -2; if the array is full returns -3; if the plot for the property is not encompassed by the management company plot or if the plot for the property overlaps any other property’s plot returns -4.

<ol start="4">

 <li>Method<strong> totalRent</strong>– Returns the total rent of the properties in the <em>properties</em></li>

 <li>Method <strong>maxRentProp</strong>-returns the String representation of the property within the <em>properties</em> array that has the highest fee amount. For simplicity assume that each “Property” object’s fee amount is different.</li>

 <li>Method <strong>maxPropertyIndex</strong>– returns the index of the property within the <em>properties</em> array that has the highest fee amount. This method will be private.</li>

 <li>Method <strong>displayPropertyAtIndex</strong>– pass in the index of the Property object in the <em>properties</em> array and return the string representation of the property. This method will be private.</li>

</ol>




<strong>You may need additional methods to include in this class. </strong><strong>Follow the Javadoc files provided.</strong>




<strong>Driver class </strong><strong>– (provided)</strong>

The provided PropertyMgmDriverNoGui.java is a class that allows you to test the methods of ManagementCompany.java

<strong> </strong>

<strong>GUI Driver class </strong><strong>– (provided)</strong>

<ul>

 <li>A Graphical User Interface (GUI) is provided. Be sure that the GUI will compile and run with your methods. The GUI will not compile if your methods in ManagementCompany.java are not exactly in the format specified.</li>

 <li>Do not modify the GUI.</li>

</ul>




<strong>JUnit Test</strong>

<ul>

 <li>Run the JUnit test file (provided). Ensure that the JUnit tests all succeed.</li>

 <li>Do not modify the JUnit tests.</li>

 <li>Implement your tests in ManagementCompanyTestSTUDENT. These tests should parallel the public Junit tests.</li>

</ul>




<table width="100%">

 <tbody>

  <tr>

   <td><strong>Assignment Details</strong></td>

  </tr>

 </tbody>

</table>




Write a Data Element Class named Property that has fields to hold the property name, the city where the property is located, the rent amount, the owner’s name, and the Plot to be occupied by the property, along with getters and setters to access and set these fields. Write a parameterized constructor (i.e., takes values for the fields as parameters) and a copy constructor (takes a Property object as the parameter).  Follow the Javadoc file provided.

Write a Data Element Class named Plot that has fields specifying the X and Y location of the upper left corner of each Plot and a depth and width of each Plot.  Notice that the X,Y location is at the upper left, not as in normal Cartesian coordinates, due to the grid system adopted by computer monitors.

A driver class is provided that creates rental properties to test the property manager.  A Graphical User Interface is provided using JavaFX which duplicates this driver’s functionality.  You are not required to read in any data, but the GUI will allow you to enter the property management company and each property by hand. A directory of images is provided.  <strong><u>Be sure to place the “images” directory (provided) inside the “src” directory in Eclipse.</u></strong>




<h2>Operation</h2>

When driver-driven application starts, a driver class (provided) creates a management company, creates rental properties, adds them to the property manager, and prints information about the properties using the property manager’s methods.

When the GUI-driven application starts (provided), a window is created as in the following screen shots which allows the user to enter applicable data and display the resulting property.  The driver and the GUI will both use the same classes and methods for their operation.

The JUnit test class also tests the same classes as the driver and the GUI.

<table width="100%">

 <tbody>

  <tr>

   <td><strong>Examples</strong></td>

  </tr>

 </tbody>

</table>




<strong><em>Expected output from running PropertyMgm</em></strong><strong><em>DriverNoGui.java</em></strong>

<strong><em>Expected output from running with GUI:</em></strong>

<strong><em> </em></strong>

<strong><em>  PropertyMgm</em></strong><strong><em>Gui.java at startup                                                                             </em></strong>




<strong><em>Add Management Co Info (Note Mgmt Co Plot)</em></strong>

<strong><em>Add property information  – the Plot outline</em></strong><strong><em>                                                    </em></strong>

<strong><em>Add property information  – successful addition</em></strong>

<strong><em>Add property information  – unsuccessful: overlaps</em></strong>




<strong><em>Add property information  – unsuccessful: Mgmt Co Plot does not encompass Property Plot</em></strong>

<strong><em>   Note: red rectangle’s width extends to right of window.</em></strong>




<strong><em>Add property information  – unsuccessful: too many properties</em></strong>

<strong><em> </em></strong>

<strong><em> </em></strong>

<strong><em> </em></strong>

<strong><em>Result of “Max Rent” button                                 Result of “Total Rent” button</em></strong>










<strong><em>Result of “List of Properties” button</em></strong>

<strong><em> </em></strong>




<table width="100%">

 <tbody>

  <tr>

   <td><strong>Deliverables</strong></td>

  </tr>

 </tbody>

</table>

<strong><u>Deliverables / Submissions</u></strong><strong>: </strong>




<strong><u>Week 1</u></strong><strong>:</strong> Design

<ul>

 <li>Turn in a UML diagram that includes box that contains pseudo-code for each of the methods specified in ManagementCompany.java. Your pseudo-code should be part-way between English and java.  There is no need to spell out all the details of variable declaration, etc., but by the same token, the pseudo-code needs to have enough detail that a competent Java programmer could implement it.</li>

</ul>




<strong><u>Week 2</u></strong><strong>:</strong> Submit two compressed files containing the follow (see below):

<strong><u>Deliverable format</u>:</strong> The deliverables will be packaged as follows. Two compressed files in the following formats:

LastNameFirstName_Assignment4.zip (a compressed file containing the following)

<ul>

 <li>UML Diagram</li>

 <li>Learning Experience</li>

 <li>Anything else required by the rubric</li>

 <li>doc (a directory) containing your javadoc files</li>

 <li><u>src</u> (a directory) <em>contains your (.java) files</em>

  <ul>

   <li>java (example)</li>

   <li>java (example)</li>

   <li>java (example)</li>

  </ul></li>

</ul>

LastNameFirstName_Assignment4_<strong>Moss</strong>.zip (a compressed file containing only .java files)

<em>NO FOLDERS!!</em>

File1.java (example)

File2.java (example)

<strong> </strong>