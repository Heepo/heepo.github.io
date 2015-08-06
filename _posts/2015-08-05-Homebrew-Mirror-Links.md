---
layout: post
title: Homebrew镜像源
categories: 工具
tags: Homebrew 镜像源
---
替换homebrew默认源为国内镜像源  

方法一  
{% highlight Bash %}
$ cd /usr/local
$ git remote set-url origin git://mirrors.tuna.tsinghua.edu.cn/homebrew.git
$ brew update
{% endhighlight %}
如果速度还是很慢，可以尝试以下操作，然后重试update
{% highlight bash %}
$ cd ~/tmp
$ git clone git://mirrors.tuna.tsinghua.edu.cn/homebrew.git
$ rm -rf /usr/local/.git
$ rm -rf /usr/local/Library
$ cp -R homebrew/.git /usr/local/
$ cp -R homebrew/Library /usr/local/
{% endhighlight %}
使用homebrew-science
{% highlight bash %}
$ cd /usr/local/Library/Taps/homebrew/homebrew-science
$ git remote set-url origin git://mirrors.tuna.tsinghua.edu.cn/homebrew-science.git
$ brew update  
{% endhighlight %}  
或者homebrew-python
{% highlight bash %}
$ cd /usr/local/Library/Taps/homebrew/homebrew-python
$ git remote set-url origin git://mirrors.tuna.tsinghua.edu.cn/homebrew-python.git
$ brew update
{% endhighlight %} 
方法二
{% highlight bash %}
$ cd /usr/local
$ git remote set-url origin git://mirrors.ustc.edu.cn/homebrew.git
{% endhighlight %} 
国内开源镜像源:
清华镜像源: http://mirrors.tuna.tsinghua.edu.cn/  
科大镜像源: http://mirrors.ustc.edu.cn/  