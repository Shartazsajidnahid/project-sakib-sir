#include<stdio.h>
#include<stdlib.h>
#include"header.h"

void searchbyroll();

void searchinfo()
{
    printf("\n____________________________________________\n");
    int x;

    printf("\n If you want to search a roll, press 1.\n");
    printf(" To get profiles of a batch, press 2.\n");
    printf("\n Enter your choice: ");
    scanf("%d", &x);

    if(x==1) searchbyroll();
    if(x==2) searchbybatch();

}
