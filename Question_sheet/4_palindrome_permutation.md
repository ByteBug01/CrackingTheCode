**4.  givrn a string, Check if characters of a given string can be rearranged to form a palindrome**

```c++
#include<bits/stdc++.h>
using namespace std;

bool pp(string str){
    int count[no_of_chars]={0};
    for(int i=0; str[i]; i++){
        count[str[i]]++;
    }
int odd = 0;
for(int i=0; i<no_of_chars; i++){
    if(count[i]&1)
    odd++;

    if(odd>1)
return false;
}
return true;

}

int main()
{
    pp("geeksogeeks")? cout<<"yes\n"; : cout<<"no\n;

    return 0;
}
```
> Time Complexity: O(n)