# Solid Principle
## S=> Single responsibility 
 class marker{name, color year ,price}<br />
 class invoice{<br />
    public int calculatePrice(){}<br />
    public void PrintInvoice(){}<br />
    public void saveToDB(){}<br /> 
 }
 <br />
 this class have 3 reason to change the call which is not good every call have only one reason to change the class or one class should have only one responsibility
## O=> Open/close principle 
 Open for extension close for modification<br />

## L=Liskov Substation principle:
if class B is subtype of a class A then we should be able to replace the object of A with B without breaking the behavior of the program<br />
subclass extend the capability of parent should not narrow it down.<br />

example:if we are defining a class for bike which have function turnOnEngine and accelerate, then we should no extend it for bicycle because bicycle doesn't have engine

## Interface segmented Principle:
interface should be such, that client should not implement unnecessary function they do not need.
example: hotel waiter 

like if we implement interface for waiter class then waiter class should not have to implement unnecessary functions

## D=> Dependency Inversion Principle
class should depend on interface rather then concrete class<br />
a high level class should not depend on low level class
