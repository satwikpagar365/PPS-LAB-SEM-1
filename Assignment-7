#include <stdio.h>
#include <string.h>

int main() {
    int roll[50];
    char name[50][50];
    float marks[50][3];
    float total[50];
    float percentage[50];
    char result[50][10];

    int n, i, j;
    int failed;

    printf("Enter number of students (max 50): ");
    scanf("%d", &n);

    if (n < 1 || n > 50) {
        printf("Invalid number of students.\n");
        return 1;
    }

    /* Accept details */
    for (i = 0; i < n; i++) {
        printf("\n--- Student %d ---\n", i + 1);

        printf("Roll number: ");
        scanf("%d", &roll[i]);

        printf("Name: ");
        scanf(" %[^\n]", name[i]);

        total[i] = 0;
        failed = 0;

        for (j = 0; j < 3; j++) {
            printf("Marks in subject %d (out of 100): ", j + 1);
            scanf("%f", &marks[i][j]);
            total[i] += marks[i][j];

            if (marks[i][j] < 40)
                failed = 1;
        }

        percentage[i] = total[i] / 3;
        strcpy(result[i], failed ? "FAIL" : "PASS");
    }

    /* Display results */
    printf("\n\n=========================== RESULT ===========================\n");
    printf("%-6s %-20s %-6s %-6s %-6s %-8s %-6s\n",
           "Roll", "Name", "Sub1", "Sub2", "Sub3", "Percent", "Result");
    printf("--------------------------------------------------------------\n");

    for (i = 0; i < n; i++) {
        printf("%-6d %-20s %-6.1f %-6.1f %-6.1f %-8.2f %-6s\n",
               roll[i], name[i],
               marks[i][0], marks[i][1], marks[i][2],
               percentage[i], result[i]);
    }

    return 0;
}
