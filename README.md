/*Jubier Hasan Rafi_ID:241-33-191*/
/*Create a Scientific Calculator*/
#include <stdio.h>
#include <math.h>

void displayMenu() {
    printf("====== Welcome To My Scientific Calculator ======\n");
    printf("1. Summation\n");
    printf("2. Difference\n");
    printf("3. Product\n");
    printf("4. Division\n");
    printf("5. Sine\n");
    printf("6. Cosine\n");
    printf("7. Tangent\n");
    printf("8. Logarithm\n");
    printf("9. Natural Logarithm\n");
    printf("10. Exponentiation\n");
    printf("11. Power\n");
    printf("12. Square Root\n");
    printf("0. Exit\n");
    printf("===================================\n");}

void performOperation(int choice) {
    double num1, num2, result;

    switch (choice) {
        case 1:
            printf("Enter two numbers: ");
            scanf("%lf %lf", &num1, &num2);
            result = num1 + num2;
            printf("Result: %.2lf\n", result);
            break;

        case 2:
            printf("Enter two numbers: ");
            scanf("%lf %lf", &num1, &num2);
            result = num1 - num2;
            printf("Result: %.2lf\n", result);
            break;

        case 3:
            printf("Enter two numbers: ");
            scanf("%lf %lf", &num1, &num2);
            result = num1 * num2;
            printf("Result: %.2lf\n", result);
            break;

        case 4: 
            printf("Enter two numbers: ");
            scanf("%lf %lf", &num1, &num2);
            if (num2 != 0) {
                result = num1 / num2;
                printf("Result: %.2lf\n", result);
            } else 
            {printf("Error: Division by zero is not allowed.\n");}
            break;

        case 5: 
            printf("Enter the angle in degrees: ");
            scanf("%lf", &num1);
            result = sin(num1 * M_PI / 180); 
            printf("Result: %.2lf\n", result);
            break;

        case 6: 
            printf("Enter the angle in degrees: ");
            scanf("%lf", &num1);
            result = cos(num1 * M_PI / 180); 
            printf("Result: %.2lf\n", result);
            break;

        case 7: 
            printf("Enter the angle in degrees: ");
            scanf("%lf", &num1);
            result = tan(num1 * M_PI / 180); 
            printf("Result: %.2lf\n", result);
            break;

        case 8: 
            printf("Enter a number: ");
            scanf("%lf", &num1);
            if (num1 > 0) {
                result = log10(num1);
                printf("Result: %.2lf\n", result);
            } else 
            {printf("Error: Logarithm undefined for non-positive numbers.\n");}
            break;

        case 9: 
            printf("Enter a number: ");
            scanf("%lf", &num1);
            if (num1 > 0) {
                result = log(num1);
                printf("Result: %.2lf\n", result);
            } else 
            {printf("Error: Natural logarithm undefined for non-positive numbers.\n");}
            break;

        case 10: 
            printf("Enter the power: ");
            scanf("%lf", &num1);
            result = exp(num1);
            printf("Result: %.2lf\n", result);
            break;

        case 11: 
            printf("Enter the base and exponent: ");
            scanf("%lf %lf", &num1, &num2);
            result = pow(num1, num2);
            printf("Result: %.2lf\n", result);
            break;

        case 12: 
            printf("Enter a number: ");
            scanf("%lf", &num1);
            if (num1 >= 0) {
                result = sqrt(num1);
                printf("Result: %.2lf\n", result);} 
            else 
            {printf("Error: Square root of negative numbers is not allowed.\n");}
            break;

        case 0: 
            printf("Exiting the calculator. Goodbye!\n");
            break;

        default:
            printf("Invalid choice! Please select a valid operation.\n");
    }
}

int main() {
    int choice;

    do {
        displayMenu();
        printf("Enter your choice: ");
        scanf("%d", &choice);

        if (choice != 0) {
            performOperation(choice);
        }

    } while (choice != 0);
    printf("Developed by: Jubier Hasan Rafi\n");
    return 0;
}
