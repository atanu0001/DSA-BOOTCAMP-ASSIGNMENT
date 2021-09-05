# DSA-BOOTCAMP-ASSIGNMENT

##### Q1. Write a program to Swap to two numbers.
##### Ans:
```
#include <iostream>
using namespace std;

int main()
{
    int a = 5, b = 10, temp;

    cout << "Before swapping." << endl;
    cout << "a = " << a << ", b = " << b << endl;

    temp = a;
    a = b;
    b = temp;

    cout << "\nAfter swapping." << endl;
    cout << "a = " << a << ", b = " << b << endl;

    return 0;
}
```

##### Q2. Write a program to find the largest number among three numbers entered by the user.
##### Ans:
```
#include <iostream>
using namespace std;

int main() {    
    float n1, n2, n3;

    cout << "Enter three numbers: ";
    cin >> n1 >> n2 >> n3;

    if(n1 >= n2 && n1 >= n3)
        cout << "Largest number: " << n1;

    if(n2 >= n1 && n2 >= n3)
        cout << "Largest number: " << n2;
    
    if(n3 >= n1 && n3 >= n2)
        cout << "Largest number: " << n3;
  
    return 0;
}
```

##### Q3. Write a program to check whether a year entered by a user is Leap year or not.
##### Ans:
```
#include <iostream>
using namespace std;

int main() {
    int year;

    cout << "Enter a year: ";
    cin >> year;

    if (year % 4 == 0) {
        if (year % 100 == 0) {
            if (year % 400 == 0)
                cout << year << " is a leap year.";
            else
                cout << year << " is not a leap year.";
        }
        else
            cout << year << " is a leap year.";
    }
    else
        cout << year << " is not a leap year.";

    return 0;
}
```

##### Q4. Write a program to display Fibonacci Series upto nth term. (Using loops)
##### Ans:
```
#include <iostream>
using namespace std;

int main() {
    int n, t1 = 0, t2 = 1, nextTerm = 0;

    cout << "Enter the number of terms: ";
    cin >> n;

    cout << "Fibonacci Series: ";

    for (int i = 1; i <= n; ++i) {
        // Prints the first two terms.
        if(i == 1) {
            cout << t1 << ", ";
            continue;
        }
        if(i == 2) {
            cout << t2 << ", ";
            continue;
        }
        nextTerm = t1 + t2;
        t1 = t2;
        t2 = nextTerm;
        
        cout << nextTerm << ", ";
    }
    return 0;
}
```

##### Q5. Write a program to check whether a number is Prime or Not.
##### Ans:
```
#include <iostream>
using namespace std;

int main() {
    int i, n;
    bool isPrime = true;

    cout << "Enter a positive integer: ";
    cin >> n;

    // 0 and 1 are not prime numbers
    if (n == 0 || n == 1) {
        isPrime = false;
    }
    else {
        for (i = 2; i <= n / 2; ++i) {
            if (n % i == 0) {
                isPrime = false;
                break;
            }
        }
    }
    if (isPrime)
        cout << n << " is a prime number";
    else
        cout << n << " is not a prime number";

    return 0;
}
```

##### Q6. Print this pattern using loops
##### For n=5
```
      *
     * *
    * * *
   * * * *
  * * * * *
```
##### Ans:
```
#include <iostream>
using namespace std;
 
// Function to demonstrate printing pattern
void triangle(int n)
{
    // number of spaces
    int k = 2 * n - 2;
 
    // Outer loop to handle number of rows
    // n in this case
    for (int i = 0; i < n; i++) {
 
        // Inner loop to handle number spaces
        // values changing acc. to requirement
        for (int j = 0; j < k; j++)
            cout << " ";
 
        // Decrementing k after each loop
        k = k - 1;
 
        // Inner loop to handle number of columns
        // values changing acc. to outer loop
        for (int j = 0; j <= i; j++) {
            // Printing stars
            cout << "* ";
        }
 
        // Ending line after each row
        cout << endl;
    }
}
 
// Driver Code
int main()
{
    int n = 5;
   
      // Function Call
    triangle(n);
    return 0;
}
```

##### Q7. Write a program that takes n elements from the user and displays the second largest element of an array.
##### Ans:
```
#include <iostream>
using namespace std;
int main(){
   int n, num[50], largest, second;
   cout<<"Enter number of elements: ";
   cin>>n;
   for(int i=0; i<n; i++){
      cout<<"Enter Array Element"<<(i+1)<<": ";
      cin>>num[i];
   }
   
   if(num[0]<num[1]){ 
      largest = num[1];
      second = num[0];
   }
   else{ 
      largest = num[0];
      second = num[1];
   }
   for (int i = 2; i< n ; i ++) {
     
      if (num[i] > largest) {
         second = largest;
         largest = num[i];
      }
      
      else if (num[i] > second && num[i] != largest) {
         second = num[i];
      }
   }
   cout<<"Second Largest Element in array is: "<<second;
   return 0;
}
```

##### Q8. https://www.hackerrank.com/challenges/array-left-rotation/problem
##### Ans:
```
#include <iostream>
using namespace std;

int main()
{
	int n,d;

	//input value of n and d
	cout<<"Enter the value of n and d"<<endl;
	cin>>n>>d;
	int a[n];

	//input array elements
	cout<<"enter the array elements : ";
	for(int i=0;i<n;i++)
	{
		cin>>a[i];
	}

	//print the elements of array after rotation
	cout<<"array elements after rotation : ";
	for(int i=0;i<n;i++)
	{
		cout<<a[(i+d)%n]<<" ";
	}

	return 0;
}
```

##### Q9. https://www.hackerrank.com/challenges/grading/problem
##### Ans:
```
#include <map>
#include <set>
#include <list>
#include <cmath>
#include <ctime>
#include <deque>
#include <queue>
#include <stack>
#include <string>
#include <bitset>
#include <cstdio>
#include <limits>
#include <vector>
#include <climits>
#include <cstring>
#include <cstdlib>
#include <fstream>
#include <numeric>
#include <sstream>
#include <iostream>
#include <algorithm>
#include <unordered_map>

using namespace std;


int main(){
    int n;
    cin >> n;
    for(int a0 = 0; a0 < n; a0++){
        int grade;
        cin >> grade;
        if (grade >= 38) {
            int rem = grade % 5;
            if (rem >= 3) grade += 5 - rem;
        }
        cout << grade << endl;
    }
    return 0;
}
```

##### Q10. https://www.hackerrank.com/challenges/camelcase/problem
##### Ans:
```
#include <map>
#include <set>
#include <list>
#include <cmath>
#include <ctime>
#include <deque>
#include <queue>
#include <stack>
#include <string>
#include <bitset>
#include <cstdio>
#include <limits>
#include <vector>
#include <climits>
#include <cstring>
#include <cstdlib>
#include <fstream>
#include <numeric>
#include <sstream>
#include <iostream>
#include <algorithm>
#include <unordered_map>

using namespace std;


int main(){
    string s;
    cin >> s;
    int t=1;
    for (int i=0;i<s.length();i++)
        if (isupper(s[i]))
        t++;
        cout<<t<<endl;
    return 0;
}
```
