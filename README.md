# FILE-HANDLING-PROGRAM

*COMPANY* : CODTECH IT SOLUTIONS

*NAME* : PUNEET VASHISTH

*INTERN ID* : CT04DG757

*DOMIAN* : C PROGRAMMING

*DURATION* : 4 WEEKS

*MENTOR* : NEELA SANTOSH

*I USE VS CODE*
THE CODE IS :

#include <stdio.h>
#include <stdlib.h>

void create_and_write_file(const char *filename) {
    FILE *fp = fopen(filename, "w"); // "w" mode creates/truncates the file
    if (fp == NULL) {
        perror("Error creating/writing file");
        exit(1);
    }
    fprintf(fp, "This is the initial content of the file.\n");
    fclose(fp);
    printf("File created and initial content written.\n");
}

void read_file(const char *filename) {
    FILE *fp = fopen(filename, "r"); // "r" mode for reading
    char ch;

    if (fp == NULL) {
        perror("Error reading file");
        exit(1);
    }

    printf("Reading file contents:\n");
    while ((ch = fgetc(fp)) != EOF) {
        putchar(ch);
    }
    fclose(fp);
}

void append_to_file(const char *filename) {
    FILE *fp = fopen(filename, "a"); // "a" mode for appending
    if (fp == NULL) {
        perror("Error opening file for appending");
        exit(1);
    }
    fprintf(fp, "This is appended content.\n");
    fclose(fp);
    printf("Data appended to file.\n");
}

int main() {
    const char *filename = "sample.txt";

    create_and_write_file(filename);
    read_file(filename);

    append_to_file(filename);
    read_file(filename);

    return 0;
}

*OUTPUT*
<img width="409" height="156" alt="Image" src="https://github.com/user-attachments/assets/1b9d2f8e-a42f-45fa-b585-78ab73a52153" />
