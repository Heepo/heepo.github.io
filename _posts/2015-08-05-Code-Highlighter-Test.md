---
layout: post
title: Code Highlighter 测试
categories: 技术 OJ
tags: C/C++ 算法
---
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