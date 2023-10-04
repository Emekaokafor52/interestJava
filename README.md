# interestJava
import java.util.Scanner;

public class Interest {
    public static void main(String[] args) {
        // Prompt the user for the starting value of the investment
        double principal = getPrincipal();

        // Calculate the amount after one year with 5% interest
        double amount = calculateInterest(principal);

        // Display the result
        System.out.println("After one year, your investment will grow to: $" + amount);
    }

    // Method to prompt the user for the starting value of the investment
    public static double getPrincipal() {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter the starting value of your investment: $");
        double principal = scanner.nextDouble();
        scanner.close();
        return principal;
    }

    // Method to calculate the amount after one year with 5% interest
    public static double calculateInterest(double principal) {
        double rate = 0.05; // 5% interest rate
        double amount = principal + (principal * rate);
        return amount;
    }
}
