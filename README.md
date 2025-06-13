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
    Start[Format Specifiers]

    Start --> D_int[%d]
    D_int -->|Used In| PrintD1[printf()]
    D_int -->|Used In| ScanD1[scanf()]
    D_int -->|For| TypeInt[int]

    Start --> F_float[%f / %.2f]
    F_float --> PrintF[printf()]
    F_float --> ScanF[scanf()]
    F_float --> TypeFloat[float]

    Start --> LF_double[%lf]
    LF_double --> ScanLF[scanf()]
    LF_double --> TypeDouble[double]

    Start --> C_char[%c]
    C_char --> PrintC[printf()]
    C_char --> ScanC[scanf()]
    C_char --> TypeChar[char]

    Start --> S_string[%s]
    S_string --> PrintS[printf()]
    S_string --> ScanS[scanf()]
    S_string --> TypeStr[string (char[])]

    Start --> U_uint[%u]
    U_uint --> PrintU[printf()]
    U_uint --> ScanU[scanf()]
    U_uint --> TypeUInt[unsigned int]

    Start --> LD_long[%ld]
    LD_long --> PrintLD[printf()]
    LD_long --> ScanLD[scanf()]
    LD_long --> TypeLong[long int]

    Start --> LLD_llong[%lld]
    LLD_llong --> PrintLLD[printf()]
    LLD_llong --> ScanLLD[scanf()]
    LLD_llong --> TypeLLong[long long int]

    Start --> X_hex[%x / %X]
    X_hex --> PrintX[printf()]
    X_hex --> TypeHex[Hexadecimal]

    Start --> O_octal[%o]
    O_octal --> PrintO[printf()]
    O_octal --> TypeOctal[Octal]

    Start --> Percent[%%]
    Percent --> PrintPerc[printf()]
    Percent --> TypePerc[Print % symbol]
```
