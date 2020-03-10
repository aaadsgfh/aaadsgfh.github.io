# [🏠](https://aaadsgfh.github.io/)vector类
## 基础了解：[¶](https://aaadsgfh.github.io/Blogs/vector.html#基础了解)
vector类是STL的一个模板类,是一个向量,可理解为可变长的数组

vector包含在头文件vector中:
```cpp
#include<vector>
```
## 定义方式：[¶](https://aaadsgfh.github.io/Blogs/vector.html#定义方式)
如果要创建int型的vector对象,创建如下:
```cpp
vector<int> v;
```
模板如下( _operator_ 类型的叫 _name_ 的对象):
```cpp
vector<operator> name;
```
定义方法还有很多种:
```cpp
1. vector<int> a(10);   //定义了10个整型元素的向量，但没有给出初值，其值不确定
2. vector<int> a(10,1); //定义了10个整型元素的向量,且每个元素的初值为1
3. vector<int> a(b);    //用b向量来创建a向量，整体复制性赋值
4. vector<int> a(b.begin(),b.begin()+3);
                        //定义了a值为b中第0个(包含)到第2个(包含)元素
5. int b[7]={1,2,1,6,5,9,8};
   vector<int> a(b,b+7);//从数组中获得初值
```
## 使用方法：[¶](https://aaadsgfh.github.io/Blogs/vector.html#使用方法)
用"."运算符使用其方法:
```cpp
1. v.assign(a.begin(),a.begin()+4);
   //把向量a的前0~3位赋值给v
2. v.assign(4,2);
   //使v只含4个元素，且每个元素为2
3. v.back();
   //返回v的最后一个元素
4. v.front();
   //返回v的第一个元素
5. v[i];
   //返回v的第i个元素，当且仅当v[i]存在
6. v.clear();
   //清空v中的元素
7. v.empty();
   //判断v是否为空，空则返回ture,不空则返回false
8. v.pop_back();
   //删除v向量的最后一个元素
9. v.erase(a.begin()+1,v.begin()+3);
   //删除v中第1个(从第0个算起)到第2个元素
   //即删除的元素从v.begin()+1算起(包括)一直到v.begin()+3(不包括)
10.v.push_back(5);
   //在v的最后一个向量后插入一个元素，其值为5
11.v.insert(v.begin()+1,5);
   //在v的第1个元素的位置插入数值5
   //如v为1,2,3,4,插入元素后为1,5,2,3,4
12.v.insert(v.begin()+1,3,5);
   //在v的第1个元素的位置插入3个数,其值都为5
13.v.insert(v.begin()+1,b+3,b+6);
   //数组b,在v的第1个元素的位置插入b的第3个元素到第5个元素(不包括b+6)
   //如b为1,2,3,4,5,9,8,插入元素后为1,4,5,9,2,3,4,5,9,8
14.v.size();
   //返回v中元素的个数
15.v.capacity();
   //返回v在内存中总共可以容纳的元素个数
16.v.resize(10);
   //将v的现有元素个数调至10个,多则删,少则补,其值随机
17.v.resize(10,2);
   //将v的现有元素个数调至10个,多则删,少则补,其值为2
18.v.reserve(100);
   //将v的容量(capacity)扩充至100
   //也就是说现在测试v.capacity();的时候返回值是100
   //这种操作只有在需要给v添加大量数据的时候才显得有意义
   //因为这将避免内存多次容量扩充操作(当v的容量不足时电脑会自动扩容，当然这必然降低性能)
19.v.swap(b);
   //将v中的元素和向量b中的元素进行整体性交换
20.v==b;
   //b为向量，向量的比较操作还有!=,>=,<=,>,<
```
## To be continued...
