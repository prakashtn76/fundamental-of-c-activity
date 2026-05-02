# fundamental-of-c-activity
##Question:

1.Write a C program to print all prime numbers between two limits.

#include <stdio.h>

int main() {
    
    
    int lower, upper, i, j, prime;

    printf("Enter lower limit: ");
    scanf("%d", &lower);

    printf("Enter upper limit: ");
    scanf("%d", &upper);

    printf("Prime numbers between %d and %d are:\n", lower, upper);

    for(i = lower; i <= upper; i++) {
        if(i < 2)
            continue;

        prime = 1;

        for(j = 2; j < i; j++) {
            if(i % j == 0) {
                prime = 0;
                break;
            }
        }

        if(prime)
            printf("%d ", i);
    }

    return 0;
}
Prime numbers between 10 and 50 are:
11 13 17 19 23 29 31 37 41 43 47



####Question2:

Write a C program to count the number of digits in a number.

#include <stdio.h>

int main() {

    int num, count = 0;
    printf("Enter a number: ");
    scanf("%d", &num);

    while(num != 0) {
        num = num / 10;
        count++;
    }

    printf("Number of digits = %d", count);

    return 0;
}

Output:
Enter a number: 987654
Number of digits = 6

####Question:

Write a C program to print the alphabet S in n x n matrix.
CODE
#include <stdio.h>

int main() {
    int n, i, j;

    printf("Enter size of matrix: ");
    scanf("%d", &n);

    for(i = 0; i < n; i++) {
        for(j = 0; j < n; j++) {
            if(i == 0 || i == n/2 || i == n-1 || (j == 0 && i < n/2) || (j == n-1 && i > n/2))
                printf("*");
            else
                printf(" ");
        }
        printf("\n");
    }

    return 0;
}

OUTPUT
Enter size of matrix: 7
*******
*
*
*******
      *
      *
*******

Question:

Write a C program to print the pyramid pattern.
CODE

#include <stdio.h>

int main() {
    int rows, i, j, space;

    printf("Enter number of rows: ");
    scanf("%d", &rows);

    for(i = 1; i <= rows; i++) {
        for(space = 1; space <= rows - i; space++) {
            printf(" ");
        }

        for(j = 1; j <= (2 * i - 1); j++) {
            printf("*");
        }

        printf("\n");
    }

    return 0;
}

OUTPUT
Enter number of rows: 4
   *
  ***
 *****
*******

Question5:

Write a C program to find GCD of two numbers using loop.
CODE

#include <stdio.h>

int main() {
    int num1, num2, i, gcd;

    printf("Enter two numbers: ");
    scanf("%d %d", &num1, &num2);

    for(i = 1; i <= num1 && i <= num2; i++) {
        if(num1 % i == 0 && num2 % i == 0) {
            gcd = i;
        }
    }

    printf("GCD of %d and %d = %d", num1, num2, gcd);

    return 0;
}
OUTPUT
Enter two numbers: 24 36
GCD of 24 and 36 = 12
