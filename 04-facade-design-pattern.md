## Code

```

class DVDPlayer {
    public void on() {
        System.out.println("DVD Player turning on.");
    }

    public void play() {
        System.out.println("DVD Player playing.");
    }

    public void off() {
        System.out.println("DVD Player turning off.");
    }
}

class SoundSystem {
    public void on() {
        System.out.println("Sound System turning on.");
    }

    public void setVolume(int level) {
        System.out.println("Setting volume to " + level);
    }

    public void off() {
        System.out.println("Sound System turning off.");
    }
}

class Projector {
    public void on() {
        System.out.println("Projector turning on.");
    }

    public void setInput(DVDPlayer dvd) {
        System.out.println("Projector input set to DVD Player.");
    }

    public void off() {
        System.out.println("Projector turning off.");
    }
}

public class Main {
    public static void main(String[] args) {
        DVDPlayer dvd = new DVDPlayer();
        SoundSystem sound = new SoundSystem();
        Projector projector = new Projector();

        dvd.on();
        sound.on();
        projector.on();

        sound.setVolume(11);
        projector.setInput(dvd);
        dvd.play();

        dvd.off();
        sound.off();
        projector.off();
    }
}

```

## Prompt

\```
{{Paste your code here}}
\```

Can you refactor the above code to make it clean, maintainable code by applying Facade Design Pattern?