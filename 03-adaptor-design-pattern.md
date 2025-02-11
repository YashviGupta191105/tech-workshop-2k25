## Code

```
class Appliance {
    private int voltage;

    public Appliance(int voltage) {
        this.voltage = voltage;
    }

    public void run() {
        System.out.println("Running appliance at " + voltage + " volts!");
    }
}

class WallSocket {
    private int voltage = 220; // Default voltage of the wall socket

    public void plugIn(Appliance appliance) {
        appliance.run(); // Directly run the appliance with the wall socket's voltage
    }
}

public class Main {
    public static void main(String[] args) {
        Appliance appliance = new Appliance(110);
        WallSocket socket = new WallSocket();
        socket.plugIn(appliance); // This should not work correctly but is forced in this naive implementation.
    }
}

```

## Prompt

\```
{{Paste your code here}}
\```

Can you refactor the above code to make it clean, maintainable code by applying Adapter Design Pattern?