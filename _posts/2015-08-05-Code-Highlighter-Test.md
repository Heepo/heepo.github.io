---
layout: post
title: Code Highlighter 测试
categories: 技术
tags: C/C++ 算法 OJ Jekyll
---
对输入的 n 个数进行排序并输出

输入：输入的第一行包括一个整数 n(1<=n<=100)。接下来的一行包括 n 个整数  
输出：可能有多组测试数据,对于每组数据,将排序后的 n 个整数输出,每个数后面都有一个空格。每组测试数据的结果占一行  
样例输入：4  
1432  
样例输出：1234  

{% highlight C++ linenos %}
#include <stdio.h>
  
int main () {
  int n;
  int buf[100]; //定义buf[100]来保存将要排序的数字
  while (scanf ("%d",&n) != EOF) { //多组数据输入
    for (int i = 0;i < n;i ++) {
      scanf ("%d",&buf[i]);
    } //输入待排序数字
    for (int i = 0;i < n;i ++) {
      for (int j = 0;j < n - 1 - i;j ++) {
        if (buf[j] > buf[j + 1]) {
          int tmp = buf[j];
          buf[j] = buf[j + 1];
          buf[j + 1] = tmp;
        }
      }
    } //冒泡排序主体
    for (int i = 0;i < n;i ++) {
      printf("%d ",buf[i]);
    } //输出完成排序后的数字,每个数字后都添加一个空格
    printf("\n"); //输出换行
  }
  return 0; 
}
{% endhighlight %}