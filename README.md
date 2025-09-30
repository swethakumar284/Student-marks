#include <stdio.h>

struct Student {
    char name[50];
    int rollNo;
    float marks[5];
    float total;
    float average;
};

int main() {
    struct Student s;
    int i;

    // Input student details
    printf("Enter student name: ");
    scanf("%s", s.name);
    printf("Enter roll number: ");
    scanf("%d", &s.rollNo);

    // Input marks for 5 subjects
    s.total = 0;
    for (i = 0; i < 5; i++) {
        printf("Enter marks for subject %d: ", i + 1);
        scanf("%f", &s.marks[i]);
        s.total += s.marks[i];
    }

    // Calculate average
    s.average = s.total / 5;

    // Output result
    printf("\n--- Student Result ---\n");
    printf("Name: %s\n", s.name);
    printf("Roll No: %d\n", s.rollNo);
    printf("Total Marks: %.2f\n", s.total);
    printf("Average Marks: %.2f\n", s.average);

    return 0;
}