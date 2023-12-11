/*
  Author: Dipesh Kumar Paswan
  Date: December 11, 2023
  Description: This program for multiplying of two matrices 
*/

    #include <stdio.h>
    int main() {
    int a[10][10], b[10][10], mul[10][10], r, c, i, j, k;
    
    printf("Enter the number of rows\n");
    scanf("%d", &r);
    printf("Enter the number of columns\n");
    scanf("%d", &c);

    printf("Enter the elements of the first matrix:\n");
    for(i = 0; i < r; i++) {
        for(j = 0; j < c; j++) {
            scanf("%d", &a[i][j]);
        }
    }

    printf("Enter the elements of the second matrix:\n");
    for(i = 0; i < r; i++) {
        for(j = 0; j < c; j++) {
            scanf("%d", &b[i][j]);
        }
    }

    // Multiplying the matrices
    for(i = 0; i < r; i++) {
        for(j = 0; j < c; j++) {
            mul[i][j] = 0;
            for(k = 0; k < c; k++) {
                mul[i][j] += a[i][k] * b[k][j];
            }
        }
    }

    printf("Resultant matrix after multiplication:\n");
    for(i = 0; i < r; i++) {
        for(j = 0; j < c; j++) {
            printf("%d ", mul[i][j]);
        }
        printf("\n");
    }

    return 0;
}

