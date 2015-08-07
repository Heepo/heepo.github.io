---
layout: post
title: Kramdown Missing 处理
categories: 技术
tags: Jekyll Kramdown
---
今天在尝试使用Rouge来实现代码高亮时，更新了下Jekyll为最新版本，更新后却报了"Missing dependency: kramdown"错误，如下  

{% highlight bash %}
➜  repository git:(branch) ✗ jekyll serve
You are missing a library required for Markdown. Please run:
  $ [sudo] gem install kramdown
  Conversion error: Jekyll::Converters::Markdown encountered  
  an error while converting '_posts/***.md/#excerpt':
                    Missing dependency: kramdown
             ERROR: YOUR SITE COULD NOT BE BUILT:
                    ------------------------------------
                    Missing dependency: kramdown
{% endhighlight %}
Kramdown是装了的，搜索一番之后，原来是Jekyll寻找Kramdown的位置和本机Kramdown实际所在位置不同。根本原因在于不同安装方法软件安装位置不同，相互依赖关系混乱，加上OSX本身还自带Ruby、Gem等