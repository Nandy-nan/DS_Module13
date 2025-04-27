# EX 1 Display operator precedence in the infix expression.
## DATE:27-04-25
## AIM:
To write a C program to find and display the priority of the operator in the given Postfix expression

## Algorithm
1. Start
2. Input the postfix expression
3. Traverse each character of the expression
4. Determine the priority of the operator
5. Classify and Display the priority
6. Repeat Steps 3–5 for all characters in the expression
7.End 

## Program:
```
/*
Program to find and display the priority of the operator in the given Postfix expression
#include <stdio.h>
#include <ctype.h>

int get_priority(char operator) {
    // Classify operators into categories based on their priority
    switch (operator) {
        case '^':  // Exponentiation
            return 4;  // Highest Priority
        case '*':
        case '/':
        case '%':  // Multiplication, Division, Modulus
            return 3;  // Second Highest Priority
        case '+':
        case '-':  // Addition, Subtraction
            return 2;  // Second Lowest Priority
        case '&':  // Bitwise AND
            return 1;  // Lowest Priority
        default:
            return 0;  // Invalid operator or unknown operator
    }
}

void classify_operator_priority(char expression[]) {
    
    // Loop through the given expression
    for (int i = 0; expression[i] != '\0'; i++) {
        if (ispunct(expression[i])) {  // Check if the character is an operator
            char operator = expression[i];
            int priority = get_priority(operator);

            // Classify the operator based on its priority
            switch (priority) {
                case 4:
                    printf("%c  ----> Highest Priority\n", operator);
                    break;
                case 3:
                    printf("%c  ----> Second Highest Priority\n", operator);
                    break;
                case 2:
                    printf("%c  ----> Second Lowest Priority\n", operator);
                    break;
                case 1:
                    printf("%c  ----> Lowest Priority\n", operator);
                    break;
                default:
                    break;  // In case of an invalid operator
            }
        }
    }
}

int main() {
    // Given Postfix expression
    char expression[] = "(A*B)^C+(D%H)/F&G";

    // Call function to classify the operators
    classify_operator_priority(expression);

    return 0;
}

Developed by: Nandhana R
RegisterNumber:  212223040124
*/
```

## Output:
![image](https://github.com/user-attachments/assets/f01160dd-1ba7-4a38-8b41-66fcd5f34f8d)


               


## Result:
Thus the C program to find and display the priority of the operator in the given Postfix expression is implemented successfully
