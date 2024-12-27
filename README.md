# Simple_Calculator.c
It's a basic calculator to calculate addition, subtraction, multiplication or division.
#include <stdio.h>

int main() {
    float num1, num2, result;
    char operator;

    // Display the menu
    printf("Enter first number: ");
    scanf("%f", &num1);

    printf("Enter operator (+, -, *, /): ");
    scanf(" %c", &operator);  // Note the space before %c to catch any stray newline character

    printf("Enter second number: ");
    scanf("%f", &num2);

    // Perform the operation based on the operator entered
    switch (operator) {
        case '+':
            result = num1 + num2;
            printf("Result: %.2f\n", result);
            break;

        case '-':
            result = num1 - num2;
            printf("Result: %.2f\n", result);
            break;

        case '*':
            result = num1 * num2;
            printf("Result: %.2f\n", result);
            break;

        case '/':
            if (num2 != 0) {
                result = num1 / num2;
                printf("Result: %.2f\n", result);
            } else {
                printf("Error! Division by zero.\n");
            }
            break;

        default:
            printf("Invalid operator!\n");
    }

    return 0;
}
