**牛客-Applese 的回文串**

[链接]: https://ac.nowcoder.com/acm/problem/22350

```c++
#include<bits/stdc++.h>
using namespace std;
const int maxn = 1e5+7;
char s[maxn];
bool isPal(int l,int r){
	for(int i=l,j=r;i<j;i++,j--){
		if(s[i]!=s[j])
			return false;
	}
	return true;
}
int main(){
	cin>>s;
	int size = strlen(s);
	for(int i=0,j=size-1;i<j;i++,j--){
		if(s[i]!=s[j]){
			if(isPal(i,j-1) || isPal(i+1,j)){
				cout<<"Yes";
				return 0;
			}
			cout<<"No";
			return 0;
		}
	}
	cout<<"Yes";
    
	return 0;
} 
```

