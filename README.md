#include<stdio.h>
#include<string.h>
#include <locale.h>

int main(){
    FILE *file = fopen("work.txt", "w");
    setlocale(LC_ALL, "Rus");
    char line1 [200] = "Вышел ёжик из тумана222,";
    char line2 [200] = "Вынул ножик из карман3а.";
    //char str[500];

    if (file != NULL){
            fputs (line1, file);
            fputs( "\n", file);
            fputs (line2, file);
            fputs( "\n", file);
            fputs((strcat (line1, line2)), file);


    }
    fclose(file);

    return 0;

}
