What is Polymorphism?
Polymorphism means "many forms".
In programming, it means different classes can have the same method name, but each class does its own work.

GRASP Polymorphism Principle (In Simple Words):
The Polymorphism principle says:

"If you have many classes that do similar things, but in different ways, give them the same method name and let each class handle it in its own way."

Example (Simple Example):
Imagine you are making a game. You have different characters:

Knight
Wizard
Archer
All characters can attack, but each attacks differently.
Instead of writing separate code for each, you give them a common method called attack().

// Interface
interface Character {
    void attack(); // Common method
}

// Knight class
class Knight implements Character {
    public void attack() {
        System.out.println("Knight attacks with a sword!");
    }
}

// Wizard class
class Wizard implements Character {
    public void attack() {
        System.out.println("Wizard casts a spell!");
    }
}

// Archer class
class Archer implements Character {
    public void attack() {
        System.out.println("Archer shoots an arrow!");
    }
}

// Main class to test
public class Game {
    public static void main(String[] args) {
        // Create objects
        Character knight = new Knight();
        Character wizard = new Wizard();
        Character archer = new Archer();

        // Call attack method
        knight.attack();
        wizard.attack();
        archer.attack();
    }
}

Now, when you say character.attack(), it will do the right thing depending on the type of character.

Why is this useful?
You don't need to check if it's a Knight, Wizard, or Archer.
You can add new characters easily (like Dragon) by just giving them their own attack() method.
Your code becomes cleaner, simpler, and easier to manage.