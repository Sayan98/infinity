# infinity
arbitrary precision integer arithmetic

## usage

1. Build `libInteger.a` using `make all` in the `src` directory.
2. Copy the `Integer.h` and file to your project.
3. Include `Integer.h` in your source file.
4. Compile with `-L$(LIB)` and `-lInteger` flags where `LIB` is the directory where `libInteger.a` resides in.


## tests

Run `make test` in the `src` directory to compile the sanity checks. Execute the generated executable with `./test.out`.


## example

```cpp
#include <iostream>
#include "Integer.h"

int main() {
    Integer a("199999999999999999999999999999999999999999999999");
    Integer b("999999999999999999999999999999999999999999999999");
    Integer c = -319879352;
    Integer d ("-141241241241");

    // Integers
    std::cout << "a :: " << a;
    std::cout << "b :: " << b;
    std::cout << "c :: " << c;
    std::cout << "d :: " << d;

    // logical ops
    std::cout << "a <= b :: " << (a <= b) << std::endl;
    std::cout << "a < b :: " << (a < b) << std::endl;
    std::cout << "a >= b :: " << (a >= b) << std::endl;
    std::cout << "a > b :: " << (a > b) << std::endl;
    std::cout << "a == b :: " << (a == b) << std::endl;
    std::cout << "a != b :: " << (a != b) << std::endl;

    // arithmetic ops
    std::cout << "-a :: " << -a;
    std::cout << "a + b :: " << a + b;
    std::cout << "a - b :: " << a - b;
    std::cout << "a * b :: " << a * b;
    std::cout << "a / b :: " << a / b;

    return 0;
}
```

## warning
This a pet project to explore arbitrary precision integers. If you need arbitrary precision arithmetic, consider using something more mature like [GMP](https://gmplib.org).


## author
Sayan Goswami (c) 2018


