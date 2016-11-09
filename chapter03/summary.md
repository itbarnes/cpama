## 格式化输入输出

### printf

> printf(格式串, 表达式1, 表达式2, ...), 表达式数量和类型必须与格式串中占位符数量和格式匹配, 否则报错.  
> 转换说明, %m.pX 或者 %-m.pX, `-`表示左对齐, 默认右对齐. m表示最小字段宽度, 如果数字长度小于m则空格补齐, 否则正常显示, 不会截断.  
> 转换说明符X, d表示十进制整数, f表示十进制浮点数, e表示指数形式的浮点数, g表示指数形式或者十进制浮点数形式.  

### scanf

> 格式转换说明符和printf一致.  
> scanf会忽略空白符, 包括空格、换行符和水平垂直制表符等.  
> 当scanf函数遇到一个不可能属于当前项的字符序列时, 会把当前字符放回原处, 供下一个扫描项使用  

```c
#include <stdio.h>

int main(void) {
    int i, j;
    float x, y;

    printf("input sth...\n");   //1-20.3-4.0e3 •
    scanf("%d%d%f%f", &i, &j, &x, &y);

    printf("i: %d\nj: %d\nx: %.2f\ny: %.2f\n", i, j, x, y);

    return 0;
}
```
```shell
gcc main.c
./a.out
input sth...
1-20.3-4.0e3
i: 1
j: -20
x: 0.30
```

