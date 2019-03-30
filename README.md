#include"header.h"

void allmarkshow(){
int i;

FILE *mark= fopen("markinfo.txt", "r");
FILE *fp= fopen("info.txt", "r");

printf(" ======================================================================================================");
printf("\n Roll\t\tCourse1\t\tCourse2\t\tCourse3\t\tCourse4\t\tCourse5\t\tCourse6\n");
printf(" ======================================================================================================\n\n");
for(i=0; i<3; i++){

    /*fgets(student[i].name, 22, fp);
    fgets(student[i].address, 82, fp);
    fgets(student[i].roll, 10, fp);
    fscanf(fp,"%d\n", &student[i].reg);
    */
    //fgets(mark, "%s", &student[i].roll);
    fscanf(mark, "%s\t%lf\t%lf\t%lf\t%lf\t%lf\t%lf\n",&student[i].roll, &student[i].mark1, &student[i].mark2, &student[i].mark3,&student[i].mark4,&student[i].mark5,&student[i].mark6);

    printf(" %s\t%.2lf\t\t%.2lf\t\t%.2lf\t\t%.2lf\t\t%.2lf\t\t%.2lf\n", student[i].roll, student[i].mark1, student[i].mark2, student[i].mark3, student[i].mark4, student[i].mark4, student[i].mark5, student[i].mark6);

}



}
