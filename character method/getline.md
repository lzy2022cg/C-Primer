**面向行的输入: getline()**
> getline是定义在string头文件中的一个函数，该函数读取一行(可以接受空格)，通过回车确定结尾，并摒弃掉换行符。

getline有两种常用的方法
- 读入带有空格的字符串格式为 getline(cin,对应字符串指针）
```cpp
#include<bits/stdc++.h>
using namespace std;

string a;
int main(){
	getline(cin,a);//输入一个含有空格的字符串
	//int lena=a.length();  //求输入长度（包含空格）
	return 0;
}
```
- 输入带有空格的字符一维数组格式为 cin.getline(字符指针，字符个数）
```cpp
#include<bits/stdc++.h>
using namespace std;

const int maxn=105;
char a[maxn];
int main(){
	cin.getline(a,20);//输入一个含有空格的字符数组
	return 0;
}
```
- 如果是二位数组该怎嘛办？？很简单，就是在一位数组的代码上加循环行数即可。
```cpp
#include<bits/stdc++.h>
using namespace std;

const int maxn=105;
char a[maxn][maxn];
int main(){
	for(int i=0;i<20;i++)cin.getline(a[i],21);//输入一个含有空格的字符数组 
	//注意cin.getline(a[i],21);读入的是a[i][0~19]位。
	return 0;
}
```
