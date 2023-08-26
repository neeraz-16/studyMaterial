# Problem
create a object(single instance) and use it in all the project

# solution:
1. create the constructor as private
2. create a static method

example:
```
class JDBC{
    //Lazy way-- not thread safe--we can make it thread safe by using synchronized block
    private static JDBC jdbc;
    private JDBC(){}
    public static JDBC getJDBC()
    {
        if(jdbc==null)
        {
            jdbc=new JDBC();
        }
        return jdbc;
    } 
    //Eager way;
    private static JDBC jdbc=new JDBC();
    private JDBC(){}
    public static JDBC getJDBC()
    {
        return jdbc;
    }
}
```
This pattern can be break by multiple way
1. by cloning-> override clone method
2. by reflection api we can access constructor-> write login in constructor or use enum
3. by serialization and deserialization ->  override readResolve method
