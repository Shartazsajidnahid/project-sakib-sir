#include<stdio.h>
#include<stdlib.h>
#include"header.h"

void inputinfo()
{
    printf("\n____________________________________________\n");
    int i,n;

    FILE *fp;
    fp= fopen("info.txt", "w");

    for(i=0; i<3; i++)
    {

        printf("\nFor student %d:\n", i+1);
        fflush(stdin);

        printf("Enter name: ");
        gets(student[i].name);
        fflush(stdin);

        printf("Enter address: ");
        gets(student[i].address);
        fflush(stdin);

        printf("Enter roll: ");
        gets(student[i].roll);
        fflush(stdin);

        printf("Enter reg: ");
        scanf("%d", &student[i].reg);

        fprintf(fp, "%s\t%s\t%s\t%d\n", student[i].name, student[i].address, student[i].roll, student[i].reg);
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
