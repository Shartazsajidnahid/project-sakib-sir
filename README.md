#include<stdio.h>
#include<stdlib.h>

void inputinfo();
void outputinfo();
void searchinfo();
void searchbyroll();
void searchbybatch();

struct input
{
    char name[22], address[82], roll[10];
    int reg, mark;
};

struct input student[140];
