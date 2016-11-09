## C语言基本概念

### 1
```c
#include <stdio.h>

int main(void) {
    printf("       *\n");
    printf("      * \n");
    printf("     *  \n");
    printf("*   *   \n");
    printf(" * *    \n");
    printf("  *     \n");

    return 0;
}
```

### 2

```c
#include <stdio.h>
#define PI 3.14;

int main(void) {
    int radius = 10;
    float area;

    area = 4.0f / 3 * radius * radius * radius * PI;    //预定义放在结尾处
    printf("area is %.2f \n", area);

    return 0;
}
```

### 3
```c
#include <stdio.h>
#define PI 3.14;

int main(void) {
    float radius;
    float area;

    printf("plz input the radius.. \n");
    scanf("%f", &radius);

    area = 4.0f / 3 * radius * radius * radius * PI;    //预定义放在结尾处
    printf("area is %.2f \n", area);

    return 0;
}
```

### 4

```c
#include <stdio.h>
#define TAX_RATE 0.05;

int main(void) {
    float amount;
    float total;

    printf("Enter an amount: \n");
    scanf("%f", &amount);

    if(amount <= 0) {
        printf("error number \n");
        return 0;
    }

    total = amount + amount * TAX_RATE;

    printf("With tax added: $%.2f \n", total);

    return 0;
}
```

### 5

```c
#include <stdio.h>

float compute(float num);
float _pow(float num, int square);

int main(void) {
    float num;
    printf("Enter a number... \n");
    scanf("%f", &num);

    printf("Result is : %.2f\n", compute(num));

    return 0;
}

float compute(float num) {
    float result;
    result = 3 * _pow(num, 5) + 2 * _pow(num, 4) - 5 * _pow(num, 3) - _pow(num, 2) + 7 * num - 6;

    return result;
}

float _pow(float num, int square) {
    if (square < 0) {
        float base = num;
        for (int i = 0; i < (-1 * square - 1); i++) {
            base *= num;
        }

        return 1 / base;
    } else if (square == 0) {
        return 1;
    } else {
        float total = num;
        for (int i = 0; i < square - 1; i++) {
            total *= num;
        }

        return total;
    }
}
```

### 6
```c
#include <stdio.h>

float compute(float num);

int main(void) {
    float num;
    printf("Enter a number... \n");
    scanf("%f", &num);

    printf("Result is : %.2f\n", compute(num));

    return 0;
}

float compute(float num) {
    return ((((3 * num + 2) * num - 5) * num - 1) * num + 7) * num - 6;
}
```

### 7

```c
#include <stdio.h>

int main(void) {
    int total, num_20, num_10, num_5, num_1;
    printf("Enter a dollar amount:\n");
    scanf("%d", &total);

    if (total < 0) {
        printf("error amount...\n");
        return 0;
    }

    num_20 = total / 20;
    num_10 = (total - num_20 * 20) / 10;
    num_5 = (total - num_20 * 20 - num_10 * 10) / 5;
    num_1 = total - num_20 * 20 - num_10 * 10 - num_5 * 5;

    printf("$20 bills: %d\n$10 bills: %d\n$5 bills: %d\n$1 bills: %d\n", num_20, num_10, num_5, num_1);

    return 0;
}
```

### 8
```c
#include <stdio.h>

#define MONTH_OF_YEAR 12

int main(void) {
    float loan_amount, interest_rate, payment_per_month, interest_rate_per_month;
    float af_first, af_second, af_third;

    printf("Enter amount of loan:\n");
    scanf("%f", &loan_amount);

    printf("Enter interest rate:\n");
    scanf("%f", &interest_rate);

    printf("Enter monthly payment:\n");
    scanf("%f", &payment_per_month);

    if (loan_amount < 0 || interest_rate < 0 || payment_per_month < 0 || loan_amount < payment_per_month) {
        printf("ur input has something wrong ...\n");
        return 0;
    }

    interest_rate_per_month = interest_rate / 100 / MONTH_OF_YEAR;

    af_first = loan_amount - payment_per_month + loan_amount * interest_rate_per_month;
    af_second = af_first - payment_per_month + af_first * interest_rate_per_month;
    af_third = af_second - payment_per_month + af_second * interest_rate_per_month;

    printf("Balance remaining after first payment: $%.2f\n", af_first);
    printf("Balance remaining after second payment: $%.2f\n", af_second);
    printf("Balance remaining after third payment: $%.2f\n", af_third);

    return 0;
}
```
