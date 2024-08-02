# Simple-calculator
//1.Create a Java program that acts as a simple calculator.

import java.util.Scanner;

public class SimpleCalculator {
    public static void main(String[] args) {
        // Create a scanner object to read input from the user
        Scanner scanner = new Scanner(System.in);
        
        // Prompt the user to enter the first number
        System.out.print("Enter the first number: ");
        double num1 = scanner.nextDouble();
        
        // Prompt the user to enter the second number
        System.out.print("Enter the second number: ");
        double num2 = scanner.nextDouble();
        
        // Prompt the user to enter an operator
        System.out.print("Enter an operator (+, -, *, /): ");
        char operator = scanner.next().charAt(0);
        
        // Variable to store the result of the calculation
        double result;
        
        // Perform the calculation based on the operator
        switch (operator) {
            case '+':
                result = num1 + num2;
                break;
            case '-':
                result = num1 - num2;
                break;
            case '*':
                result = num1 * num2;
                break;
            case '/':
                if (num2 != 0) {
                    result = num1 / num2;
                } else {
                    // Handle division by zero
                    System.out.println("Error: Division by zero is not allowed.");
                    return;
                }
                break;
            default:
                // Handle invalid operator input
                System.out.println("Error: Invalid operator. Please enter one of +, -, *, /.");
                return;
        }
        
        // Display the result of the calculation
        System.out.println("The result is: " + result);
        
        // Close the scanner
        scanner.close();
    }
}



//output

Enter the first number: 10
Enter the second number: 5
Enter an operator (+, -, *, /): /
The result is: 2.0

Enter the first number: 10
Enter the second number: 0
Enter an operator (+, -, *, /): /
Error: Division by zero is not allowed.

Enter the first number: 10
Enter the second number: 5
Enter an operator (+, -, *, /): x
Error: Invalid operator. Please enter one of +, -, *, /.

