# Digital_Vending_Machine
Objective : Designing simulating and laying upp a Digital Controller Circuit for a Vending Machine in 45nm CMOS.

## Software Used
[Cadence Virtuoso](https://ee.usc.edu/~redekopp/ee209/virtuoso/setup/USCVLSI-VirtuosoTutorial.pdf)

## Working
In this, consumer will deposit a amount (75 cents) to dispense the product from vending machine in form of quarter, dime, cents. machine has to dispense the product as well as if any change. 
When the total amount deposited by the consumer exceeds 75 cents, this controller needs to set the signal OUT=1 to start dispensing the product. 
In order to show how much money has been placed, the controller will displays a 4-bit code C [3:0] at all times, with a value of 1111 denoting 75 cents (15 nickels). 
The machine accepts nickels, dimes, and quarters only as input. For each of the three coins, the machine includes three unique sensors. A quarter activates sensor Q, a dime activates sensor D, and a nickel activates sensor N.
A sensor sends the controller a brief high voltage pulse (logic 1) when it recognizes a coin being deposited.The 4-bit code C [3:0] should display the amount of change to be handed to the consumer when the product is dispensed (OUT=1).
A reset signal RST will quickly go high after the product and any changes have been dispersed to reset the controller to the state of C [3:0] = 0000 and OUT= 0

## Deployment
First of all make a new project and attache the  45nm technology library and draw a schematic of transistor by creating cell view. After making all the basic transistors create a symbol and launch ADE to run the simulation. 
After verifying the schematic, its the time to draw a optimized layout by adding all instances like pmos, nmos, vdd, ground. now make a Metal for connection and run the Design Rule Check (DRC) to compile the layout. 
To check the layout with schematic make sure to run LVS which extract the netlist from layout and matches with netlist extracted from original schematic. if they matches then your requirement has been fullfilled.
