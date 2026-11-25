#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int main() {
    int number, guess;
    int attempts = 0;

    srand(time(NULL));
    number = rand() % 100 + 1;

    printf("===== NUMBER GUESSING GAME =====\n");
    printf("ทายตัวเลขระหว่าง 1 - 100\n");

    while (1) {
        printf("\nกรอกตัวเลข: ");
        scanf("%d", &guess);

        attempts++;

        if (guess < number) {
            printf("มากกว่านี้!\n");
        }
        else if (guess > number) {
            printf("น้อยกว่านี้!\n");
        }
        else {
            printf("\nยินดีด้วย! คุณทายถูกแล้ว 🎉\n");
            printf("จำนวนครั้งที่ทาย: %d\n", attempts);
            break;
        }
    }

    return 0;
}
