** 2. Given two strings check if one is permutaion of other **

```c++
#include<iostream>
using namespace std;

bool areAnagram(string s1, string s2){
//if two strings are permutation of each other then they are anagram.

vector<int> frq(26, 0); //space in vector is 26 and each has value 0
for(char c: s1){ frq[c-'a']++; }
for(char c: s2){ frq[c-'a']--; }

for(int i: frq)
{
    if(i!=0)
    {
        return false;
    }
}
return true;
} 
```
>Time Complexity : O(n)