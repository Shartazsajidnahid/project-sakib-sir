#include<stdio.h>
#include<stdlib.h>
#include"header.h"

void main()
{

    int i;

    printf("\n\tFor all profiles press 1.\n");
    printf("\tFor input press 2.\n");
    printf("\tTo analaize, press 3\n\n");
    printf("\tEnter your choice: ");
    scanf("%d", &i);


    if(i==3) searchinfo();
    if(i==2) inputinfo();
    if(i==1) outputinfo();


}
