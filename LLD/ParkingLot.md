# parking lot design
* first create a Rough flow

vehicle coming->entrance gate-->parking spot-->exit(payment)-vehicle out

## what interviewer is looking for:
* How good are you in requirement collection
* Object-oriented design skills, classes and component
* Think in different object oriented design patterns
* Tackling concurrency

## Requirement collection
* Big parking lot(20K to 30K) 
* 4 entrance, 4 exit
* customer collect ticket and get the ticket which have time, ticket number, parking lot number
* parking lot should be near to the entrance
* Limit for parking lot
* Type of parking spots - bike, HC, car
* hourly rate
* payment type(cash card)
* monitoring system
* code should be reusable it can be used different places like mall, airport

# actors and objects in the system
* Parking lot system
* Entry exit terminal(printer)
* parking spot(Create a abstract class for parking spot and inherent it for different types of parking spot
  )
* ticket:id,parking spot, parking spot type, issue time
* database
* monitoring system
* parking assignment strategy(findParkingSpot(near to the entrance), fillParkingSpot(),vacantParkingSpot())
### Payment system(strategy design pattern)
### tariff calculator(time, parking spot type)(interface)extend for different type of tariff calculation like weekdays weekends
### monitoring system(observer design pattern)(log message)
### parking  class(singleton design pattern)
different object