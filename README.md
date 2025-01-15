import java.util.Scanner;

public class Main {
    static int a, b, result, i, fib, choice;

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        do {
            System.out.println("Menu");
            System.out.println("1.Calci");
            System.out.println("2.Factorial");
            System.out.println("3.Fibonacci");
            System.out.println("4.Roots");
            System.out.println("5.Exit");
            System.out.println("Enter your choice:");
            choice = scanner.nextInt();
            System.out.println("Your Choice - " + choice);

            switch (choice) {
                case 1:
                    System.out.println("Calci");
                    System.out.println("1.Sum");
                    System.out.println("2.Sub");
                    System.out.println("3.Mul");
                    System.out.println("4.Div");
                    System.out.println("5.Exit");
                    System.out.println("Enter your choice:");
                    int calc = scanner.nextInt();
                    switch (calc) {
                        case 1:
                            System.out.println("SUM");
                            System.out.println("Enter the two numbers");
                            a = scanner.nextInt();
                            b = scanner.nextInt();
                            result = a + b;
                            System.out.println("The sum of " + a + " and " + b + " is: " + result);
                            break;
                        case 2:
                            System.out.println("SUB");
                            System.out.println("Enter the two numbers");
                            a = scanner.nextInt();
                            b = scanner.nextInt();
                            result = a - b;
                            System.out.println("The difference between " + a + " and " + b + " is: " + result);
                            break;
                        case 3:
                            System.out.println("Mul");
                            System.out.println("Enter the two numbers");
                            a = scanner.nextInt();
                            b = scanner.nextInt();
                            result = a * b;
                            System.out.println("The product of " + a + " and " + b + " is: " + result);
                            break;
                        case 4:
                            System.out.println("Div");
                            System.out.println("Enter the two numbers");
                            a = scanner.nextInt();
                            b = scanner.nextInt();
                            if (b != 0) {
                                result = a / b;
                                System.out.println("The quotient of " + a + " and " + b + " is: " + result);
                            } else {
                                System.out.println("Division by zero is not allowed.");
                            }
                            break;
                        case 5:
                            System.out.println("Exit");
                            break;
                        default:
                            System.out.println("Invalid choice in calculator.");
                    }
                    break;
                case 2:
                    System.out.println("Factorial");
                    System.out.println("Enter your number:");
                    i = scanner.nextInt();
                    if (i < 0) {
                        System.out.println("Factorial of a negative number is undefined.");
                    } else {
                        int fact = 1;
                        int temp = i;  // Save original value of i for the result
                        while (i > 0) {
                            fact = fact * i;
                            i--;
                        }
                        System.out.println("The factorial of " + temp + " is: " + fact);
                    }
                    break;
                case 3:
                    System.out.println("Fibonacci");
                    System.out.println("Enter number of terms:");
                    fib = scanner.nextInt();
                    int n1 = 0, n2 = 1;
                    System.out.print("Fibonacci sequence: ");
                    for (int j = 0; j < fib; j++) {
                        System.out.print(n1 + " ");
                        int num3 = n2 + n1;
                        n1 = n2;
                        n2 = num3;
                    }
                    System.out.println();
                    break;
                case 4:
                    System.out.println("Root");
                    System.out.println("1.Square");
                    System.out.println("2.Cube");
                    System.out.println("3.Quad");
                    System.out.println("4.Exit");
                    int root_ch = scanner.nextInt();
                    switch (root_ch) {
                        case 1:
                            System.out.println("Square");
                            i = scanner.nextInt();
                            result = i * i;
                            System.out.println("The square of " + i + " is: " + result);
                            break;
                        case 2:
                            System.out.println("Cube");
                            i = scanner.nextInt();
                            result = i * i * i;
                            System.out.println("The cube of " + i + " is: " + result);
                            break;
                        case 3:
                            System.out.println("Quad");
                            i = scanner.nextInt();
                            result = i * i * i * i;
                            System.out.println("The fourth power of " + i + " is: " + result);
                            break;
                        default:
                            System.out.println("Invalid choice in roots.");
                    }
                    break;
                case 5:
                    System.out.println("Exiting...");
                    break;
                default:
                    System.out.println("Invalid Choice.");
            }
        } while (choice != 5);

        scanner.close();
    }
}
# lab01
