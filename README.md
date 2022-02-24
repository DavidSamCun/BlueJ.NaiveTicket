# NaiveTicket

The second Objects lab, from the BlueJ book's second chapter.

First you need to FORK this repo into your account, then you need to CLONE that foreked repo, the one in your account. 
When you are finished with your code, be sure to ADD/COMMIT and PUSH your code to your repo.

Use the URL from your repo as the submission to the portal. 

Look for the [Chapter 2 file](./doc/BlueJ-objects-first-ch2.pdf) you need in the [doc](./doc) folder.
There is 35 pages of reading and exercises in the chapter.

Work through all these exercises. You edit this file with your answers for these exercises.

### Exercise 2.1    - Answered
* Create a TicketMachine object on the object bench.
*           - Done
* Upon viewing its methods, `getBalance`, `getPrice`, `insertMoney`, `printTicket`.
*           - getBalance = 0, getPrice = 500, insertMoney = 500, checked getBalance = 500, print ticket "Ticket price: 500 cents. Your Total is 500."
* Use `getPrice` method to view the value of the price of the tickets that was set when this object was created.
*           - getPrice = 500
* Use `insertMoney` method to simulate inserting an amount of money into the machine.
*           - insertMoney set to 500.
* Use `getBalance` to check that the machine has a record of the amount inserted.
    * You can insert several separate amounts of money into the machine, just like you might insert multiple coins or notes into a real machine. Try inserting the exact amount required for a ticket. As this is a simple machine, a ticket will not be issued automatically, so once you have inserted enough money, call the `printTicket` method. A facsimile ticket should be printed in the BlueJ terminal window.
            - "Ticket price: 500 cents. Your Total is 500."
### Exercise 2.2    - Answered
* What value is returned if you check the machine’s balance after it has printed a ticket?
            - getBalance is set back to 0
### Exercise 2.3    - Answered
* Experiment with inserting different amounts of money before printing tickets.
    * Do you notice anything strange about the machine’s behavior?
    *       - Result was the same, despite the amount
    * What happens if you insert too much money into the machine – do you receive any refund?
    *       - No, it takes it all and outputs the total and balance is reset to 0. "Ticket price: 500 cents. Your Total is 1000."
    * What happens if you do not insert enough and then try to print a ticket?
    *       - Ticket still prints with the balance. ex "Ticket price: 500 cents. Your Total is 5." when 5 was out. 
### Exercise 2.4    - Answered
* Try to obtain a good understanding of a ticket machine’s behavior by interacting with it on the object bench before we start looking at how the `TicketMachine` class is implemented in the next section.

### Exercise 2.5    - Answered
* Create another ticket machine for tickets of a different price.
    * Buy a ticket from that machine.
    * Does the printed ticket look different?
    *       - Does not look different
### Exercise 2.6    - Answered
* Write out what you think the outer wrappers of the `Student` and `LabClass` classes might look like – do not worry about the inner part.
*           -  public class Student {}
*           -  public class LabClass {}

### Exercise 2.7    - Answered
Does it matter whether we write<br>
`public class TicketMachine`<br>
or<br>
`class public TicketMachine`<br>
in the outer wrapper of a class?
            -  public class TicketMachine is the properway. Class public TicketMachine gives an error.

* Edit the source of the `TicketMachine` class to make the change and then close the editor window.
    * Do you notice a change in the class diagram?
    *       -  The box for TicketMachine is crossedout in red. 
    * What error message do you get when you now press the compile button?
    *       -  Error(s) found in class. 
    * Do you think this message clearly explains what is wrong?
    *   -   To someone who's never coded before, no, it only shows where it's wrong. 
    *   -   Highlighting the error area's show the following
    *       - <identifier> expected
    *       - illegal start of expression
    *       - invalid method declaration; return type required

### Exercise 2.8    - Answered
* Check whether or not it is possible to leave out the word `public` from the outer wrapper of the `TicketMachine` class.
            - It is possible. Need to re-compile both TicketMachine and TicketMachineTest.
* 
### Exercise 2.9    - Answered
* From your earlier experimentation with the ticket machine objects within BlueJ you can probably remember the names of some of the methods – `printTicket`, for instance.
    * Look at the class definition in Code 2.1 and use this knowledge, along with the additional information about ordering we have given you, to try to make a list of the names of the fields, constructors, and methods in the `TicketMachine` class.
    * Hint: There is only one constructor in the class.
            - Name the fields, constructors and methods
            - fields - price, balance, total, ticketNumber,
            - constructor - TicketMachine
            - methods - getBalance, getPrice, insertMoney, getTicketnumber, calculateTotal, incrementTicketNumber, printTicket
### Exercise 2.10   - Answered
* Do you notice any features of the constructor that make it significantly different from the other methods of the class?
            - Constructor has the same name as the class, methods have many names 
* 
### Exercise 2.11   - Answered
* What do you think is the type of each of the following fields?

```java
private int count; 
            - type int
private Student representative;
            - type Student
private Server host;
            - type Server
```

### Exercise 2.12   - Answered
* What are the names of the following fields?

```java
private boolean alive;
            - alive
private Person tutor;
            - tutor
private Game game;
            - game 
```
### Exercise 2.13   - Answered

In the following field declaration from the TicketMachine class<br>

```java
private int price;
```
does it matter which order the three words appear in?
* Edit the `TicketMachine` class to try different orderings. After each change, close the editor.
            - "int private price;" gives an identifier error
    * Does the appearance of the class diagram after each change give you a clue as to whether or not other orderings are
possible?
            - Diagram blocks are covered in red crosses, indicating there's a syntax error. Red slashes indicate it needs to be compiled. 
    * Check by pressing the compile button to see if there is an error message.
            - Errors found in class
    * Make sure that you reinstantiate the original version after your experiments!

### Exercise 2.14   - Answered
* Is it always necessary to have a semicolon at the end of a field declaration?
*           - Yes, or it won't compile
* Once again, experiment via the editor.
*           - Syntax error was discovered, making it unable to compile. 
* The rule you will learn here is an important one, so be sure to remember it.
            
*
### Exercise 2.15   - Answered
* Write in full the declaration for a field of type `int` whose name is `status`.
            - private int status;
### Exercise 2.16   - Answered
* To what class does the following constructor belong?
```
public Student(String name)
```         - class student.

### Exercise 2.17   - Answered
* How many parameters does the following constructor have and what are their types?
```
public Book(String title, double price)
```
            - Two parameters. One is type String named title, and the other is type double named price. 
### Exercise 2.18   - Answered
* Can you guess what types some of the `Book` class’s fields might be?
*           - Maybe int for page and String for the title or subject. 
* Can you assume anything about the names of its fields?
            - One of the fields the page field. Another would be title field. 
READ upto and INCLUDING section 2.15 of this chapter.
