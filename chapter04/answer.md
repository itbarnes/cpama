## 表达式

### 01
```c
#include <stdio.h>

int main() {
    int x, y, num;
    printf("Enter a two-digit number:\n");
    scanf("%d", &num);

    if (num < 10 || num > 99) {
        printf("Entered wrong number.\n");
        return 0;
    }

    x = num / 10;
    y = num - 10 * x;

    printf("The reversal is: %d\n", 10 * y + x);

    return 0;
}
```

### 02
```c
#include <stdio.h>

int main() {
    int x, y, z, num;
    printf("Enter a three-digit number:\n");
    scanf("%d", &num);

    if (num < 100 || num > 999) {
        printf("Entered wrong number.\n");
        return 0;
    }

    x = num / 100;
    y = (num - 100 * x) / 10;
    z = num - 100 * x - 10 * y;

    printf("The reversal is: %d\n", 100 * z + 10 * y + x);

    return 0;
}
```

### 03
```c
#include <stdio.h>

int main() {
    int x, y, z;

    printf("Enter a three-digit number:\n");
    scanf("%1d%1d%d", &x, &y, &z);  //%1d 仅匹配一位整数

    printf("The reversal is: %d%d%d\n", z, y, x);

    return 0;
}
```
### 04
```c
#include <stdio.h>
int number;

int main() {
    int arr[5] = {0, 0, 0, 0, 0};
    int index = 0;

    printf("Enter a number between 0 and 32767:\n");
    scanf("%d", &number);

    while (number != 0) {
        int temp = number;
        number /= 8;
        arr[index] = temp - 8 * number;
        index++;
    }

    printf("In octal, your number is: %d%d%d%d%d\n", arr[4], arr[3], arr[2], arr[1], arr[0]);

    return 0;
}
```



















