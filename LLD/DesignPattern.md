# Design patter
Solution to commonly occurring  problem in software development

##Gang of four//1995
Design Patterns: Elements of Reusable Object-Oriented Software

## categorization of design pattern
* Creational design patter <br/>
Singleton pattern, Factory patter,Builder patter

* Structural design Patter <br />
Proxy pattern,Adopter patter

* behavioral design patter <br />
Observer patter,State pattern,Iterator pattern


# Strategy design Pattern
is a relationship-inheritance =|>
passenger vehicle is a vehicle<br /> 
has a relationship =><br/>
### Problem: 
when multiple child of a class have same type of method by that same method is not used by other child on same level ex: in a vehicle class if its five child have a types of mechanism for breaking system and another have different type of mechanism
### Solution: implement it using interfaces
* create a break interface
* create classes for all types of break by implementing the interface
* created a variable in main class with the interface name(loosely coupled) and it can be assigned by child classes 

# Observer design Pattern
### Problem: 
* observable: inform all observer when its state change 
* observe
### solution:
* observable interface:<br />
List< observerInterface > <br />
add(observerInterface,obj)<br />
remove(observerInterface obj)<br />
notify()<br />
setData()
* observer interface:update();

## Example: weather station:
* update current temperature(observable)
* observer
1. TV display
2. Mobile Display

## implementation
WSObservable interface{<br />
    add(DisplayObserver obj);<br/>
    remove(DisplayObserver obj);<br/>
    notify();<br/>
    setTemp();

}
#
DisplayObserver interface{
    Update();
}
#
 class WSobservable implement WSObservable{<br />
    List< DisplayObserver >displayList<br/>
    int temp;<br/>
    add(DisplayObserver obj){} <br />
    remove(DisplayObserver obj){}<br />
    notify(){notify all observer by for loop by update function} <br/>
    setTemp(int newTemp){call based on business logic};
}
#
mobileDisplayObserver implement DisplayObserver{
    WSObservable 
}
#
TvDisplayObserver implement DisplayObserver
