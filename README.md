# C-Programming_Docs
# 📘 C Language Format Specifiers (for `printf` and `scanf`)

In C programming, format specifiers are used in functions like `printf()` and `scanf()` to tell the compiler the type of data being handled.

---

## 🧾 Format Specifier Table

| Format Specifier | Data Type           | Example (Print)         | Usage Purpose             |
|------------------|---------------------|--------------------------|---------------------------|
| `%d`             | `int`               | `printf("%d", num);`     | Integer                   |
| `%f`             | `float`             | `printf("%f", pi);`      | Float                     |
| `%.2f`           | `float`             | `printf("%.2f", pi);`    | Float (2 decimal places)  |
| `%lf`            | `double`            | `scanf("%lf", &d);`      | Double input (`%f` in `printf`) |
| `%c`             | `char`              | `printf("%c", ch);`      | Character                 |
| `%s`             | `char[]` (string)   | `printf("%s", str);`     | String                    |
| `%u`             | `unsigned int`      | `printf("%u", num);`     | Unsigned Integer          |
| `%ld`            | `long int`          | `printf("%ld", n);`      | Long Integer              |
| `%lld`           | `long long int`     | `printf("%lld", n);`     | Long Long Integer         |
| `%x` / `%X`      | Hexadecimal         | `printf("%x", num);`     | Hexadecimal format        |
| `%o`             | Octal               | `printf("%o", num);`     | Octal format              |
| `%%`             | Percent Symbol      | `printf("%%");`          | Prints `%`                |

---

## 🔁 Example Code (Print & Input)

```c
#include <stdio.h>

int main() {
    int a = 10;
    float b = 3.14;
    char ch = 'A';
    char str[10] = "Hello";

    // Print
    printf("%d\n", a);
    printf("%f\n", b);
    printf("%c\n", ch);
    printf("%s\n", str);

    // Input
    scanf("%d", &a);
    scanf("%f", &b);
    scanf(" %c", &ch);  // Note: space before %c
    scanf("%s", str);   // No '&' needed for strings

    return 0;
}
```
```mermaid
graph TD
    A[Format Specifiers] --> B[%d]
    A --> C[%f / %.2f]
    A --> D[%lf]
    A --> E[%c]
    A --> F[%s]
    A --> G[%u]
    A --> H[%ld]
    A --> I[%lld]
    A --> J[%x / %X]
    A --> K[%o]
    A --> L[%%]

    B --> B1[int]
    C --> C1[float]
    D --> D1[double]
    E --> E1[char]
    F --> F1[string (char[])]
    G --> G1[unsigned int]
    H --> H1[long int]
    I --> I1[long long int]
    J --> J1[hexadecimal]
    K --> K1[octal]
    L --> L1[percent symbol]
```
