# How to get the range of acceptable value of arithmetic types.

```numeric_limits``` from ```limits``` can be used to get the acceptable minimum, maximum numbers of the arithmetic types.

```c++
#include<iostream>
#include<limits>

using namespace std;

int main()
{
	// integer range
	cout << "int : " << (numeric_limits<int>::min()) <<
				" to " <<
				(numeric_limits<int>::max()) << "\n";  

	// long range
	cout << "long : " << (numeric_limits<long>::min()) <<
				" to " <<
				(numeric_limits<long>::max()) << "\n";  

	// unsigned long range
	cout << "unsigned long : " <<
				(numeric_limits<unsigned long>::min()) <<
				" to " <<
				(numeric_limits<unsigned long>::max()) << "\n";

	return 0;
}
```
##### Output

```bash
$ ./a.out
int : -2147483648 to 2147483647
long : -9223372036854775808 to 9223372036854775807
unsigned long : 0 to 18446744073709551615
```
