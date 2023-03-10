**Determine if a string has all Unique Characters**

 1st Approach

```c++
#include<bits/stdc++.h>
using namespace std;

bool uniqueChar(string str){

    sort(str.begin(), str.end());

for(int i=0; i<str.length()-1>; i++)
{
    if(str[i]==str[i+1])
    return false;
}
return true;
}

int main(){
    string s;
    cout<<"enter the string\n";
    cin>>s;

    if (uniqueChar(str)) {
        cout << "The String " << str
             << " has all unique characters\n";
    }
    else {
 
        cout << "The String " << str
             << " has duplicate characters\n";
    }
}


```
>time complexity: O(nlogn)


2nd Approach

```c++
const int MAX_CHAR=256;
bool uniqueChar(string str){
if(str.length()> MAX_CHAR){
    return false;
}
bool chars[MAX_CHAR]={0};
for(int i=0; i<str.length()-1; i++){
    if(chars[int(str[i])]==true)
    return false;

chars[int(str[i])]=true;
}
return true;
}
```

>Time complexity: O(n)