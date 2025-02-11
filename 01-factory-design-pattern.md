## Code

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
{{Paste your code here}}
\```

Can you refactor the above code to make it clean, maintainable code by applying Factory Design Pattern?