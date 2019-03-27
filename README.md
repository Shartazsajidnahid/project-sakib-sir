#include<stdio.h>
#include<stdlib.h>
#include"header.h"

void outputinfo()
{
    printf("\n____________________________________________\n");
    int i,n;

    FILE *fp;
    fp= fopen("info.txt", "r");



    printf("\n\n\t***Here are the profiles of all students:***");

    for(i=0; i<3; i++)
    {

        printf("\n\n  Profile of student %d:\n\n",i+1);
        fscanf(fp, "%s\t%s\t%s\t%d\n", &student[i].name, &student[i].address, &student[i].roll, &student[i].reg);
        printf("\tName   : %s\n\tAddress: %s\n\tRoll   : %s\n\tReg    : %d\n", student[i].name,student[i].address, student[i].roll, student[i].reg);
    }
    fclose(fp);

    printf("\n\n**All the inputs were shown!**");


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

