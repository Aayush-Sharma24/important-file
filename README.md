#include <stdio.h>

int main() {
    char name[50],section[15], roll_no[50];

    printf("===== Contact Form =====\n");

    printf("Enter your name: ");
    fgets(name, sizeof(name), stdin);

    printf("Enter your section: ");
    fgets(section, sizeof(section), stdin);

    printf("Enter your roll no: ");
    fgets(roll_no, sizeof(roll_no), stdin);

    

    FILE *file = fopen("contact_data.txt", "a"); // append mode
    if (file == NULL) {
        printf("Error opening file!\n");
        return 1;
    }

    fprintf(file, "Name: %s", name);
    fprintf(file, "section: %s", section);
    fprintf(file, "roll_no: %s", roll_no);
    
    fprintf(file, "-------------------------------\n");

    fclose(file);

    printf("\n Abe ja jake kuch padh le warna fail ho jayega \n");

    return 0;
}
