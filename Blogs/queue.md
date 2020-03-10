# [🏠](https://aaadsgfh.github.io/)queue类
## 基础了解：[¶](https://aaadsgfh.github.io/Blogs/queue.html#基础了解)

queue类是STL的一个模板类,队列,是一种先进先出(FIFO)的数据结构,读音和Q类似

queue包含在头文件queue中:
```cpp
#include<queue>
```

## 定义方式：[¶](https://aaadsgfh.github.io/Blogs/queue.html#定义方式)

```cpp
queue<int> Q;
```
即
```cpp
queue<operator> name;
```

## 使用方法：[¶](https://aaadsgfh.github.io/Blogs/queue.html#使用方法)

```cpp
1. Q.empty();
   //返回队列是否为空
2. Q.size();
   //返回当前队列长度
3. Q.front();
   //返回当前队列的第一个元素
4. Q.back();
   //返回当前队列的最后一个元素
5. Q.push();
   //在队列后面插入一个元素, 比如插入数字5:Q.push(5)
6. Q.pop();
   //从当前队列里,移出第一个元素
```

## 代码示例：[¶](https://aaadsgfh.github.io/Blogs/queue.html#代码示例)

```cpp
#include <iostream>
#include <queue>

using namespace std;
int main()
{
	queue<int> Q;
	cout<<"queue empty?  "<<Q.empty()<<endl;

	for(int i=0;i<5;i++)
		Q.push(i);	      //进队
    
	cout<<"queue empty?  "<<Q.empty()<<endl;
	cout<<"queue size:   "<<Q.size()<<endl;
    cout<<endl;

    for(int i=0;i<5;i++)
    { 
    	cout<<"queue front:  "<<Q.front()<<endl;    
        Q.pop();      //出队
    }
    return 0;
}
```
