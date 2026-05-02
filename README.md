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
