## 8.1 IO库
## 8.2 文件输入输出
## 8.3 string流

**笔记:**
> C++引入了`ostringstream、istringstream、stringstream`这三个类，要使用他们创建对象就必须包含<sstream>这个头文件。istringstream类用于执行C++风格的串流的输入操作。ostringstream类用于执行C风格的串流的输出操作。strstream类同时可以支持C风格的字符串流的输入输出操作。istringstream的构造函数原形如下：`istringstream::istringstream(string str)`;它的作用是从string对象str中读取字符。`通过上述可推出ostringstream、stringstream类的功能`

关于istringstream类的例子
```cpp
  #include <sstream>
#include <iostream>
#include <string>
using namespace std;
int main()
{
    int a, b, c;
    string s;

    getline(cin, s);
    istringstream ss(s);
    ss >> a >> b >> c;
    cout << "a:" << a << " b:" << b << " c:" << c << endl;

    return 0;
}
```