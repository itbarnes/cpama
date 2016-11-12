## 选择语句

### 01
```
#include <stdio.h>

int main() {
    int num;
    printf("Enter a number:\n");
    scanf("%4d", &num); //不超过4位

    if (num >= 0 && num < 10) {
        printf("The number %d has 1 digits\n", num);
    } else if (num >= 10 && num < 100) {
        printf("The number %d has 2 digits\n", num);
    } else if (num >= 100 & num < 1000) {
        printf("The number %d has 3 digits\n", num);
    } else {
        printf("The number %d has 4 digits\n", num);
    }
}
```

### 02
#include <stdio.h>

int main() {
    int hour, minute;
    char *flag = "AM";
    printf("Enter a 24-hour time:\n");
    scanf("%2d:%2d", &hour, &minute);

    if(hour < 0 || hour > 23 || minute < 0 || minute > 59) {
        printf("Entered a wrong time.\n");
        return 0;
    }

    if(hour > 12) {
        hour -= 12;
        flag = "PM";
    }

    printf("Equivalent 12-hour time is: %d:%.2d %s\n", hour, minute, flag);
}
```

### 07
```
#include <stdio.h>

int _max(int a, int b);

int _min(int a, int b);

int main() {
    int a, b, c, d;
    int max, min;

    printf("Enter four integers:\n");
    scanf("%d%d%d%d", &a, &b, &c, &d);

    max = _max(_max(_max(a, b), c), d);
    min = _min(_min(_min(a, b), c), d);

    printf("Largest is : %d\nSmallest is %d\n", max, min);
}

int _max(int a, int b) {
    return a > b ? a : b;
}

int _min(int a, int b) {
    return a > b ? b : a;
}
```

### 10
```
#include <stdio.h>

int main() {
    int score, grade;
    printf("Enter numerical grade:\n");
    scanf("%d", &score);

    if (score < 0 || score > 100) {
        printf("Entered a wrong number.\n");
        return 0;
    }

    grade = score / 10;

    switch (grade) {
        case 0:
        case 1:
        case 2:
        case 3:
        case 4:
        case 5:
            printf("Letter grade: F\n");
            break;
        case 6:
            printf("Letter grade: D\n");
            break;
        case 7:
            printf("Letter grade: C\n");
            break;
        case 8:
            printf("Letter grade: B\n");
            break;
        case 9:
        case 10:
            printf("Letter grade: A\n");
        default:
            break;

    }

}

```



