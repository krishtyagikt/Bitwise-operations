# Bitwise-operations

```c++
#include <bits/stdc++.h>
using namespace std ;

string to_binary(int x) 
{
	string s;
	while(x > 0) 
	{
		s += (x % 2 ? '1' : '0');
		x /= 2;
	}
	reverse(s.begin(), s.end());
	return s;
}

int main() 
{
	cout << "user-defined fucntion to_binary : 13 = " << to_binary(13) << endl; // 1101
	cout << "using pre-defined : bitsets  : 13 = " << bitset<8>(13) << endl ; // 00001101  (padding of additional 0 bits at the starting.
	
	int x = 53;
	int y = 28;
	cout << "x = " << to_binary(x) << ", y = " << to_binary(y) << endl;
	
	cout << "AND, OR, XOR:" << endl;
	cout << to_binary(x & y) << " " << to_binary(x | y) << " " << to_binary(x ^ y) << endl;
}
```
