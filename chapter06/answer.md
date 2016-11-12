## 循环

### 01
```
#include <stdio.h>

int main() {
    float max = 0, temp;

    for(;;) {
        printf("Enter a number:\n");
        scanf("%f", &temp);

        if( temp <= 0) {
            printf("The largest number entered is : %f", max);
            return 0;
        }

        if( temp > max) {
            max = temp;
        }
    }
}
```

### 02
```
#include <stdio.h>

int m, n;

int main() {

    printf("Enter two integers: \n");
    scanf("%d%d", &m, &n);

    if (0 == n) {
        printf("Greatest common divider is %d\n", m);
        return 0;
    }

    while (n != 0) {
        int mod = m % n;
        m = n;
        n = mod;
    }

    printf("Greatest common divider is %d\n", m);
    return 0;
}
```

