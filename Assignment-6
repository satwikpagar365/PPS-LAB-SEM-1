#include <stdio.h>

// Function to calculate factorial without recursion
int factorialWithoutRecursion(int n)
{
    int fact = 1;

    for(int i = 1; i <= n; i++)
    {
        fact = fact * i;
    }

    return fact;
}

// Recursive function to calculate factorial
int factorialWithRecursion(int n)
{
    if(n == 0 || n == 1)
    {
        return 1;
    }
    else
    {
        return n * factorialWithRecursion(n - 1);
    }
}

int main()
{
    int num;

    printf("Enter a number: ");
    scanf("%d", &num);

    if(num < 0)
    {
        printf("Factorial of a negative number is not defined.\n");
    }
    else
    {
        printf("Factorial without recursion = %d\n", factorialWithoutRecursion(num));

        printf("Factorial with recursion = %d\n", factorialWithRecursion(num));
    }

    return 0;
}
