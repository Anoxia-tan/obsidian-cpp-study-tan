C++中的仿函数（Functor）是一种特殊的对象，它可以像函数一样被调用，但实际上是一个类的实例。仿函数可以通过重载函数调用运算符 operator() 来实现，从而使得该对象可以像函数一样被调用。仿函数主要用于在算法中作为操作符使用，例如在STL（标准模板库）中的各种算法中。通过使用仿函数，可以将操作抽象出来，使得算法更加灵活，可以适用于不同的数据类型或者自定义的操作。
```c++
#include <iostream>

// 定义一个加法仿函数
class AddFunctor {
public:
    int operator()(int a, int b) {
        return a + b;
    }
};

int main() {
    AddFunctor adder;  // 创建仿函数对象

    int result = adder(3, 5);  // 使用仿函数调用
    std::cout << "Result:" << result << std::endl;

    return 0;
}
```