# Computer Science II
## Lab 1.0 - Introduction

An introduction to the Java programming language and tools 
including Eclipse, Eclipse Git client, etc. 

Followed by an introduction to using conditionals and loops in the Java programming language.


This is a lab used in Computer Science II (CSCE 156, CSCE 156H) 
in the [Department of Computer Science & Engineering](https://computing.unl.edu) 
at the [University of Nebraska-Lincoln](https://unl.edu).

Chris Bourke wrote this lab, revamped and combined with Lab 2 by Sarah Roscoe for Summer 2021 - 2024. 

## Overview

### Prior to Lab

In each lab there may be pre-lab activities that you are *required* 
to complete prior to attending lab.  Failure to do so may mean that 
you will not be given full credit for the lab.  

### Resources
Prior to lab you should read/review the following resources.
* `if-else tutorial`:
http://download.oracle.com/javase/tutorial/java/nutsandbolts/if.html
* `for` loop tutorial:
http://download.oracle.com/javase/tutorial/java/nutsandbolts/for.html
* `while` loop tutorial:
http://download.oracle.com/javase/tutorial/java/nutsandbolts/while.html


### Lab Objectives & Topics
Following the lab, you should be able to:
* Clone projects from GitHub using Eclipse
* Open, compile, and execute a given Java program in Eclipse.
* Write a simple program in the Eclipse IDE, compile, and 
  execute that program.
* Use `if-else` statements to control the logical flow of the
  program.
* Use `for` and `while` loops to implement repetition statements in a
  program.
* Write complex programs that require conditional logical statements
  and loops.



### Peer Programming Pair-Up
You will work on this lab with a partner One of you should submit your code to the corresponding Handin assignment, or both of you should submit identical code. Handin link: https://cse-apps.unl.edu/handin





You will work in a *pair programming* setup.  At the start of
each lab, you may be randomly paired up with another student by
a lab instructor.  One of you will be designated the *driver* 
and the other the *navigator*.  

The navigator will be responsible for reading the instructions 
and telling the driver what is to be done.  The driver will be 
in charge of the keyboard and workstation (**on Zoom, this means the driver shares their screen**).  Both driver and 
navigator are responsible for suggesting fixes and solutions 
*together*.  Neither the navigator nor the driver is "in charge."  
Beyond your immediate pairing, you are encouraged to help and 
interact and with other pairs in the lab.

Each week you should try to alternate: if you were a driver 
last week, be a navigator next, etc.  Resolve any issues (you 
were both drivers last week) within your pair.  Ask the lab 
instructor to resolve issues only when you cannot come to a 
consensus.  

Because of the peer programming setup of labs, it is absolutely 
essential that you complete any pre-lab activities and familiarize
yourself with the handouts prior to coming to lab.  Failure to do
so will negatively impact your ability to collaborate and work with 
others which may mean that you will not be able to complete the
lab.  

## 1. Getting Started

### 1.1. Setup


#### 1.1.1. Install Java Developer Kit  

You may already have "Java" installed on your computer, but this
is most likely the Java Virtual Machine (JVM) that allows you to
run Java programs.  To actually develop Java programs you need a
Java Development Kit (JDK).  There are several alternative JDKs
and you are welcome to explore them, but for this course, we are
recommending Oracle's JDK available for download at the following
URL.  Follow the instructions for downloading and installing.

https://www.oracle.com/java/technologies/javase-downloads.html

#### 1.1.2. Install Eclipse

Eclipse is an Integrated Development Environment (IDE) for 
Java development.  There are many other popular IDEs available 
and you are welcome (and encouraged) to try them out and use 
them if you wish.  However, for this course, most instructions
will assume the use of Eclipse and it is the IDE we will 
primarily use for this course.  You can download and install
Eclipse at the following URL.

https://www.eclipse.org/


## 2. Checking Out Code From Github Using Eclipse

Each lab will have some starter code and other *artifacts* 
(data files, scripts, etc.) that will be provided for to you.  
The code is hosted on Github (https://github.com) and you must 
*clone* your own copy to work with it.  You will not need to 
know the details of using git nor be a registered Github user 
to get access to the code necessary for your labs.  However, 
you are *highly encouraged* to learn this essential tool.  
You may find it very useful to keep track of your own code 
and to share code if you work in pairs or groups.  

To check out the code for this lab, do the following.  You may 
want to reference this step-by-step process in subsequent labs.

1. First we need a Git *perspective* (a context in the Eclipse 
User Interface that will allow us to work with Git).  To open 
the Git perspective, click on the "Open Perspective" tab in the 
upper right:  
<p align="center">
<img src="images/eclipseOpenPerspectiveMarkUp.png" alt="Open Perspective" width="50%"/>
</p>  

2. Select "Git" from the menu and click `OK`  

3. Click the "Clone a Git repository" in the Git Repositories 
navigation menu:
<p align="center">
<img src="images/eclipseGitRepoMarkUp.png" alt="Clone a Git repository" width="50%"/>
</p>  

4. Copy/paste or type into the URI field, the URL: 
   https://github.com/kangilpark/CSCE156-Lab01/ 
<p align="center">
<img src="images/eclipseCloneDialogAMarkUp.png" alt="URL" width="50%"/>
</p>

5. Click `Next`; once Eclipse has grabbed the project, the 
"master" branch should be selected (checkbox); click `Next` 
again.  
<p align="center">
<img src="images/eclipseCloneDialogBMarkUp.png" alt="URL" width="50%"/>
</p>

6. Select the directory where you want your project to be saved.  
Caution: the default option may not correspond to your default 
workspace.  You will want to change it to your workspace.  Mark 
the "Import all existing projects after clone finishes" checkbox 
option or you will need to manually import the cloned project 
into Eclipse.  
<p align="center">
<img src="images/eclipseCloneDialogCMarkUp.png" alt="URL" width="50%"/>
</p>

7. Switch back to your Java or JavaEE perspective and you can 
see your cloned project.  

# Java

All students should complete this Java section, even if you are 
already familiar with Java, in order to familiarize yourself 
with how labs will work for the semester.  

## 3.1 Running & Editing Programs

### 3.1.1 Running a Program

We will now familiarize you with Eclipse by editing an existing
project's code.

1. Expand the `src` directory.  Under this we have a *package* named 
`unl.cse`.  Java classes are organized in a hierarchy of packages.
Packages correspond to actual directories in your file system.  

2. Expand the package and you'll find several *classes*.	All Java code 
must be contained in a class.  This is in contrast to other languages 
that may allow global variables or allow functions to exist without an 
object or a class.

3. Double click on the `StatisticsDemo` class to open it in the Eclipse 
editor.  This class contains a main method, `public static void main(String args[])`
In Java, classes are executable only if a main method is defined.  
Classes without a `main` method can be used by other classes, but 
they cannot be run by themselves as an entry point for the Java 
Virtual Machine (JVM).

4. Click on the "play" button as highlighted (click "Proceed" if prompted):
<p align="center">
<img src="images/eclipseScreen.png" alt="Eclipse Screen" width="50%"/>
</p>
5. The output for this program will appear in the "console" tab at the bottom.
6. Click on the console tab and enter the input as specified.

### 3.1.2 Completing the Statistics Program

Though the program runs, it does not output correct answers.  You 
will need to modify these classes to complete the program.

1. Implement the `getMax()` method in the `Statistics` class.  Use the 
`getMin()`	method for directions on syntax.
2. Implement the `getSum()` method in the `Statistics` class.  Use the 
other methods for direction on syntax.
3. Rerun the program to verify that it now works.

### 3.1.3 Modifying the Statistics Program

The program you've completed is interactive in that it prompts the 
user for input.  You will now change the program to instead use *command 
line arguments* to read in the list of numbers directly from the command 
line.

Command line arguments are available to your main method through 
the `args` array of Strings.  The size of this array 
can be obtained by using `args.length` which is an
integer.  Modify your code to iterate through this array and convert 
the arguments to integers using the following snippet of code:

```java
for(int i=0; i<args.length; i++) {
  array[i] = Integer.parseInt(args[i]);
}
```

The *command line* may not be apparent as you are using an IDE.  
However, it is still available to you.  Instead of clicking the "Play" 
button to run your program, click the down arrow right next to it.  
Then select "Run Configurations".  This brings up a dialog box with 
which you can run custom configurations.  Click the Arguments tab and 
enter a space-delimited list of numbers under "Program Arguments"
and click "Run".

## 4. IDE Orientation

In the next activities you'll get more familiar with using Eclipse and the
convenient functionality IDEs provide.  

### 4.1 Using External Libraries

No man is an island.  Good code depends on selecting and (re)using 
standard libraries whenever possible so that you are not continually 
reinventing the wheel.  This activity will familiarize you with how 
to import and use an external Java library.  Java libraries are 
usually packaged into JAR *J*ava *AR*chive files which contain a 
collection of compiled class files and other resources necessary 
to use the library.

1. You'll notice that there are compilation errors in the `Birthday.java` 
file.  This is because this class uses other classes that are not 
available in the standard Java Development Kit (JDK).  It instead 
uses classes from the Joda-Time library; a library of useful classes 
and utilities for dealing with dates, times, intervals, durations, etc.
2. The JAR file, `joda-time-2.0.jar` has been included in the project 
in the `lib` folder.  External libraries are usually kept in a hierarchy 
of folders like this (you can create your own folders by right-clicking 
the project and selecting "New" then "Folder")
3. Right-click the JAR file and select "Build Path" then "Add to Build 
Path."  The library is now included in your project and the compiler 
errors should go away.

### 4.2 Cleaning Up

Though the syntax errors should now be resolved, the code isn't pretty
making it difficult to read and understand.  Eclipse provides a built-in
code formatter functionality.  Typically if you write good code to begin
with it will automatically provide consistent indentation and other 
stylistic features.  It is best practice to get in the habit of writing 
good, clean code automatically.  However, if you need to clean up a file 
in one shot you can do use the auto-formatter feature.  

* On Windows: press `control-shift-f` to reformat the code
* On Mac: press `shift-command-f` to reformat the code

Another issue with the code is that it is using `lower_underscore_casing` 
for some of its variables.  Change the variable names to the preferred 
`lowerCamelCasing` convention in Java.  You could do this manually but 
a neat trick that most IDEs provide is as follows.

1. Highlight the variable name (any instance will do)
2. Right click and select `Refactor` then `Rename`
3. Type the new variable name and hit enter and it will automatically 
be changed for all instances!  

Finally, every *non-trivial* class and method should have documentation.
In Java, it is standard to use doc-style or "javadoc" comments.  Look
at the `Statistics.java` file again to see the format for these style of comments.
Add documentation to this file to complete it.

### 4.3 Finishing The Program

Though the program should have no syntax errors, if you run it, no 
output will be displayed.  You need to complete the program as follows.

1. For the variables, name, month, date, and year, enter your own 
information (your name and your birthday)
2. Add appropriate code (using `System.out.println()`) which prints 
to the standard output a full line) a greeting similar to the following. 
`Greetings, NAME.  Today you are XX years, XX months, and XX days old.`
Of course, the placeholders should be replaced with variable values.  
In Java, variable values can be concatenated with strings using the `+` 
(plus) operator.
3. Add a conditional statement that, if today is the user's birthday 
will output `Happy Birthday`.  If it is not the user's birthday, output 
`Your friends have XX shopping days until your next birthday`
again with an appropriate variable value.


# Part 2

## 5. Conditionals & Loops

Java provides standard control structures for conditionals and
repetition. Specifically, Java provides the usual `if-else`
statements as well as `for` and `while` loops. The syntax for these
control structures should look familiar.  Some examples:

```java
if(x > 0) {
  //DO SOMETHING
} else if(x < 0) {
  //DO SOMETHING ELSE
} else {
  //OTHERWISE
}

for(int i=0; i<n; i++) {
  //DO SOMETHING
}

int i = 0;
while(i < n) {
  //DO SOMETHING
  i++;
}
```

In addition, Java provides a foreach-loop, also referred to as an
*enhanced for-loop*, for iterating over collections or elements in an 
array.  This feature is mostly for convenience.  The following example
demonstrates how to use this loop.

```java
String arr[] = new String[10];
...
for(String s : arr) {
  System.out.println(s); 
}
```

An enhanced for-loop can be used for `Set` and `List` collections.

## 6. Activities 

### 6.1 Sum of Natural Numbers

Natural numbers are the usual counting numbers; 1, 2, 3, ... In this
exercise you will write several loops to compute the sum of natural
numbers 1 thru `n` where `n` is read from the command line. You will
also write an enhanced for-loop to iterate over an array and process
data.

1.  Open the `Natural.java` source file. The code to read in `n` has been
    provided for you. An array mapping integer values 1 thru 10 to text
    values has also been created for you.

2.  Write a `for`-loop and a `while`-loop in the relevant methods to
    compute the sum of natural numbers 1 thru `n` and return the 
    result.  In the `main` method call your methods and output 
    the result.  
    
3.  Write a an enhanced for-loop to iterate over the elements of the `zeroToTen`
    array. As you iterate over the elements, concatenate each
    string, delimited by a single space to a result string and print the
    result at the end of the loop. Your result should look something
    like the following:
    
    `zero + one + two + three + four + five + six + seven + eight + nine + ten = 55`

### 6.2 Child Tax Credit

When filing for federal taxes, a credit is given to tax payers with
dependent children according to the following rules. The first dependent
child younger than 18 is worth a $1,000.00 credit. Each dependent child
younger than 18 after the first child is worth a $500 tax credit each.
You will complete a Java program to output a table of dependent
children, how much each contributes to a tax credit, and a total child
tax credit. Your table should look something like the following.

```text
Child           Amount
Tommy (14)      $1000.00
Richard (12)    $500.00
Harold (21)     $0.00
Total Credit:   $1500.00
```

1.  Open the `Child.java` and `ChildCredit.java` source files

2.  The `Child` class has already been implemented for you. Note how the 
    `Child` class is used.  Several instances of children have been created 
    and placed into a `List`.

    Similar to an array, a `List` stores elements using 0-indexing. Each one
    can be accessed using the `get` method. For example, `kids.get(i)` gets 
    the i-th kid.  You could also use an *enhanced for loop* to iterate over 
    the elements in the `List`.

3.  Implement the `produceReport` method to compute the child tax credit(s)
    and output a table similar to the one above.  Your method should return
    the grand total of the credit.  
    
    Each child is an *instance* of the `Child` class. Each instance has its own
    variables so that each child can be a different age. To get a
    particular child’s age, you can use a *getter* method. For example,
    to get the age of `tom` you can use the syntax, `tom.getAge()`

### Advanced Activity (Optional)

Use the `String.format()` method to reformat the output of the Child Tax 
Credit program to print every piece of data in its own column.


## 7. Testing, Submitting, & Grading your lab

### 7.1 Testing

Every lab will come with a collection of test files that contain 
a suite of *unit tests* using the JUnit testing framework.  Before
you submit your lab, you should run these tests locally to verify 
that your code is correct.  

1. Open the `StatisiticsTests.java` source file in the `src/test/java`
source folder.  This file contains several unit tests written using
JUnit *annotations*.  You are encouraged to explore how these tests
are written and work and to even add your own tests but otherwise, 
the file is complete.
2. Run the test suite by clicking the usual "Play" button.  A report
will be presented in a JUnit tab detailing which test cases pass and
which fail along with expected output and the actual output (for 
failed test cases).  
3. Address any issues or failing tests by debugging your code and 
rerun the test suite until all tests pass.

### 7.2 Submitting

Many of your assignments will include a programming portion that will 
require you to hand in *soft-copy* source files for graders to 
compile and evaluate.  To do this, you will use a web-based handin 
program.  After handing your file(s) in, you can then grade them by 
using the web grader.  To demonstrate, do the following.

1. Open a browser to https://cse-apps.unl.edu/handin
2. Login with your **CSE credentials**
3. Click on Lab 1.0 and hand in the following files:
  * `Natural.java`
  * `ChildCredit.java`
  * `Statistics.java`
  * `Birthday.java`
You can either click the large "handin" area and select the file or you can drag-drop the files.  You 
will be able to re-handin the same file as many times as you want up 
until the due date.

### 7.3 Grading

Now that the file has been handed in, you can "grade" yourself 
by using the webgrader

1. Open a new tab/window and point your browser 
to https://cse-linux-01.unl.edu/~c-kpark5/CSCE156/grade/ (depending on your section, this 
URL may be different).
2. Fill the form with your CSE login and password, select the 
appropriate assignment and click "Grade"
3. Observe the expected output and compare it to your output to be
sure that your program is correct.  

For labs, the grader script simply runs the provided JUnit test
suite, but it *may* run additional or modified tests.  In any case,
be sure your code compiles, runs and passes all tests in the
webgrader.  Address any issues and resubmit as many times as you 
like up to the due date.


