#include<stdio.h>
#include<stdlib.h>
#include"header.h"

void markinput(){

    printf("\n    =======================================\n");

FILE *mark;
FILE *fp;
fp=fopen("info.txt", "r");
mark=fopen("markinfo.txt", "w");

int i;

for(i=0; i<3; i++){

    printf("\n\n");
    fgets(student[i].name, 22, fp);
    fgets(student[i].address, 82, fp);
    fscanf(fp, "%s\n", &student[i].roll);
    //fgets(student[i].roll, 10, fp);
    fscanf(fp,"%d\n", &student[i].reg);

    printf(" \tName : %s \tRoll : %s\n",student[i].name, student[i].roll );

    printf(" \tEnter mark of course 1: ");
    scanf("%lf", &student[i].mark1);

    printf(" \tEnter mark of course 2: ");
    scanf("%lf", &student[i].mark2);

    printf(" \tEnter mark of course 3: ");
    scanf("%lf", &student[i].mark3);

    printf(" \tEnter mark of course 4: ");
    scanf("%lf", &student[i].mark4);

    printf(" \tEnter mark of course 5: ");
    scanf("%lf", &student[i].mark5);

    printf(" \tEnter mark of course 6: ");
    scanf("%lf", &student[i].mark6);

    //fprintf(mark, "%s", student[i].roll);
    fprintf(mark, "%s\t%lf\t%lf\t%lf\t%lf\t%lf\t%lf\n",student[i].roll,  student[i].mark1, student[i].mark2,student[i].mark3,student[i].mark4,student[i].mark5,student[i].mark6);


}
fclose(fp);
fclose(mark);



}

