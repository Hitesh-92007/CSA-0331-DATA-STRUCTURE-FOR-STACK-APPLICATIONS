#include <stdio.h>

int main()
{
    int arr[8] = {98, 23, 45, 14, 6, 67, 33, 42};
    int i, j, key, k;

    for (i = 1; i < 8; i++)
    {
        key = arr[i];
        j = i - 1;

        while (j >= 0 && arr[j] > key)
        {
            arr[j + 1] = arr[j];
            j--;
        }
        arr[j + 1] = key;

        /* 6th iteration (i = 5) */
        if (i == 5)
        {
            for (k = 0; k < 8; k++)
            {
                printf("%d", arr[k]);
                if (k < 7)
                    printf(",");
            }
            break;
        }
    }

    return 0;
}
