## Code

```
class WeatherData {
    private double temperature;
    private double humidity;
    private double pressure;
    
    // Methods to get weather data
    public double getTemperature() {
        return temperature;
    }
    public double getHumidity() {
        return humidity;
    }
    public double getPressure() {
        return pressure;
    }
    
    public void measurementsChanged() {
        double temp = getTemperature();
        double humid = getHumidity();
        double pres = getPressure();
        
        // Direct dependency, each display needs to be updated manually here
        CurrentConditionsDisplay.update(temp, humid);
        StatisticsDisplay.update(temp, humid, pres);
    }
}

class CurrentConditionsDisplay {
    public static void update(double temp, double humid) {
        System.out.println("Current conditions: " + temp + "F degrees and " + humid + "% humidity.");
    }
}

class StatisticsDisplay {
    public static void update(double temp, double humid, double pres) {
        System.out.println("Statistics: Temp-" + temp + " Humidity-" + humid + " Pressure-" + pres);
    }
}

public class Main {
    public static void main(String[] args) {
        WeatherData weatherData = new WeatherData();
        weatherData.measurementsChanged(); // Suppose measurements have changed
    }
}


```

## Prompt

\```
{{Paste your code here}}
\```

Can you refactor the above code to make it clean, maintainable code by applying Observer Design Pattern?