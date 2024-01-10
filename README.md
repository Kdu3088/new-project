# new-project
indiana codes
#include <stdio.h>

int main() {
    FILE *file;
    char ch;

    file = fopen("book.txt", "r");
    if (file == NULL) {
        printf("Cannot open file \n");
        return 0;
    }

    ch = fgetc(file);
    while (ch != EOF) {
        putchar(ch);
        ch = fgetc(file);
    }

    fclose(file);
    return 0;
}
