#include<stdio.h>
#include<stdlib.h>
#include"header.h"

void searchbyroll(){

printf("\n____________________________________________\n");
char roll[10];
int i,j,n,  count=0;
FILE *fp;
fp= fopen("info.txt", "r");

printf("\n Enter the roll: ");

scanf("%s", roll);

printf("\n\n Here is the profile of the student you're looking for:\n\n");
for(i=0; i<3; i++){
    count=0;
    fscanf(fp, "%s\t%s\t%s\t%d\n", &student[i].name, &student[i].address, &student[i].roll, &student[i].reg);

    for(j=0; j<8; j++){
        if(roll[j]==student[i].roll[j]) count++;
    }

    if(count==8){
        printf("\tName   : %s\n\tAddress: %s\n\tRoll   : %s\n\tReg    : %d\n", student[i].name,student[i].address, student[i].roll, student[i].reg);
    }
}





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
