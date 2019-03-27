#include<stdio.h>
#include<stdlib.h>
#include"header.h"

void searchbybatch()

{
    printf("____________________________________________\n");
        int a,b,i,x,y,j=0,n;
        printf("\n Enter the batch no: (example: 11, 06...)\n");
        scanf("%d",&a);
        b=a%10;
        a/=10;
        FILE *fp= fopen("info.txt", "r");
        printf("\n\n");
        for(i=0; i<3; i++)
        {

            fscanf(fp, "%s\t%s\t%s\t%d\n", &student[i].name, &student[i].address, &student[i].roll, &student[i].reg);
            x=student[i].roll[4]-48;
            y=student[i].roll[5]-48;

            if(x==a && y==b)
            {
            printf("Student no %d\n", j+1);
            printf("\tName   : %s\n\tAddress: %s\n\tRoll   : %s\n\tReg    : %d\n\n", student[i].name,student[i].address, student[i].roll, student[i].reg);
            j++;
            }
        }

        fclose(fp);
lab:
    printf("\n\n\tTo go to menu, press 0\n\telse to exit, press 1.\n\n");

    printf("\tEnter your choice: ");
    scanf("%d", &n);
    if(n==0) menu();
    else if (n==1) return 0;
    else
    {
        printf(" wrong input, lets try again.\n");
        goto lab;
    }


}
