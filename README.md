# CS111C-W02-Generics
Generics 

Week02SourceCode.zip: 
  Box.java
  BoxR.java
  BoxTester.java
  NameInput.java
  NumericInput.java
  Student.java 

Trio LabA.zip: 
  Trio.java
  TrioTester.java

Table of Contents:
  1 Generics
    1.1 Generics in Java's Classes
    1.2 Using Generics in Your Own Classes
    1.3 Some Generics Rules
  
Youtube Video: 
https://www.youtube.com/playlist?list=PL5igFWijWBo2tS3m_f57CEv1b14-_rkeX
  
Lecture Notes: 
https://docs.google.com/document/d/1zVmbITmWMZtj4wS-KX-13-lv4sxG7sV3KahooXj21MA/edit?usp=sharing
  
  
Lab A: Generics: 

Create a Java class using generics: Trio.

• Objects of this class hold three unordered items of the same type. 

• A Trio object is unordered.
  
  • For example, the Trio (3, 4, 5) is considered the same as the Trio (4, 5, 3) and the Trio ("hi", "bye",       "hello") is considered the same as the Trio ("hello", "hi", "bye").
  
  • The order doesn't matter. (This is like a set in mathematics.)

• Use generics to ensure that the three objects are of the same type. 
  
  • For example, a Trio can hold three Integers or it could hold three Strings or it could hold three        Students, etc.
 
 • A Trio could not, however, hold two Integers and a String.

• Write this class using generics. Here is the class header: public class Trio<T>

Requirements:

Your class must compile (10 points) and have the following:

• (10 points) instance data for the three items

• (10 points) a constructor to create the object by sending three items as parameters

• (10 points) getters and setters for each item in the trio

• (10 points) a toString method that returns a text representation of the trio 

• (15 points) a contains method that returns whether or not the trio contains an item sent in as a parameter

• (15 points) a method called sameItems that returns true if the three items are the same as each other, meaning they are equal to each other (not aliases, but equal- logically equivalent), and false otherwise

  • For example, invoking sameItems on the Trio (3, 3, 3) will return true. Invoking sameItems on the Trio (3, 4, 4) will return false.

• (20 points) an equals method that overrides the equals method of the Object class.

  • The method returns true if the current Trio holds the same three items in any order as the Trio sent as a parameter and false otherwise.

  • Note that the equals method should not alter either the parameter or the current Trio object.

Extra Credit (20 points):

• implement the Comparable interface

• order Trio objects by the smallest item in each Trio

  • For example, (3, 1, 4) is less than (2, 6, 4) because the smallest item in the first Trio (1) is less than the smallest item in the second Trio (2)

• Hint: make a private helper method to find the smallest item in any Trio.

• Note that there are other ways you could reasonable compare Trio objects- but this is the way you are required to do it for the extra credit.

• Note that the compareTo method should not alter either the parameter or the current Trio object.

• To compile, change the class header and method header to the following.

  • Essentially, these changes mean that you are requiring the data type T to implement Comparable as well.

  • That matters because it means you can invoke compareTo on the items in the Trio!

  • The "?" is called a wildcard and is related to bounds in generics. This is not information you are responsible for in our course. For now, you can just use it.
   
   public class Trio<T extends Comparable<? super T>> implements Comparable<Trio <T>>

   public int compareTo(Trio<T> otherTrio) {

Testing and Submission:

I have provided a driver program that you can use to test your class. You might want to add additional code, but you can use this driver program as a starting point for testing.

Review the Assignment Submission Guidelines. Most importantly, make sure your code compiles- code that does not compile will receive a zero.

If submitting as a group, submit one assignment only through one group member's Insight account. Put the names of all group members in Java comments at the top of each Java file.
