# Polymorphism & Composition Homework - Quiz

# Polymorphism

1. What does the ___word___ 'polymorphism' mean?
occurring in several different forms

2. What does it mean when we apply polymorphism to OO design? Give a simple Java example.
allows an object to take on multiple different forms or behaviours.

public interface IFit {  
    public String getType();
}

public class Battery implements IFit {
    private String type;
    public Battery(String type) { this.type = type; }
    @Override
    public String getType() { return type; }
}

public class Engine implements IFit {
    private String type;
    public Engine(String type) { this.type = type; }
    @Override
    public String getType() { return this.type; }
}

public class Vehicle {
    private ArrayList<IFit> parts = new ArrayList<>();
    public Vehicle() { this.parts = parts;}
}

3. What can we use to implement polymorphism in Java?
inheritance and interfaces

4. How many 'forms' can an object take when using polymorphism?
multiple

5. Give an example of when you could use polymorphism.
Where there are multiple classes with similar behaviours


# Composition and Aggregation

6. What do we mean by 'composition' in reference to object-oriented programming?
a Class which contains other objects as instance variables which are part of the class

7. When would you use composition? Provide a simple example in Java.
where there is a 'has-a' relationship between 2 classes.

public class Engine {
    private String type;
}

public class Vehicle {
    private Engine engine;
    public Vehcile() {
        this.engine = new Engine;
    }
}

In this example, the Vehicle class contains an Engine object as an instance variable and it needs this to function.

8. Give a difference between composition and aggregation?
in composition, the parts cannot exist without the container object, while in aggregation, the parts can exist independently

9. What is/are the advantage(s) of using composition/aggregation?
easier to understand, test and maintain code

10. When using composition, when an object is destroyed, what happens to all the objects it is composed of?
they're destroyed along with it

11. When using aggregation, when an object is destroyed, what happens to all the objects it is composed of?
they still exist independently