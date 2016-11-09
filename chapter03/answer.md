## 格式化输入/输出

### 01
```c
#include <stdio.h>

int main(void) {
    int year, month, day;

    printf("Enter a date (mm/dd/yyyy):\n");
    scanf("%d/%d/%d", &month, &day, &year);

    printf("%d%.2d%.2d\n", year, month, day);  //%.2d 如果输入一位整数，前面会补0

    return 0;
}
```

### 02
```c
#include <stdio.h>

int main(void) {
    int number;
    float price;
    char date[11];

    printf("Enter item number:\n");
    scanf("%d", &number);

    printf("Enter unit price:\n");
    scanf("%f", &price);

    printf("Enter purchase date (mm/dd/yyyy):\n");
    scanf("%s", date);

    printf("%-12d$%12.2f%12s\n", number, price, date);
    return 0;
}
```

### 03
```c
#include <stdio.h>
int main(void) {
    int prefix, id, code, item_number, check_digit;
    printf("Enter ISBN:\n");
    scanf("%d-%d-%d-%d-%d", &prefix, &id, &code, &item_number, &check_digit);

    printf("GS1 prefix: %d\nGroup id: %d\nPublisher code: %d\nItem number: %d\nCheck digit: %d\n",
           prefix, id, code, item_number, check_digit);

    return 0;
}
```