# Builder design pattern
## problem
while creating the object we have to pass a lot of attribute we face problems like:
1. pass all teh parameters
2. some parameters mey be optional

## solution
create object step by step and finally return object
mainly use to create immutable objects
we use functional chaining to create a object of a class

```
class user{
    private final name;
    private final email;

    private user(userBuilder user){
        //initialize 
        this.name=user.name;
        this.email=user.email;
    }
    //generate getter
    class userBuilder{
        private final name;
        private final email;
        
        public user build()
        {
            user user1=new user(this);
            return user1;
        }

        public userBuilder setName(string name)
        {
            this.name=name;
            return this;
        }
        public userBuilder setEmail(String email)
        {
            this.email=email;
            return this.
        }

    }
}
```
with the help of above class we can create a user by method chaining
user= user.userBuilder().setName("Neeraz").setEmail("email").build()