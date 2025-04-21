# user-input-
#include <stdio.h>

void insertionsort(int arr[], int n) {
    for(int i = 1; i < n; ++i) {
        int key = arr[i];
        int j = i - 1;

        while(j >= 0 && arr[j] > key) {
            arr[j + 1] = arr[j];
            j--;
        }
        arr[j + 1] = key;
    }
}

int main() {
    int b[5];
    int i;

    printf("Enter 5 numbers:\n");
    for(i = 0; i < 5; i++) {
        scanf("%d", &b[i]);
    }

    insertionsort(b, 5);

    printf("Sorted numbers:\n");
    for(i = 0; i < 5; i++) {
        printf("%d ", b[i]);
    }

    return 0;
}
