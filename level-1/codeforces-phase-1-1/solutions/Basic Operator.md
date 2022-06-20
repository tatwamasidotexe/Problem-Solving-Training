# 617 A
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
# 546 A
``` cpp
// GNU G++20 11.2.0 (64 bit, winlibs)
#include <iostream>
#include <cmath>

using namespace std;

int calcTotal (int w, int k){
    int sum = 0;
    for(int i = 1; i <=w; i++) {
        sum+= i*k;
    }
    return sum;
}

int main()
{        
    int k, n, w;
    std::cin >> k >> n >> w;
    int total = calcTotal(w,k);
    if(total > n) {
        std::cout<<total - n;
    } else {
        std::cout<<0;
    }
    return 0;
}
```

# 151 A
``` cpp
// GNU G++20 11.2.0 (64 bit, winlibs)

// CODEFORCES 151-A

#include <iostream>

using namespace std;

int main()
{        
    int n, k, l, c, d, p, nl, np;

    while(std::cin>>n >> k >> l >> c >> d >> p >> nl >> np){
        // these are all the max drinks/slices/salt divisions we can have
        int total_drinks = (k*l)/nl;
        int total_slices = c*d;
        int total_salt = p/np;

        int res = min(min(total_drinks, total_salt), total_slices)/n;
        std::cout<< res;
    }
    
    return 0;
}
```
