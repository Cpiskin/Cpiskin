import java.util.Scanner; // Import the Scanner class

public class GuessTheNumber {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in); // Create a Scanner object

        int secretNumber = (int) (Math.random() * 100) + 1; // Generate a random number between 1 and 100
        int attempts = 0; // Initialize the attempts counter

        System.out.println("Welcome to Guess the Number!");
        System.out.println("I'm thinking of a number between 1 and 100.");

        while (true) {
            System.out.print("Guess the number: ");
            int userGuess = scanner.nextInt(); // Read user input

            attempts++; // Increment the attempts counter

            if (userGuess == secretNumber) {
                System.out.println("Congratulations! You guessed the number in " + attempts + " attempts.");
                break; // Exit the loop when the user guesses correctly
            } else if (userGuess < secretNumber) {
                System.out.println("Try a higher number.");
            } else {
                System.out.println("Try a lower number.");
            }
        }

        scanner.close(); // Close the Scanner
    }
}
