```cpp
// GNU G++20 11.2.0 (64 bit, winlibs)
#include <iostream>
#include <cmath>

using namespace std;

int countSteps (int x, int n){
    if(n==1) {
        return x;
    } else {
        return floor(x/n) + countSteps(x%n, n-1);
    }
}

int main()
{        
    int x, n;
    std::cin >> x;
    std::cout<<countSteps(x,5);
    return 0;
}
```
