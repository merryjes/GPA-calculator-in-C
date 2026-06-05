# GPA-calculator-in-C
A C program that calculates GPA based on Numerical Ratings (NR) and Academic Units (AU


# GPA Calculator in C 🎓



## Overview
This program calculates GPA based on Numerical Ratings (NR) and Academic Units (AU).  
It asks the user for the number of subjects, then computes:

- Total weighted points = NR × AU
- Total units
- GPA = Total weighted points ÷ Total units




#include <stdio.h>

int main() {
    int n, i;
    float NR[50], AU[50], totalPoints = 0, totalUnits = 0, GPA;

    printf("Enter number of subjects: ");
    scanf("%d", &n);

    for (i = 0; i < n; i++) {
        printf("\nSubject %d:\n", i + 1);
        printf("Enter Numerical Rating (NR): ");
        scanf("%f", &NR[i]);
        printf("Enter Academic Units (AU): ");
        scanf("%f", &AU[i]);

        totalPoints += NR[i] * AU[i];  // Weighted points
        totalUnits += AU[i];           // Total units
    }

    GPA = totalPoints / totalUnits;

    printf("\nTotal Weighted Points = %.2f", totalPoints);
    printf("\nTotal Units = %.2f", totalUnits);
    printf("\nGPA = %.2f\n", GPA);

    return 0;
}


can i repository this
