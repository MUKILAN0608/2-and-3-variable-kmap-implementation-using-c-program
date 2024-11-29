#include <stdio.h>
#include <stdlib.h>
void twoVariable() {
    int SIZE = 2;
    int Kmap[SIZE][SIZE];
    int numMinTerms, i, j;
   
   
    for (i = 0; i < SIZE; i++) {
        for (j = 0; j < SIZE; j++) {
            Kmap[i][j] = 0;
        }
    }

    printf("2-Variable K-Map:\n");
    printf("\t\t0\t\t1\n");
    printf("\t\tB'\t\tB\n");
    printf("0\tA'\tm0\t\tm1 \n");
    printf("1\tA\tm2\t\tm3 \n");

    printf("ENTER THE NUMBER OF MIN TERMS: ");
    scanf("%d", &numMinTerms);
    int *MinTerm = (int *)malloc(numMinTerms * sizeof(int)); 
    if (MinTerm == NULL) {
        printf("Memory allocation failed!");
        return;
    }
   
    printf("Enter the min terms:\n");
    for (i = 0; i < numMinTerms; i++) {
        int minTerm;
        scanf("%d", &minTerm);
        if (minTerm < 0 || minTerm > 3) {
            printf("Invalid min term! Please enter min terms between 0 and 3.\n");
            i--; 
            continue;
        }
        MinTerm[i] = minTerm;
       
       
        int row = minTerm / 2;
        int col = minTerm % 2;
       
        Kmap[row][col] = 1;
    }
   
    printf("\n");

  
    printf("Updated K-map:\n");
    printf("\tB'\tB\n");

            for (i = 0; i < SIZE; i++) {
                printf("A%c\t", (i == 0) ? '\'' : ' ');
                for (j = 0; j < SIZE; j++) {
                    if (Kmap[i][j] == 0) {
                        if (i == 0 && j == 0)
                            printf("m0\t");
                        else if (i == 0 && j == 1)
                            printf("m1\t");
                        else if (i == 1 && j == 0)
                            printf("m2\t");
                        else if (i == 1 && j == 1)
                            printf("m3\t");
                    } else {
                        printf("%d\t", Kmap[i][j]);
                    }
                }
                printf("\n");
            }
   
    if(numMinTerms==1)
    {
        if(MinTerm[0]==0)
        {
            printf("\nThe Simplfied Expression is A'B' ");
        }
        else if(MinTerm[0]==1)
        {
            printf("The Simplfied Expression is A'B ");
        }
        else if(MinTerm[0]==2)
        {
            printf("The Simplfied Expression is AB' ");
        }
        else if(MinTerm[0]==3)
        {
            printf("The Simplfied Expression is AB ");
        }
    }
    if(numMinTerms==2)
    {
        if(MinTerm[0]==0)
        {
            if(MinTerm[1]==1)
            {
                printf("The Simplfied Expression is A' ");
            }
            else if(MinTerm[1]==2)
            {
                printf("The Simplfied Expression is B' ");
            }
            else if(MinTerm[1]==3)
            {
                printf("The Simplfied Expression is A'B'+AB ");
            }
        }
        if(MinTerm[0]==1)
        {
            if(MinTerm[1]==2)
            {
                printf("The Simplfied Expression is A'B+AB' ");
            }
            else if(MinTerm[1]==3)
            {
                printf("The Simplfied Expression is B ");
            }
        }
        if(MinTerm[0]==2)
        {
            if(MinTerm[1]==3)
            {
                printf("The Simplfied Expression is A ");
            }
        }
    }
   
   if(numMinTerms==3)
    {
        if(MinTerm[0]==0)
        {
            if(MinTerm[1]==1)
            {
                if(MinTerm[2]==2)
                {
                    printf("The Simplfied Expression is A'+B' ");
                }
                else if(MinTerm[2]==3)
                {
                    printf("The Simplfied Expression is A'+B ");
                }
            }
            else if(MinTerm[1]==2)
            {
                if(MinTerm[2]==3)
                {
                    printf("The Simplfied Expression is A+B' ");
                }
            }
        }
        else if (MinTerm[0]==1)
        {
            if(MinTerm[1]==2)
            {
                if(MinTerm[2]==3)
                {
                    printf("The Simplfied Expression is A+B ");
                }
            }
        }
    }
       
    if(numMinTerms==4)
    {
        printf("The Simplfied Expression is 1 ");
    }
    free(MinTerm); // Free dynamically allocated memory
}

void threeVariable() {
    int SIZE = 2;
    int SIZE1 = 4;
    int Kmap[SIZE][SIZE1]; // Initialize K-map with zeros
    int numMinTerms, i, j;
    for (i = 0; i < SIZE; i++)
    {
        for (j = 0; j < SIZE1; j++)
        {
            Kmap[i][j] = 0;
        }
    }
    printf("3-Variable K-Map:\n");
    printf("\t00\t\t01\t\t11\t\t10\n");
    printf("\tB'C'\tB'C\t\tBC\t\tBC'\n");
    printf("0 A'm0\t\tm1\t\tm3\t\tm2\n");
    printf("1 A m4\t\tm5\t\tm7\t\tm6\n");
    printf("ENTER THE NUMBER OF MIN TERMS: ");
    scanf("%d", &numMinTerms);
    int *MinTerm = (int *)malloc(numMinTerms * sizeof(int));
    printf("Enter the min terms:\n");
    for (i = 0; i < numMinTerms; i++)
    {
        int minTerm;
        scanf("%d", &minTerm);
        if (minTerm < 0 || minTerm > 7)
        {
            printf("Invalid min term! Please enter min terms between 0 and 7.\n");
            printf("1");
        }
        MinTerm[i] = minTerm;
       
        // Calculate the row and column index from the min term
        int row, col;
        if (minTerm == 0)
            row = 0, col = 0;
        else if (minTerm == 1)
            row = 0, col = 1;
        else if (minTerm == 3)
            row = 0, col = 2;
        else if (minTerm == 2)
            row = 0, col = 3;
        else if (minTerm == 4)
            row = 1, col = 0;
        else if (minTerm == 5)
            row = 1, col = 1;
        else if (minTerm == 7)
            row = 1, col = 2;
        else if (minTerm == 6)
            row = 1, col = 3;
        // Set the corresponding cell in the K-map to 1
        Kmap[row][col] = 1;
    }

    printf("Updated K-map:\n");
    printf("\tB'C'B'C\tBC\tBC'\n");
    for (i = 0; i < SIZE; i++)
    {
        printf("A%c\t", (i == 0) ? '\'' : ' ');
        for (j = 0; j < SIZE1; j++)
        {
            if (Kmap[i][j] == 0)
            {
                if (i == 0 && j == 0)
                printf("m0\t");
                else if (i == 0 && j == 1)
                    printf("m1\t");
                else if (i == 0 && j == 2)
                    printf("m3\t");
                else if (i == 0 && j == 3)
                    printf("m2\t");
                else if (i == 1 && j == 0)
                    printf("m4\t");
                else if (i == 1 && j == 1)
                    printf("m5\t");
                else if (i == 1 && j == 2)
                    printf("m7\t");
                else if (i == 1 && j == 3)
                    printf("m6\t");
            }
            else
            {
                printf("%d\t", Kmap[i][j]);
            }
        }
        printf("\n");
    }
    if(numMinTerms==1)
    {
        if(MinTerm[0]==0)
        {
            printf("The Simplfied Expression is A'B'C' ");
        }
        if(MinTerm[0]==1)
        {
            printf("The Simplfied Expression is A'B'C ");
        }
        if(MinTerm[0]==2)
        {
            printf("The Simplfied Expression is A'BC' ");
        }
        if(MinTerm[0]==3)
        {
            printf("The Simplfied Expression is ABC ");
        }
        if(MinTerm[0]==4)
        {
            printf("The Simplfied Expression is AB'C' ");
        }
        if(MinTerm[0]==5)
        {
            printf("The Simplfied Expression is AB'C ");
        }
        if(MinTerm[0]==6)
        {
            printf("The Simplfied Expression is ABC' ");
        }
        if(MinTerm[0]==7)
        {
            printf("The Simplfied Expression is ABC ");
        }
    }
    if(numMinTerms==2)
    {
    if(MinTerm[0]==0)
    {
        if(MinTerm[1]==1)
        {
            printf("The Simplfied Expression is A'B' ");
        }
        else if(MinTerm[1]==2)
        {
            printf("The Simplfied Expression is A'C' ");
        }
        else if(MinTerm[1]==3)
        {
            printf("The Simplfied Expression is A'B'C'+A'BC ");
        }
        else if(MinTerm[1]==4)
        {
            printf("The Simplfied Expression is B'C' ");
        }
        else if(MinTerm[1]==5)
        {
            printf("The Simplfied Expression is A'B'C'+AB'C ");
        }
        else if(MinTerm[1]==6)
        {
            printf("The Simplfied Expression is A'B'C'+ABC' ");
        }
        else if(MinTerm[1]==7)
        {
            printf("The Simplfied Expression is A'B'C'+ABC ");
        }
    }
    else if(MinTerm[0]==1)
    {
        if(MinTerm[1]==2)
        {
            printf("The Simplfied Expression is A'B'C+A'BC' ");
        }
        else if(MinTerm[1]==3)
        {
            printf("The Simplfied Expression is A'C ");
        }
        else if(MinTerm[1]==4)
        {
            printf("The Simplfied Expression is A'B'C+AB'C' ");
        }
        else if(MinTerm[1]==5)
        {
            printf("The Simplfied Expression is B'C ");
        }
        else if(MinTerm[1]==6)
        {
            printf("The Simplfied Expression is A'B'C+ABC' ");
        }
        else if(MinTerm[1]==7)
        {
            printf("The Simplfied Expression is A'B'C+ABC ");
        }
    }
    else if(MinTerm[0]==2)
    {
        if(MinTerm[1]==3)
        {
            printf("The Simplfied Expression is A'B ");
        }
        else if(MinTerm[1]==4)
        {
            printf("The Simplfied Expression is A'BC'+AB'C' ");
        }
        else if(MinTerm[1]==5)
        {
            printf("The Simplfied Expression is A'BC'+AB'C ");
        }
        else if(MinTerm[1]==6)
        {
            printf("The Simplfied Expression is BC' ");
        }
        else if(MinTerm[1]==7)
        {
            printf("The Simplfied Expression is A'BC'+ABC ");
        }
    }
    else if(MinTerm[0]==3)
    {
        if(MinTerm[1]==4)
        {
            printf("The Simplfied Expression is A'BC+AB'C' ");
        }
        else if(MinTerm[1]==5)
        {
            printf("The Simplfied Expression is A'BC+AB'C ");
        }
        else if(MinTerm[1]==6)
        {
            printf("The Simplfied Expression is A'BC+ ABC'");
        }
        else if(MinTerm[1]==7)
        {
            printf("The Simplfied Expression is BC ");
        }
    }
    else if(MinTerm[0]==4)
    {
        if(MinTerm[1]==5)
        {
            printf("The Simplfied Expression is AB' ");
        }
        else if(MinTerm[1]==6)
        {
            printf("The Simplfied Expression is A'C' ");
        }
        else if(MinTerm[1]==7)
        {
            printf("The Simplfied Expression is AB'C'+ABC ");
        }
    }
    else if(MinTerm[0]==5)
    {
        if(MinTerm[1]==6)
        {
            printf("The Simplfied Expression is AB'C+ABC' ");
        }
        else if(MinTerm[1]==7)
        {
            printf("The Simplfied Expression is AC ");
        }
    }
    else if(MinTerm[0]==6)
    {
        if(MinTerm[1]==7)
        {
            printf("The Simplfied Expression is AB ");
        }
    }
}
    if(numMinTerms==3)
    {
        if(MinTerm[0]==0)
        {
            if(MinTerm[1]==1)
            {
                if(MinTerm[2]==2)
                {
                    printf("The Simplfied Expression is A'B'+A'C' ");
                }
                else if(MinTerm[2]==3)
                {
                    printf("The Simplfied Expression is A'B'+A'C ");
                }
                else if(MinTerm[2]==4)
                {
                    printf("The Simplfied Expression is A'B'+B'C' ");
                }
                else if(MinTerm[2]==5)
                {
                    printf("The Simplfied Expression is A'B'+B'C ");
                }
                else if(MinTerm[2]==6)
                {
                    printf("The Simplfied Expression is A'B'+ABC' ");
                }
                else if(MinTerm[2]==7)
                {
                    printf("The Simplfied Expression is A'B'+ABC ");
                }
            }
            else if(MinTerm[1]==2)
            {
                if(MinTerm[2]==3)
                {
                    printf("The Simplfied Expression is A'C'+A'B ");
                }
                else if(MinTerm[2]==4)
                {
                    printf("The Simplfied Expression is A'C'+B'C' ");
                }
                else if(MinTerm[2]==5)
                {
                    printf("The Simplfied Expression is A'C'+AB'C ");
                }
                else if(MinTerm[2]==6)
                {
                    printf("The Simplfied Expression is A'C'+BC' ");
                }
                else if(MinTerm[2]==7)
                {
                    printf("The Simplfied Expression is A'C'+ABC ");
                }
            }
            if(MinTerm[1]==3)
            {
                if(MinTerm[2]==4)
                {
                    printf("The Simplfied Expression is B'C'+A'BC ");
                }
                else if(MinTerm[2]==5)
                {
                    printf("The Simplfied Expression is A'B'C'+A'BC+AB'C ");
                }
                else if(MinTerm[2]==6)
                {
                    printf("The Simplfied Expression is A'B'C'+A'BC+ABC' ");
                }
                else if(MinTerm[2]==7)
                {
                    printf("The Simplfied Expression is A'B'C'+BC ");
                }
            }
            if(MinTerm[1]==4)
            {
                if(MinTerm[2]==5)
                {
                    printf("The Simplfied Expression is B'C'+AB' ");
                }
                else if(MinTerm[2]==6)
                {
                    printf("The Simplfied Expression is B'C'+AC' ");
                }
                else if(MinTerm[2]==7)
                {
                    printf("The Simplfied Expression is B'C'+ABC ");
                }
            }
            if(MinTerm[1]==5)
            {
               if(MinTerm[2]==6)
                {
                    printf("The Simplfied Expression is A'B'C'+AB'C+ABC' ");
                }
                else if(MinTerm[2]==7)
                {
                    printf("The Simplfied Expression is A'B'C'+AC ");
                }
            }
            if(MinTerm[2]==6)
            {
               if(MinTerm[2]==7)
                {
                    printf("The Simplfied Expression is A'B'C'+AB ");
                }  
            }
        }
        else if (MinTerm[0]==1)
        {
            if(MinTerm[1]==2)
            {
                if(MinTerm[2]==3)
                {
                    printf("The Simplfied Expression is A'C+A'B ");
                }
                else if(MinTerm[2]==4)
                {
                    printf("The Simplfied Expression is A'B'C+A'BC'+AB'C' ");
                }
                else if(MinTerm[2]==5)
                {
                    printf("The Simplfied Expression is B'C+A'B'C' ");
                }
                else if(MinTerm[2]==6)
                {
                    printf("The Simplfied Expression is BC'+A'B'C ");
                }
                else if(MinTerm[2]==7)
                {
                    printf("The Simplfied Expression is A'B'C+A'BC'+ABC ");
                }
            }
            else if(MinTerm[1]==3)
            {
                if(MinTerm[2]==4)
                {
                    printf("The Simplfied Expression is A'C+AB'C' ");
                }
                else if(MinTerm[2]==5)
                {
                    printf("The Simplfied Expression is A'C+B'C ");
                }
                else if(MinTerm[2]==6)
                {
                    printf("The Simplfied Expression is A'C+ABC' ");
                }
                else if(MinTerm[2]==7)
                {
                    printf("The Simplfied Expression is A'C+BC ");
                }
            }
            else if(MinTerm[1]==4)
            {
                if(MinTerm[2]==5)
                {
                    printf("The Simplfied Expression is AB'+B'C ");
                }
                else if(MinTerm[2]==6)
                {
                    printf("The Simplfied Expression is AC'+A'B'C ");
                }
                else if(MinTerm[2]==7)
                {
                    printf("The Simplfied Expression is A'B'C+AB'C'+ABC ");
                }
            }
            else if(MinTerm[1]==5)
            {
                 if(MinTerm[2]==6)
                {
                    printf("The Simplfied Expression is B'C+ABC ");
                }
                else if(MinTerm[2]==7)
                {
                    printf("The Simplfied Expression is B'C+AC ");
                }
            }
            else if(MinTerm[1]==6)
            {
                if(MinTerm[2]==7)
                {
                    printf("The Simplfied Expression is AB+A'B'C ");
                }
            }
        }
        else if (MinTerm[0]==2)
        {
            if(MinTerm[1]==3)
            {
                if(MinTerm[2]==4)
                {
                    printf("The Simplfied Expression is A'B+ AB'C'");
                }
                else if(MinTerm[2]==5)
                {
                    printf("The Simplfied Expression is A'B+AB'C ");
                }
                else if(MinTerm[2]==6)
                {
                    printf("The Simplfied Expression is A'B+BC' ");
                }
                else if(MinTerm[2]==7)
                {
                    printf("The Simplfied Expression is A'B+BC ");
                }
            }
            if(MinTerm[1]==4)
            {
                if(MinTerm[2]==5)
                {
                    printf("The Simplfied Expression is AB'+A'BC' ");
                }
                else if(MinTerm[2]==6)
                {
                    printf("The Simplfied Expression is AC'+BC' ");
                }
                else if(MinTerm[2]==7)
                {
                    printf("The Simplfied Expression is A'BC'+AB'C'+ABC ");
                }
            }
            if(MinTerm[1]==5)
            {
               if(MinTerm[2]==6)
                {
                    printf("The Simplfied Expression is BC'+AB'C ");
                }
                else if(MinTerm[2]==7)
                {
                    printf("The Simplfied Expression is AC+A'BC' ");
                }
            }
            if(MinTerm[1]==6)
            {
                if(MinTerm[2]==7)
                {
                    printf("The Simplfied Expression is BC'+AB ");
                }
            }
        }
        else if (MinTerm[0]==3)
        {
            if(MinTerm[1]==4)
            {
                if(MinTerm[2]==5)
                {
                    printf("The Simplfied Expression is AB'+A'BC ");
                }
                else if(MinTerm[2]==6)
                {
                    printf("The Simplfied Expression is A'C'+A'BC ");
                }
                else if(MinTerm[2]==7)
                {
                    printf("The Simplfied Expression is BC+AB'C' ");
                }
            }
            if(MinTerm[1]==5)
            {
               if(MinTerm[2]==6)
                {
                    printf("The Simplfied Expression is A'BC+AB'C+ABC' ");
                }
                else if(MinTerm[2]==7)
                {
                    printf("The Simplfied Expression is BC+AC ");
                }
            }
            if(MinTerm[1]==6)
            {
                if(MinTerm[2]==7)
                {
                    printf("The Simplfied Expression is BC+AB ");
                }
            }
        }
        else if (MinTerm[0]==4)
        {
            if(MinTerm[1]==5)
            {
               if(MinTerm[2]==6)
                {
                    printf("The Simplfied Expression is AB'+AC' ");
                }
                else if(MinTerm[2]==7)
                {
                    printf("The Simplfied Expression is AB'+AC ");
                }
            }
            else if(MinTerm[1]==6)
            {
                if(MinTerm[2]==7)
                {
                    printf("The Simplfied Expression is AC'+AB ");
                }
            }
        }
        else if (MinTerm[0]==5)
        {
            if(MinTerm[1]==6)
            {
                if(MinTerm[2]==7)
                {
                    printf("The Simplfied Expression is AC+AB ");
                }
            }
        }
    }
    if(numMinTerms==4)
    {
        if(MinTerm[0]==0)
        {
            if(MinTerm[1]==1)
            {
                if(MinTerm[2]==2)
                {
                    if(MinTerm[3]==3)
                    {
                        printf("The Simplfied Expression is A' ");
                    }
                    else if(MinTerm[3]==4)
                    {
                       printf("The Simplfied Expression is B'C'+A'C+A'BC' ");
                    }
                    else if(MinTerm[3]==5)
                    {
                       printf("The Simplfied Expression is A'B'+A'C'+B'C ");
                    }
                    else if(MinTerm[3]==6)
                    {
                       printf("The Simplfied Expression is A'B'BC' ");
                    }
                    else if(MinTerm[3]==7)
                    {
                       printf("The Simplfied Expression is A'B'+A'BC'+ABC ");
                    }
                }
                else if(MinTerm[2]==3)
                {
                    if(MinTerm[3]==4)
                    {
                       printf("The Simplfied Expression is  B'C'+A'C ");
                    }
                    else if(MinTerm[3]==5)
                    {
                       printf("The Simplfied Expression is A'B'+A'C+B'C ");
                    }
                    else if(MinTerm[3]==6)
                    {
                       printf("The Simplfied Expression is  A'B'+A'C+ABC' ");
                    }
                    else if(MinTerm[3]==7)
                    {
                       printf("The Simplfied Expression is A'B'+BC ");
                    }
                }
                else if(MinTerm[2]==4)
                {
                    if(MinTerm[3]==5)
                    {
                       printf("The Simplfied Expression is B' ");
                    }
                    else if(MinTerm[3]==6)
                    {
                       printf("The Simplfied Expression is A'B'+AC' ");
                    }
                    else if(MinTerm[3]==7)
                    {
                       printf("The Simplfied Expression is B'C'+A'B'+ABC ");
                    }
                }
                else if(MinTerm[2]==5)
                {
                     if(MinTerm[3]==6)
                    {
                       printf("The Simplfied Expression is B'C+A'B'+ABC' ");
                    }
                    else if(MinTerm[3]==7)
                    {
                       printf("The Simplfied Expression is A'B'+AC ");
                    }
                }
                else if(MinTerm[2]==6)
                {
                    if(MinTerm[3]==7)
                    {
                       printf("The Simplfied Expression is A'B'+AB ");
                    }
                }
            }
            else if(MinTerm[1]==2)
            {
                if(MinTerm[2]==3)
                {
                    if(MinTerm[3]==4)
                    {
                        printf("The Simplfied Expression is B'C'+A'B ");
                    }
                    else if(MinTerm[3]==5)
                    {
                        printf("The Simplfied Expression is A'B+AB'C+A'B'C' ");
                    }
                    else if(MinTerm[3]==6)
                    {
                        printf("The Simplfied Expression is A'C'+A'B+BC' ");
                    }
                    else if(MinTerm[3]==7)
                    {
                        printf("The Simplfied Expression is A'C'+BC ");
                    }
                }
                else if(MinTerm[2]==4)
                {
                    if(MinTerm[3]==5)
                    {
                        printf("The Simplfied Expression is A'C'+AB' ");
                    }
                    else if(MinTerm[3]==6)
                    {
                        printf("The Simplfied Expression is C' ");
                    }
                    else if(MinTerm[3]==7)
                    {
                        printf("The Simplfied Expression is A'C'+B'C'+ABC ");
                    }
                }
                else if(MinTerm[2]==5)
                {
                    if(MinTerm[3]==6)
                    {
                        printf("The Simplfied Expression is A'C'+BC'+AB'C ");
                    }
                    else if(MinTerm[3]==7)
                    {
                        printf("The Simplfied Expression is A'C'+AC ");
                    }
                }
                else if(MinTerm[2]==6)
                {
                   if(MinTerm[3]==7)
                    {
                        printf("The Simplfied Expression is A'C'+AB ");
                    }
                }
            }
            else if(MinTerm[1]==3)
            {
                if(MinTerm[2]==4)
                {
                    if(MinTerm[3]==5)
                    {
                        printf("The Simplfied Expression is B'C'+AB'+A'BC ");
                    }
                    else if(MinTerm[3]==6)
                    {
                        printf("The Simplfied Expression is B'C'+AC'+A'BC ");
                    }
                    else if(MinTerm[3]==7)
                    {
                        printf("The Simplfied Expression is B'C'+BC ");
                    }
                }
                else if(MinTerm[2]==5)
                {
                    if(MinTerm[3]==6)
                    {
                        printf("The Simplfied Expression is A'B'C'+A'BC+AB'C+ABC' ");
                    }
                    else if(MinTerm[3]==7)
                    {
                        printf("The Simplfied Expression is AC+A'B'C'+A'BC");
                    }
                }
                else if(MinTerm[2]==6)
                {
                    if(MinTerm[3]==7)
                    {
                        printf("The Simplfied Expression is AB+BC+A'B'C' ");
                    }
                }
            }
            else if(MinTerm[1]==4)
            {
                if(MinTerm[2]==5)
                {
                    if(MinTerm[3]==6)
                    {
                        printf("The Simplfied Expression is BC+AB'+AC' ");
                    }
                    else if(MinTerm[3]==7)
                    {
                        printf("The Simplfied Expression is AC+BC ");
                    }
                }
                else if(MinTerm[2]==6)
                {
                    if(MinTerm[3]==7)
                    {
                        printf("The Simplfied Expression is BC+AB ");
                    }
                }
            }
            else if(MinTerm[1]==5)
            {
                if(MinTerm[2]==6)
                {
                    if(MinTerm[3]==7)
                    {
                        printf("The Simplfied Expression is AC+AB+A'B'C' ");
                    }
                }
            }
        }
        else if(MinTerm[0]==1)
        {
            if(MinTerm[1]==2)
            {
                if(MinTerm[2]==3)
                {
                    if(MinTerm[3]==4)
                    {
                        printf("The Simplfied Expression is A'C+A'B+AB'C' ");
                    }
                    else if(MinTerm[3]==5)
                    {
                        printf("The Simplfied Expression is B'C+A'B ");
                    }
                    else if(MinTerm[3]==6)
                    {
                        printf("The Simplfied Expression is AC+BC'");
                    }
                    else if(MinTerm[3]==7)
                    {
                        printf("The Simplfied Expression is A'C+A'B+BC ");
                    }
                }
                else if(MinTerm[2]==4)
                {
                    if(MinTerm[3]==5)
                    {
                        printf("The Simplfied Expression is A'C+AB' ");
                    }
                    else if(MinTerm[3]==6)
                    {
                        printf("The Simplfied Expression is BC'+AC'+A'B'C  ");
                    }
                    else if(MinTerm[3]==7)
                    {
                        printf("The Simplfied Expression is A'B'C+A'BC'+AB'C+ABC ");
                    }
                }
                else if(MinTerm[2]==5)
                {
                    if(MinTerm[3]==6)
                    {
                        printf("The Simplfied Expression is B'C+BC' ");
                    }
                    else if(MinTerm[3]==7)
                    {
                        printf("The Simplfied Expression is AC+B'C+A'BC' ");
                    }
                }
                else if(MinTerm[2]==6)
                {
                   if(MinTerm[3]==7)
                    {
                        printf("The Simplfied Expression is BC'+AB+A'B'C ");
                    }
                }
            }
            else if(MinTerm[1]==3)
            {
                if(MinTerm[2]==4)
                {
                    if(MinTerm[3]==5)
                    {
                        printf("The Simplfied Expression is A'C+AB' ");
                    }
                    else if(MinTerm[3]==6)
                    {
                        printf("The Simplfied Expression is A'C+AB' ");
                    }
                    else if(MinTerm[3]==7)
                    {
                        printf("The Simplfied Expression is BC+A'C+AB'C' ");
                    }
                }
                else if(MinTerm[2]==5)
                {
                    if(MinTerm[3]==6)
                    {
                        printf("The Simplfied Expression is A'C+B'C+ABC' ");
                    }
                    else if(MinTerm[3]==7)
                    {
                        printf("The Simplfied Expression is C ");
                    }
                }
                else if(MinTerm[2]==6)
                {
                    if(MinTerm[3]==7)
                    {
                        printf("The Simplfied Expression is A'C+AB ");
                    }
                }
            }
            else if(MinTerm[1]==4)
            {
                if(MinTerm[2]==5)
                {
                    if(MinTerm[3]==6)
                    {
                        printf("The Simplfied Expression is B'C+AC' ");
                    }
                    else if(MinTerm[3]==7)
                    {
                        printf("The Simplfied Expression is B'C+AB'+AC ");
                    }
                }
                else if(MinTerm[2]==6)
                {
                    if(MinTerm[3]==7)
                    {
                        printf("The Simplfied Expression is AC'+AB+A'B'C ");
                    }
                }
            }
            else if(MinTerm[1]==5)
            {
                if(MinTerm[2]==6)
                {
                    if(MinTerm[3]==7)
                    {
                        printf("The Simplfied Expression is AB+BC' ");
                    }
                }
            }
        }
        else if(MinTerm[0]==2)
        {
            if(MinTerm[1]==3)
                {
                    if(MinTerm[2]==4)
                    {
                        if(MinTerm[3]==5)
                        {
                            printf("The Simplfied Expression is AB'+A'B ");
                        }
                        else if(MinTerm[3]==6)
                        {
                            printf("The Simplfied Expression is AC'+A'B ");
                        }
                        else if(MinTerm[3]==7)
                        {
                            printf("The Simplfied Expression is A'B+BC+AB'C' ");
                        }
                    }
                    else if(MinTerm[2]==5)
                    {
                        if(MinTerm[3]==6)
                        {
                            printf("The Simplfied Expression is BC'+AB+AB'C ");
                        }
                        else if(MinTerm[3]==7)
                        {
                            printf("The Simplfied Expression is AC+A'B ");
                        }
                    }
                    else if(MinTerm[2]==6)
                    {
                        if(MinTerm[3]==7)
                        {
                            printf("The Simplfied Expression is B ");
                        }
                    }
                }
                else if(MinTerm[1]==4)
                {
                    if(MinTerm[2]==5)
                    {
                        if(MinTerm[3]==6)
                        {
                            printf("The Simplfied Expression is BC'+AB' ");
                        }
                        else if(MinTerm[3]==7)
                        {
                            printf("The Simplfied Expression is AC+AB'+A'BC' ");
                        }
                    }
                    else if(MinTerm[2]==6)
                    {
                        if(MinTerm[3]==7)
                        {
                            printf("The Simplfied Expression is AC'+AB+BC' ");
                        }
                    }
                }
                else if(MinTerm[1]==5)
                {
                    if(MinTerm[2]==6)
                    {
                        if(MinTerm[3]==7)
                        {
                            printf("The Simplfied Expression is AC+BC' ");
                        }
                    }
                }
            }
            else if(MinTerm[0]==3)
            {
                if(MinTerm[1]==4)
                {
                    if(MinTerm[2]==5)
                    {
                        if(MinTerm[3]==6)
                        {
                            printf("The Simplfied Expression is AC'+AB'+A'BC ");
                        }
                        else if(MinTerm[3]==7)
                        {
                            printf("The Simplfied Expression is AB'+BC ");
                        }
                    }
                    else if(MinTerm[2]==6)
                    {
                         if(MinTerm[3]==7)
                        {
                            printf("The Simplfied Expression is BC+AC' ");
                        }
                    }
                }
                else if(MinTerm[1]==5)
                {
                    if(MinTerm[2]==6)
                    {
                        if(MinTerm[3]==7)
                        {
                            printf("The Simplfied Expression is AC+AB+BC ");
                        }
                    }
                }
            }
            else if(MinTerm[0]==4)
            {
                if(MinTerm[1]==5)
                {
                    if(MinTerm[2]==6)
                    {
                        if(MinTerm[3]==7)
                        {
                            printf("The Simplfied Expression is A ");
                        }
                    }
                }
            }
        }
    if(numMinTerms==5)
    {
    if(MinTerm[0]==0)
    {
        if(MinTerm[1]==1)
        {
            if(MinTerm[2]==2)
            {
                if(MinTerm[3]==3)
                {
                    if(MinTerm[4]==4)
                    {
                        printf("The Simplfied Expression is A'+B'C' ");
                    }
                    else if(MinTerm[4]==5)
                    {
                       printf("The Simplfied Expression is A'+B'C ");
                    }
                    else if(MinTerm[4]==6)
                    {
                       printf("The Simplfied Expression is A'+BC' ");
                    }
                    else if(MinTerm[4]==7)
                    {
                       printf("The Simplfied Expression is A'+BC ");
                    }
                }
                else if(MinTerm[3]==4)
                {
                    if(MinTerm[4]==5)
                    {
                       printf("The Simplfied Expression is B'+AC' ");
                    }
                    else if(MinTerm[4]==6)
                    {
                       printf("The Simplfied Expression is C'+A'B' ");
                    }
                    else if(MinTerm[4]==7)
                    {
                       printf("The Simplfied Expression is A'B'+A'C'+B'C'+BC ");
                    }
                }
                else if(MinTerm[3]==5)
                {
                    if(MinTerm[4]==6)
                    {
                       printf("The Simplfied Expression is B'C+BC'+A'B' ");
                    }
                    else if(MinTerm[4]==7)
                    {
                        printf("The Simplfied Expression is A'B'+A'C'+B'C+AC ");
                    }
                }
                else if(MinTerm[3]==6)
                {
                    if(MinTerm[4]==7)
                    {
                       printf("The Simplfied Expression is A'B'+BC'+AB ");
                    }  
                }
            }
            else if(MinTerm[2]==3)
            {
                if(MinTerm[3]==4)
                {
                    if(MinTerm[4]==5)
                    {
                       printf("The Simplfied Expression is B'+A'C ");
                    }
                    else if(MinTerm[4]==6)
                    {
                       printf("The Simplfied Expression is A'B'+A'C+B'C'+AC' ");
                    }
                    else if(MinTerm[4]==7)
                    {
                       printf("The Simplfied Expression is A'B'+A'C+B'C'+BC ");
                    }
                }
                else if(MinTerm[3]==5)
                {
                    if(MinTerm[4]==6)
                    {
                       printf("The Simplfied Expression is A'B'+A'C+B'C+ABC' ");
                    }
                    else if(MinTerm[4]==7)
                    {
                       printf("The Simplfied Expression is A'B'+A'C+AC ");
                    }
                }
                else if(MinTerm[3]==6)
                {
                    if(MinTerm[4]==7)
                    {
                       printf("The Simplfied Expression is A'B'+A'C+AB ");
                    }
                }
            }
            else if(MinTerm[2]==4)
            {
                if(MinTerm[3]==5)
                {
                    if(MinTerm[4]==6)
                    {
                       printf("The Simplfied Expression is B'+AC' ");
                    }
                    else if(MinTerm[4]==7)
                    {
                       printf("The Simplfied Expression is B'+AC ");
                    }
                }
                else if(MinTerm[3]==6)
                {
                    if(MinTerm[4]==7)
                    {
                       printf("The Simplfied Expression is A'B'+B'C'+AB ");
                    }
                }
            }
            else if(MinTerm[2]==5)
            {
                if(MinTerm[3]==6)
                {
                    if(MinTerm[4]==7)
                    {
                       printf("The Simplfied Expression is A'B'+B'C+AB ");
                    }
                }
            }
        }
        else if(MinTerm[1]==2)
        {
            if(MinTerm[2]==3)
            {
                if(MinTerm[3]==4)
                {
                    if(MinTerm[4]==5)
                    {
                        printf("The Simplfied Expression is B'C'+AB'+A'B ");
                    }
                    else if(MinTerm[4]==6)
                    {
                        printf("The Simplfied Expression is C'+A'B  ");
                    }
                    else if(MinTerm[4]==7)
                    {
                        printf("The Simplfied Expression is  B'C'+BC+A'C' ");
                    }
                }
                else if(MinTerm[3]==5)
                {
                    if(MinTerm[4]==6)
                    {
                        printf("The Simplfied Expression is A'C'+A'B+BC'+AB'C ");
                    }
                    else if(MinTerm[4]==7)
                    {
                        printf("The Simplfied Expression is A'C'+A'B+AC ");
                    }
                }
                else if(MinTerm[3]==6)
                {
                    if(MinTerm[4]==7)
                    {
                        printf("The Simplfied Expression is B+A'C' ");
                    }
                }
            }
            else if(MinTerm[2]==4)
            {
                if(MinTerm[3]==5)
                {
                    if(MinTerm[4]==6)
                    {
                        printf("The Simplfied Expression is C'+AB' ");
                    }
                    else if(MinTerm[4]==7)
                    {
                        printf("The Simplfied Expression is A'C'+B'C'+AC ");
                    }
                }
                else if(MinTerm[3]==6)
                {
                  if(MinTerm[4]==7)
                    {
                        printf("The Simplfied Expression is C'+AB ");
                    }  
                }
            }
            else if(MinTerm[2]==5)
                {
                    if(MinTerm[3]==6)
                    {
                        if(MinTerm[4]==7)
                        {
                            printf("The Simplfied Expression is A'C'+BC'+AB ");
                        }  
                    }
                }
        }
        else if(MinTerm[1]==3)
        {
            if(MinTerm[2]==4)
            {
                if(MinTerm[3]==5)
                {
                    if(MinTerm[4]==6)
                    {
                        printf("The Simplfied Expression is B'C'+AB'+AC'+A'BC ");
                    }
                    else if(MinTerm[4]==7)
                    {
                        printf("The Simplfied Expression is B'C'+AB'+BC ");
                    }
                }
                else if(MinTerm[3]==6)
                {
                    if(MinTerm[4]==7)
                    {
                        printf("The Simplfied Expression is B'C'+AB+BC ");
                    }  
                }
            }
            else if(MinTerm[2]==5)
            {
                if(MinTerm[3]==6)
                {
                    if(MinTerm[4]==7)
                    {
                        printf("The Simplfied Expression is BC+AC+AB+A'B'C' ");
                    }
                }
            }
        }
        else if(MinTerm[1]==4)
        {
            if(MinTerm[2]==5)
            {
                if(MinTerm[3]==6)
                {
                    if(MinTerm[4]==7)
                    {
                        printf("The Simplfied Expression is A+B'C' ");
                    }
                }
            }
        }
    }
    if(MinTerm[0]==1)
    {
        if(MinTerm[1]==2)
        {
            if(MinTerm[2]==3)
            {
                if(MinTerm[3]==4)
                {
                    if(MinTerm[4]==5)
                    {
                        printf("The Simplfied Expression is AB'+B'C+AB ");
                    }
                    else if(MinTerm[4]==6)
                    {
                        printf("The Simplfied Expression is AC+BC'+AC' ");
                    }
                    else if(MinTerm[4]==7)
                    {
                        printf("The Simplfied Expression is A'C+A'B+BC+AB'C' ");
                    }
                }
                else if(MinTerm[3]==5)
                {
                     if(MinTerm[4]==6)
                    {
                        printf("The Simplfied Expression is A'C+B'C+BC' ");
                    }
                    else if(MinTerm[4]==7)
                    {
                        printf("The Simplfied Expression is C+A'C' ");
                    }
                }
                else if(MinTerm[3]==6)
                {
                    if(MinTerm[4]==7)
                    {
                        printf("The Simplfied Expression is B+A'C ");
                    }
                }
            }
            else if(MinTerm[2]==4)
            {
                if(MinTerm[3]==5)
                {
                    if(MinTerm[4]==6)
                    {
                        printf("The Simplfied Expression is AB'+B'C+BC' ");
                    }
                    else if(MinTerm[4]==7)
                    {
                        printf("The Simplfied Expression is AB'+B'C+AC+A'BC'");
                    }
                }
                else if(MinTerm[3]==6)
                {
                    if(MinTerm[4]==7)
                    {
                        printf("The Simplfied Expression is  B'C'+AB+AC'+A'B'C ");
                    }
                }
            }
            else if(MinTerm[2]==5)
            {
                if(MinTerm[3]==6)
                {
                    if(MinTerm[4]==7)
                    {
                        printf("The Simplfied Expression is B'C+BC'+AB ");
                    }
                }
            }
        }
        else if(MinTerm[1]==3)
        {
            if(MinTerm[2]==4)
            {
                if(MinTerm[3]==5)
                {
                    if(MinTerm[4]==6)
                    {
                        printf("The Simplfied Expression is A'C+AB'+AC' ");
                    }
                    else if(MinTerm[4]==7)
                    {
                        printf("The Simplfied Expression is C+A'B  ");
                    }
                }
                else if(MinTerm[3]==6)
                {
                    if(MinTerm[4]==7)
                    {
                        printf("The Simplfied Expression is A'C+BC+AC' ");
                    }
                }
            }
            else if(MinTerm[2]==5)
            {
                if(MinTerm[3]==6)
                {
                    if(MinTerm[4]==7)
                    {
                        printf("The Simplfied Expression is C+AB  ");
                    }
                }
            }
        }
        else if(MinTerm[1]==4)
        {
            if(MinTerm[2]==5)
            {
                if(MinTerm[3]==6)
                {
                    if(MinTerm[4]==7)
                    {
                        printf("The Simplfied Expression is A+B'C ");
                    }
                }
            }
        }
    }
    else if(MinTerm[0]==2)
    {
        if(MinTerm[1]==3)
        {
            if(MinTerm[2]==4)
            {
                if(MinTerm[3]==5)
                {
                    if(MinTerm[4]==6)
                    {
                        printf("The Simplfied Expression is A'B+AB'+BC' ");
                    }
                    else if(MinTerm[4]==7)
                    {
                        printf("The Simplfied Expression is A'B+AB'+BC ");
                    }
                }
                else if(MinTerm[3]==6)
                {
                    if(MinTerm[4]==7)
                    {
                        printf("The Simplfied Expression is B+AC' ");
                    }
                }
            }
            else if(MinTerm[2]==5)
            {
                if(MinTerm[3]==6)
                {
                    if(MinTerm[4]==7)
                    {
                        printf("The Simplfied Expression is B+AC ");
                    }
                }
            }
        }
        if(MinTerm[1]==4)
        {
            if(MinTerm[2]==5)
            {
                if(MinTerm[3]==6)
                {
                    if(MinTerm[4]==7)
                    {
                        printf("The Simplfied Expression is A+BC' ");
                    }
                }
            }  
        }
    }
    else if(MinTerm[0]==3)
    {
        if(MinTerm[1]==4)
            {
            if(MinTerm[2]==5)
            {
                if(MinTerm[3]==6)
                {
                    if(MinTerm[4]==7)
                    {
                     printf("The Simplfied Expression is A+BC ");  
                    }
                }
            }
        }
    }
}
    if(numMinTerms==6)
    {
        if(MinTerm[0]==0)
        {
            if(MinTerm[1]==1)
            {
                if(MinTerm[2]==2)
                {
                    if(MinTerm[3]==3)
                    {
                        if(MinTerm[4]==4)
                        {
                            if(MinTerm[5]==5)
                            {
                                printf("The Simplfied Expression is A'+B' ");
                            }
                            else if(MinTerm[5]==6)
                            {
                                printf("The Simplfied Expression is A'+C' ");
                            }
                            else if(MinTerm[5]==7)
                            {
                                printf("The Simplfied Expression is A'+B'C'+BC ");
                            }
                        }
                        else if(MinTerm[4]==5)
                        {
                            if(MinTerm[5]==6)
                            {
                                printf("The Simplfied Expression is A'+B'C'+BC' ");
                            }
                            else if(MinTerm[5]==7)
                            {
                                printf("The Simplfied Expression is A'+C ");
                            }
                        }
                        else if(MinTerm[4]==6)
                        {
                            if(MinTerm[5]==7)
                            {
                                printf("The Simplfied Expression is A'+B ");
                            }
                        }
                    }
                    else if(MinTerm[3]==4)
                    {
                        if(MinTerm[4]==5)
                        {
                            if(MinTerm[5]==6)
                            {
                                printf("The Simplfied Expression is B'+C' ");
                            }
                            else if(MinTerm[5]==7)
                            {
                                printf("The Simplfied Expression is B'+AC+A'C' ") ;
                            }
                        }
                        else if(MinTerm[4]==6)
                        {
                           if(MinTerm[5]==7)
                            {
                                printf("The Simplfied Expression is C'+A'B'+AB ");
                            }
                        }
                    }
                    else if(MinTerm[3]==5)
                    {
                        if(MinTerm[4]==6)
                        {
                            if(MinTerm[5]==7)
                            {
                                printf("The Simplfied Expression is A'B'+BC'+AC ");
                            }
                        }
                    }
                }
                else if(MinTerm[2]==3)
                {
                    if(MinTerm[3]==4)
                    {
                        if(MinTerm[4]==5)
                        {
                            if(MinTerm[5]==6)
                            {
                                printf("The Simplfied Expression is B'+A'C+AC' ");
                            }
                            else if(MinTerm[5]==7)
                            {
                                printf("The Simplfied Expression is B'+C ");
                            }
                        }
                        else if(MinTerm[4]==6)
                        {
                            if(MinTerm[5]==7)
                            {
                                printf("The Simplfied Expression is A'B'+BC+AC' ");
                            }
                        }
                    }
                    else if(MinTerm[3]==5)
                    {
                        if(MinTerm[4]==6)
                        {
                            if(MinTerm[5]==7)
                            {
                                printf("The Simplfied Expression is C+A'B'+ABC' ");
                            }
                        }
                    }
                }
                if(MinTerm[2]==4)
                {
                    if(MinTerm[3]==5)
                    {
                        if(MinTerm[4]==6)
                        {
                            if(MinTerm[5]==7)
                            {
                                printf("The Simplfied Expression is A+B' ");
                            }
                        }
                    }
                }
            }
            else if(MinTerm[1]==2)
            {
                if(MinTerm[2]==3)
                {
                    if(MinTerm[3]==4)
                    {
                        if(MinTerm[4]==5)
                        {
                            if(MinTerm[5]==6)
                            {
                                printf("The Simplfied Expression is C'+A'B+AB' ");
                            }
                            else if(MinTerm[5]==7)
                            {
                                printf("The Simplfied Expression is B'C'+AC+A'B ");
                            }
                        }
                        else if(MinTerm[4]==6)
                        {
                            if(MinTerm[5]==7)
                            {
                                printf("The Simplfied Expression is B+C' ");
                            }
                        }
                    }
                    if(MinTerm[3]==5)
                    {
                        if(MinTerm[4]==6)
                        {
                            if(MinTerm[5]==7)
                            {
                                printf("The Simplfied Expression is B+AC'+AC ");
                            }
                        }
                    }
                }
                if(MinTerm[2]==4)
                {
                    if(MinTerm[3]==5)
                    {
                        if(MinTerm[4]==6)
                        {
                            if(MinTerm[5]==7)
                            {
                                printf("The Simplfied Expression is A+C' ");
                            }
                        }
                    }
                }
            }
            else if(MinTerm[1]==3)
            {
                if(MinTerm[2]==4)
                {
                    if(MinTerm[3]==5)
                    {
                        if(MinTerm[4]==6)
                        {
                            if(MinTerm[5]==7)
                            {
                                printf("The Simplfied Expression is A+B'C'+BC ");
                            }
                        }
                    }
                }
            }
        }
        else if(MinTerm[0]==1)
        {
            if(MinTerm[1]==2)
            {
                if(MinTerm[2]==3)
                {
                    if(MinTerm[3]==4)
                    {
                        if(MinTerm[4]==5)
                        {
                            if(MinTerm[5]==6)
                            {
                                printf("The Simplfied Expression is AB'+A'C+BC' ");
                            }
                            else if(MinTerm[5]==7)
                            {
                                printf("The Simplfied Expression is C+AB'+A'B ");
                            }
                        }
                        else if(MinTerm[4]==6)
                        {
                            if(MinTerm[5]==7)
                            {
                                printf("The Simplfied Expression is B+A'C+AC' ");
                            }  
                        }
                    }
                    else if(MinTerm[3]==5)
                    {
                        if(MinTerm[4]==6)
                        {
                            if(MinTerm[5]==7)
                            {
                                printf("The Simplfied Expression is B+C ");
                            }
                        }
                    }
                }
                else if(MinTerm[2]==4)
                {
                    if(MinTerm[3]==5)
                    {
                        if(MinTerm[4]==6)
                        {
                            if(MinTerm[5]==7)
                            {
                                printf("The Simplfied Expression is A+B'C+BC' ");
                            }
                        }
                    }
                }
            }
            else if(MinTerm[1]==3)
            {
               if(MinTerm[2]==4)
                {
                    if(MinTerm[3]==5)
                    {
                        if(MinTerm[4]==6)
                        {
                            if(MinTerm[5]==7)
                            {
                                printf("The Simplfied Expression is A+C ");
                            }
                        }
                    }
                }
            }
        }
        else if(MinTerm[0]==2)
        {
            if(MinTerm[1]==3)
            {
                if(MinTerm[2]==4)
                {
                    if(MinTerm[3]==5)
                    {
                        if(MinTerm[4]==6)
                        {
                            if(MinTerm[5]==7)
                            {
                                printf("The Simplfied Expression is A+B ");
                            }
                        }
                    }
                }
            }
        }
    }
    if(numMinTerms==7)
    {
        if(MinTerm[0]==0)
        {
            if(MinTerm[1]==1)
            {
                if(MinTerm[2]==2)
                {
                    if(MinTerm[3]==3)
                    {
                        if(MinTerm[4]==4)
                        {
                            if(MinTerm[5]==5)
                            {  
                                if(MinTerm[6]==6)
                                {
                                    printf("The Simplfied Expression is A'+B'+BC' ");    
                                }
                                else if(MinTerm[6]==7)
                                {
                                   printf("The Simplfied Expression is B'+C+A'C' ");  
                                }
                            }
                            else if(MinTerm[5]==6)
                            {
                                if(MinTerm[6]==7)
                                {
                                   printf("The Simplfied Expression is B+C'+A'B' ");  
                                }
                            }
                        }
                        else if(MinTerm[4]==5)
                        {
                            if(MinTerm[5]==6)
                            {
                                if(MinTerm[6]==7)
                                {
                                   printf("The Simplfied Expression is B+C+A'B' ");  
                                }
                            }
                        }
                    }
                    else if(MinTerm[3]==4)
                    {
                        if(MinTerm[4]==5)
                        {
                            if(MinTerm[5]==6)
                            {
                               if(MinTerm[6]==7)
                                {
                                   printf("The Simplfied Expression is B'+C'+AC ");  
                                }
                            }
                        }
                    }
                }
                else if(MinTerm[2]==3)
                {
                   if(MinTerm[3]==4)
                    {
                        if(MinTerm[4]==5)
                        {
                            if(MinTerm[5]==6)
                            {
                               if(MinTerm[6]==7)
                                {
                                   printf("The Simplfied Expression is B'+C+AB ");  
                                }
                            }
                        }
                    }
                }
            }
            else if(MinTerm[1]==2)
            {
                if(MinTerm[2]==3)
                {
                   if(MinTerm[3]==4)
                    {
                        if(MinTerm[4]==5)
                        {
                            if(MinTerm[5]==6)
                            {
                               if(MinTerm[6]==7)
                                {
                                   printf("The Simplfied Expression is B+C'+AB' ");  
                                }
                            }
                        }
                    }
                }
            }
        }
        else if(MinTerm[0]==1)
        {
            if(MinTerm[1]==2)
            {
                if(MinTerm[2]==3)
                {
                   if(MinTerm[3]==4)
                    {
                        if(MinTerm[4]==5)
                        {
                            if(MinTerm[5]==6)
                            {
                               if(MinTerm[6]==7)
                                {
                                   printf("The Simplfied Expression is B+C+AB' ");  
                                }
                            }
                        }
                    }
                }
            }
        }
    }
    if(numMinTerms==8)
    {
        printf("The Simplfied Expression is 1 ");
    }
   
    }

int main() {
    int f;

    printf("ENTER THE K MAP YOU REQUIRE:\n");
    printf("1. 2 VARIABLE K-MAP\n2. 3 VARIABLE K-MAP\n");
    scanf("%d", &f);

    switch (f) {
        case 1: {
            twoVariable();
            break;
        }

        case 2: {
            threeVariable();
            break;
        }

      

        default: {
            printf("Invalid choice!\n");
            break;
        }
    }

    return 0;
}
