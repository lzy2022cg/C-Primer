## 8.1 IO库
## 8.2 文件输入输出
## 8.3 string流

**笔记:**
> C++引入了`ostringstream、istringstream、stringstream`这三个类，要使用他们创建对象就必须包含<sstream>这个头文件。istringstream从string读取数据，ostringstream向string写入数据，stringstream既可以从string读取数据，也可以向string写数据。istringstream的构造函数原形如下：`istringstream::istringstream(string str)`;它的作用是从string对象str中读取字符。`注意可以这样理解，将istringstream和ostingstream看作是内存，这样 istringstream& >> &string可以看作string从内存读取内容，ostringstream& << &string可以看作将内容写入到内存`
### stringstream特有的操作
| 操作 | 解释 |
| ----------- | ----------- |
|`sstream strm` | 定义一个未绑定的`stringstream`对象 |
| `sstream strm(s)` | 用`s`初始化对象 |
| `strm.str()` | 返回`strm`所保存的`string`的拷贝 |
| `strm.str(s)` | 将`s`拷贝到`strm`中，返回`void` |
| sstream | strm是一个未绑定的stringstream对象。sstream |

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
- istringstream 输入流
```cpp
string s,as;
istringstream ss(s);
ss>>as;
```
- ostringstream 输出流
```cpp
ostringstream sss(s);//string s中数据拷贝到sss流中
sss<<'1';//覆盖式写入，若原来为qwe,写入后为1we
cout<<sss.str();//输出流里面的东西
```
