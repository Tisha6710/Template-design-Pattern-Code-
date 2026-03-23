// Abstract class (Template)
abstract class Game {

    // Template method (fixed structure)
    final void play() {
        initialize();
        startPlay();
        endPlay();
    }

    abstract void initialize();
    abstract void startPlay();
    abstract void endPlay();
}

// Cricket class
class Cricket extends Game {
    void initialize() {
        System.out.println("Cricket Game Initialized");
    }

    void startPlay() {
        System.out.println("Cricket Game Started");
    }

    void endPlay() {
        System.out.println("Cricket Game Finished");
    }
}

// Football class
class Football extends Game {
    void initialize() {
        System.out.println("Football Game Initialized");
    }

    void startPlay() {
        System.out.println("Football Game Started");
    }

    void endPlay() {
        System.out.println("Football Game Finished");
    }
}

// Main class
public class Main {
    public static void main(String[] args) {

        Game game1 = new Cricket();
        game1.play();

        System.out.println();

        Game game2 = new Football();
        game2.play();
    }
}
