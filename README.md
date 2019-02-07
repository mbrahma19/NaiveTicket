# NaiveTicket

The second Objects lab, from the BlueJ book's second chapter.

Look for the [Chapter 2 file](./doc/BlueJ-objects-first-ch2.pdf) you need in the [doc](./doc) folder.
There is 35 pages of reading and exercises in the chapter.

Work through all these exercises. You edit this file with your answers for these exercises.

### Exercise 2.1
* Create a TicketMachine object on the object bench.
* Upon viewing its methods, `getBalance`, `getPrice`, `insertMoney`, `printTicket`.
* Use `getPrice` method to view the value of the price of the tickets that was set when this object was created.
* Use `insertMoney` method to simulate inserting an amount of money into the machine.
* Use `getBalance` to check that the machine has a record of the amount inserted.
	* You can insert several separate amounts of money into the machine, just like you might insert multiple coins or notes into a real machine. Try inserting the exact amount required for a ticket. As this is a simple machine, a ticket will not be issued automatically, so once you have inserted enough money, call the `printTicket` method. A facsimile ticket should be printed in the BlueJ terminal window.

### Exercise 2.2
* What value is returned if you check the machine’s balance after it has printed a ticket?
	- The balance after a ticket is printed is 0.

### Exercise 2.3
* Experiment with inserting different amounts of money before printing tickets.
	* Do you notice anything strange about the machine’s behavior?
		- The ticket is still printing even though the balance does not meet the price
	* What happens if you insert too much money into the machine – do you receive any refund?
		- The balance increases past the price. No refund provided.
	* What happens if you do not insert enough and then try to print a ticket?
		- The ticket is still printing even though the balance does not meet the price

### Exercise 2.4
* Try to obtain a good understanding of a ticket machine’s behavior by interacting with it on the object bench before we start looking at how the `TicketMachine` class is implemented in the next section.

### Exercise 2.5
* Create another ticket machine for tickets of a different price.
	* Buy a ticket from that machine.
	* Does the printed ticket look different?
		- Majority of it is the same but the price changes

### Exercise 2.6
* Write out what you think the outer wrappers of the `Student` and `LabClass` classes might look like – do not worry about the inner part.
	- Student Wrapper<br>
	public class Student{
	}
	- LabClass Wrapper<br>
	public class LabClass{
	}

### Exercise 2.7
Does it matter whether we write<br>
`public class TicketMachine`<br>
or<br>
`class public TicketMachine`<br>
in the outer wrapper of a class?
 - Yes is does matter
 
* Edit the source of the `TicketMachine` class to make the change and then close the editor window.
	* Do you notice a change in the class diagram?
		- The class now has cross hatch across it
	* What error message do you get when you now press the compile button?
		- Produces "<identifier> expected" and "invalid method declaration; Return type required"
	* Do you think this message clearly explains what is wrong?
		- It is not clear that the error is because of the incorrect class wrapper. It seems to think that the user is trying to calling a method.

### Exercise 2.8
* Check whether or not it is possible to leave out the word `public` from the outer wrapper of the `TicketMachine` class.
	- It is possible to leave out the 'public' from the outer wrapper

### Exercise 2.9
* From your earlier experimentation with the ticket machine objects within BlueJ you can probably remember the names of some of the methods – `printTicket`, for instance.
	* Look at the class definition in Code 2.1 and use this knowledge, along with the additional information about ordering we have given you, to try to make a list of the names of the fields, constructors, and methods in the `TicketMachine` class.
	* Hint: There is only one constructor in the class.
		- Fields
			- price
			- balance
			- total
		- Constructors
			- public TicketMachine(int ticketCost){...}
		- Methods
			- getBalance
			- getPrice
			- insertMoney
			- printTicket

### Exercise 2.10
* Do you notice any features of the constructor that make it significantly different from the other methods of the class?
	- There is no return type. It also intializes all the fields where as the others are either returning 1 single field or updating a single field.

### Exercise 2.11
* What do you think is the type of each of the following fields?

```java
private [int] count;
private [Student] representative;
private [Server] host; 
```

### Exercise 2.12
* What are the names of the following fields?

```java
private boolean [alive];
private Person [tutor];
private Game [game];
```
### Exercise 2.13

In the following field declaration from the TicketMachine class<br>

```java
private int price;
```
does it matter which order the three words appear in?
	- It does matter what order they are put in
* Edit the `TicketMachine` class to try different orderings. After each change, close the editor.
	* Does the appearance of the class diagram after each change give you a clue as to whether or not other orderings are
possible?
	- There is a crosshatch across it
	* Check by pressing the compile button to see if there is an error message.
	- It produces a "<identifier> expected"
	* Make sure that you reinstantiate the original version after your experiments!

### Exercise 2.14
* Is it always necessary to have a semicolon at the end of a field declaration?
	- Yes is it always necessary, this is what indicates that line of code is complete and it can run that.
* Once again, experiment via the editor.
* The rule you will learn here is an important one, so be sure to remember it.


### Exercise 2.15
* Write in full the declaration for a field of type `int` whose name is `status`.
	- public int status;

### Exercise 2.16
* To what class does the following constructor belong?
	- It belongs to Student
```
public Student(String name)
```

### Exercise 2.17
* How many parameters does the following constructor have and what are their types?
	- It requires 2 parameters
```
public Book(String title, double price)
```

### Exercise 2.18
* Can you guess what types some of the `Book` class’s fields might be?
	- String title
	- Double price
* Can you assume anything about the names of its fields?
	- title is the title of the book
	- double is the price of the book

Work all Exercises from 2.19 to 2.58 that are **NOT** marked *Challenge exercise*.
READ upto and INCLUDING section 2.15 of this chapter.
######################################################################################################
### Exercise 2.19
* public Pet(string petsName){ this.name = petsName;}

### Exercise 2.21
* getBalance returns the balance field
* getPrice returns the price field

### Exercise 2.22
* What is left to pay?

### Exercise 2.23
* No it does not need to be changed

### Exercise 2.24
* public int getTotal(){return total;}

### Exercise 2.25
* It returns a "Missing return statement error"

### Exercise 2.26
* getPrice returns an int; printTicket returns nothing (void)
* printTicket takes in a parameter and completes some manipulation of data, where getPrice provides a state of a variable

### Exercise 2.27
* Both do not have any returns. This is because they are performing an operation which does not need to return anything. This is confirmed as their return type is 'void'

### Exercise 2.28
* Completed in BlueJ

### Exercise 2.29
* setPrice has a return value. Constructors do not have this

### Exercise 2.30
* public void setPrice(int ticketCost){ price = ticketCost;}

### Exercise 2.31
* public void increase(int points){ score = score + points;}

### Exercise 2.32
* public void discount(int amount){ price = price - amount;}

### Exercise 2.33/34
* Completed in BlueJ

### Exercise 2.35
* The difference is prices is because they are different objects and their state's were set at different values

### Exercise 2.36
* It would not print the numerical price. It would print out the word 'price'

### Exercise 2.37
* It would print out the string "# price cents." 

### Exercise 2.38
* It would not be able to. They are using "Price" as a string and not as a variable to print the actual value

### Exercise 2.39
* It won't require the user to provide the input. Then it will also set the price to be 1000 cents automatically

### Exercise 2.40
* The method would not require any parameters and it would be considered a mutator method.
	- public void empty(){ total = 0; balance = 0;}

### Exercise 2.41
* The method is a mutator method.
	- public void setPrice(int x){ price = x;}
	
### Exercise 2.42
* The one with no parameter creates the object immediately. The one that requires a parameter needs user input

### Exercise 2.43



















