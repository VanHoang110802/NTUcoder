> Link: https://thptchuyen.ntucoder.net/Problem/Details/4514

Cho 2 số nguyên a,b. Viết chương trình in ra 2 số nguyên x, y biểu diễn phân số $\frac{a}{b}$ dưới dạng tối giản, chú ý ta quy ước phân số $\frac{x}{y}$ tối giản khi gcd(x, y) = 1 và y > 0. In ra ERROR nếu b = 0.

Dữ liệu:

-  Một dòng ghi hai số nguyên a, b là số nguyên 64 - bit.

Kết quả:

-  Một dòng ghi 2 số nguyên x, y hoặc xâu ERROR
---
input
```
10 2
```
---
output
```
5 1
```
---
```cpp
#include<bits/stdc++.h>
using namespace std;
long long x, y;
void XuLyNhanh()
{
    ios_base::sync_with_stdio(false);
    cin.tie(0); cout.tie(0);
}

void GiaiBai()
{
    cin >> x >> y;
    if (y == 0) cout << "ERROR";
    else
    {
        long long u = x / (__gcd(x, y)), v = y / (__gcd(x, y));
        if (u > 0 && v < 0)
        {
            u = -u;
            v = -v;
        }
        cout << u << " " << v;
    }
}

int main()
{
    XuLyNhanh();
    GiaiBai();
    return 0;
}
    
```
