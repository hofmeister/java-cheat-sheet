# Class
Purpose: Defines a new class - classes are the fundamental building blocks of a java program.

```java

class MyClass {

  private String myStringProperty; //Is null unless assigned a value
  private int myIntProperty; //Is "born" with value 0
  private Integer myIntegerProperty; //Is null unless assigned a value
  
  public MyClass() {
    this.myStringProperty = "a string value";
    this.myIntegerProperty = 1234;
    this.myIntProperty = 4321;
  }
  
  aMethodOnClass(String myStringArgument) {
    this.myStringProperty = myStringArgument;
  }
  
}

```

# Bootstrap / Main Class
Purpose: Start a java program

```java

class AnyNameYouWant {
  public static void main(String[] args) {
      //Initialise classes here
      MyClass myInstance = new MyClass();
      
      myInstance.aMethodOnClass("test");
      
      System.out.println("Output this");
  }
}

```

# If / Else
Purpose: Only execute certain code if a specific condition is true


```java

if (myIntVariable > 0) {
  System.out.println("myIntVariable is bigger than 0!"); 
} else {
  System.out.println("myIntVariable is lower than or equal to 0!");
}

```

# Foreach loop
Purpose: Iterate through a list or array to be able to access and perform something on each contained element

```java
ArrayList<String> myArrayList = new myArrayList<String>();
String[] myStringArray = new String[10];
//Imagine we add some values here...

for (String eachItemInList : myArrayList) {
  System.out.println("Print this item from the list:"); 
  System.out.println(eachItemInList); 
}

```


# For loop
Purpose: Count something from A to B and perform some action for each iteration

```java
ArrayList<String> myArrayList = new myArrayList<String>();
//Imagine we add some values here...

for (int index = 0; index < myArrayList.size(); index++) {
  System.out.println("The index for this item in the list is: "); 
  System.out.println(String.valueOf(index)); 
  System.out.println("The value for this item in the list is: "); 
  System.out.println(myArrayList.get(index)); 
}

```

