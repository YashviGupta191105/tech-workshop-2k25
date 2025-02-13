## Code
## Interface common - enforce start over every class
```
class Car {
    public void start() {
        System.out.println("Car started.");
    }
}

class Truck {
    public void start() {
        System.out.println("Truck started.");
    }
}

class Motorcycle {
    public void start() {
        System.out.println("Motorcycle started.");
    }
}

public class Main {
    public static void main(String[] args) {
        Car car = new Car();
        Truck truck = new Truck();
        Motorcycle motorcycle = new Motorcycle();
        
        car.start();
        truck.start();
        motorcycle.start();
    }
}
```

## Prompt

\```
interface Vehicle {
    void start();
}

class Car implements Vehicle {
    public void start() {
        System.out.println("Car started.");
    }
}

class Truck implements Vehicle {
    public void start() {
        System.out.println("Truck started.");
    }
}

class Motorcycle implements Vehicle {
    public void start() {
        System.out.println("Motorcycle started.");
    }
}

class VehicleFactory {
    public static Vehicle getVehicle(String type) {
        switch (type.toLowerCase()) {
            case "car":
                return new Car();
            case "truck":
                return new Truck();
            case "motorcycle":
                return new Motorcycle();
            default:
                throw new IllegalArgumentException("Unknown vehicle type: " + type);
        }
    }
}

public class Main {
    public static void main(String[] args) {
        Vehicle car = VehicleFactory.getVehicle("car");
        Vehicle truck = VehicleFactory.getVehicle("truck");
        Vehicle motorcycle = VehicleFactory.getVehicle("motorcycle");
        
        car.start();
        truck.start();
        motorcycle.start();
    }
}

\```

Can you refactor the above code to make it clean, maintainable code by applying Factory Design Pattern?
