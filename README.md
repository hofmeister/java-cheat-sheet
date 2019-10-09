# Class
Purpose: Defines a new class - classes are the fundamental building blocks of a java program.

```java

//Define the class and give it a name. Name can be anything - in this case "MyClass"
class MyClass {

  //First define any properties you want. This defines the internal "state" of your class.
  
  private String myStringProperty; //Is null unless assigned a value
  
  private int myIntProperty; //Is "born" with value 0
  
  private Integer myIntegerProperty; //Is null unless assigned a value
  
  //The constructor is called once when you create new instances. This is where you can do initialisation 
  //of properties. The constructor can take any arguments - like any other method.
  //You can not call the constructor after construction.
  public MyClass() {
    this.myStringProperty = "a string value";
    this.myIntegerProperty = 1234;
    this.myIntProperty = 4321;
  }
  
  //A method usually performs some action on the class properties. 
  // - Changes the internal state of the class (which means it changes the values of one or more properties on the class)
  // - Returns the current state of the class (which means it returns on or more values of the properties in the class)
  // - Performs calculations or transformations - which means it takes the internal state and converts it to something else
  //   like a sum total or converts an ArrayList to an array
  public void aMethodOnClass(String myStringArgument) {
    this.myStringProperty = myStringArgument;
  }
 
}

```

# Bootstrap / Main Class
Purpose: Start a java program

```java

//Define the class and give it a name. Name can be anything - in this case "AnyNameYouWant"
public class AnyNameYouWant {

  //This static method is "special" and any class that contains this exact method is considered a "program" that
  //can be executed.
  public static void main(String[] args) {
      //Initialise class - creating what is called "an instance of the class"
      MyClass myInstance = new MyClass();
      
      //Call method on the instance - giving it the argument "test"
      myInstance.aMethodOnClass("test");
      
      System.out.println("Output this");
  }
}

```

# If / Else
Purpose: Only execute certain code if a specific condition is true

```java
if (myIntVariable > 0) { //Conditions are always either true or false
  System.out.println("myIntVariable is bigger than 0!"); 
} else { //Else is performed is the condition is false. Else is optional
  System.out.println("myIntVariable is lower than or equal to 0!");
}

```

Syntax: 

```java
if (<condition>) {
  <action if condition == true>
} else { 
  <action if condition == false>
}

```


# Foreach loop over List
Purpose: Iterate through a list to be able to access and perform something on each contained element

```java
//Create array list with values
ArrayList<String> myArrayList = new ArrayList<String>();
myArrayList.add("First value");
myArrayList.add("Second value");

//Iterate through all values in myArrayList
for (String eachItemInList : myArrayList) {
  System.out.println("Print this item from the list:"); 
  //Print out the current value in the ArrayList ("First value", "Second Value")
  System.out.println(eachItemInList); 
}

```

Syntax: 

```java
for (<valuetype> <entryVariableName> : <listVariableName>) {
  <action for every entry>
}

```

# Foreach loop over array
Purpose: Iterate through an array to be able to access and perform something on each contained element

```java
//Create empty array of size 2
String[] myArray = new String[2];
//Assign value to array index 0
myArray[0] = "First value";
//Assign value to array index 1
myArray[1] = "Second value";

//Iterate through all values in myArray
for (String eachItemInArray : myArray) {
  System.out.println("Print this item from the array:"); 
  //Print out the current value in the array ("First value", "Second Value")
  System.out.println(eachItemInArray); 
}

```
Syntax: 

```java
for (<valuetype> <entryVariableName> : <arrayVariableName>) {
  <action for every entry>
}

```

# For loop
Purpose: Count something from A to B and perform some action for each iteration

```java
//Create array list with values
ArrayList<String> myArrayList = new ArrayList<String>();
myArrayList.add("First value");
myArrayList.add("Second value");

//Count from 0 to myArrayList.size() (in this case it's 2)
for (int index = 0; index < myArrayList.size(); index++) {
  System.out.println("The index for this item in the list is: "); 
  //Print out the current index (0,1)
  System.out.println(String.valueOf(index)); 
  System.out.println("The value for this item in the list is: "); 
  //Print out the value at the current index ("First value", "Second Value")
  System.out.println(myArrayList.get(index)); 
}

```

Syntax: 

```java
for (<initial value(1)>; <condition(2)> ; <action after every iteration(4)>) {
  <action for every loop(3)>
}

```

# Example: Convert from list to array
Purpose: Convert an array list into an array

```java
//Create array list with values
ArrayList<String> myArrayList = new ArrayList<String>();
myArrayList.add("First value");
myArrayList.add("Second value");

//Create empty array of same size as array list
String[] myArray = new String[myArrayList.size()];

//Count from 0 to myArrayList.size() (in this case it's 2)
for (int index = 0; index < myArrayList.size(); index++) {
  //Copy each value at each index from myArrayList to myArray at the same index 
  myArray[index] = myArrayList.get(index);
}



```

