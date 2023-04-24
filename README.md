public enum AnimalType {
    MAMMAL,
    BIRD,
    REPTILE,
    AMPHIBIAN,
    FISH
}

public class Dog {
    private String breed;
    private int age;
    private String name;

    public Dog(String breed, int age, String name) {
        this.breed = breed;
        this.age = age;
        this.name = name;
    }

    public String getBreed() {
        return breed;
    }

    public int getAge() {
        return age;
    }

    public String getName() {
        return name;
    }

    public void bark() {
        System.out.println(name + " barks!");
    }

    public void fetch() {
        System.out.println(name + " fetches the ball!");
    }
}

public interface Pet {
    void playWith();
}
public class Dog implements Pet {
    private String breed;
    private int age;
    private String name;

    public Dog(String breed, int age, String name) {
        this.breed = breed;
        this.age = age;
        this.name = name;
    }

    public String getBreed() {
        return breed;
    }

    public int getAge() {
        return age;
    }

    public String getName() {
        return name;
    }

    public void bark() {
        System.out.println(name + " barks!");
    }

    public void fetch() {
        System.out.println(name + " fetches the ball!");
    }

    @Override
    public void playWith() {
        System.out.println(name + " plays with you!");
    }
}

// Bird interface
public interface Bird {
    public void fly();
}

// Parrot class implementing Bird interface
public class Parrot implements Bird {
    public void fly() {
        System.out.println("Parrot is flying!");
    }
}

// Dog class
public class Dog {
    public void bark() {
        System.out.println("Woof!");
    }
}

// Bird interface
public interface Bird {
    public void fly();
}

// Parrot class implementing Bird interface
public class Parrot implements Bird {
    public void fly() {
        System.out.println("Parrot is flying!");
    }
}

// Main class
public class Main {
    public static void main(String[] args) {
        // Creating instances of Dog and Parrot classes
        Dog myDog = new Dog();
        Parrot myParrot = new Parrot();

        // Calling methods of Dog and Parrot classes
        myDog.bark();
        myParrot.fly();
    }
}
