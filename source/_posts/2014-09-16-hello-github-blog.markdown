---
layout: post
title: 搭个博客
date: 2014-09-16 12:40:47 +0800
comments: true
categories: 
---
<p>搭建步骤</p>

<p>搭建本地环境(安装Git、安装Ruby、安装DevKit)</p>

<p>配置环境(克隆Octopress、安装Octopress依赖项)</p>

<p>将博客部署到GitHub上</p>

<p>配置博客</p>

<p>发表博客</p>

<p>搭建具体步骤大牛们已经很详细了,我就不赘述了.</p>

<p>参考</p>

<p>http://blog.devtang.com/blog/2012/02/10/setup-blog-based-on-github/</p>

<p>http://blog.csdn.net/jackystudio/article/details/16117585
主题</p>

<p>这是我使用的主题:</p>

<p>$ git clone git@github.com:shashankmehta/greyshade.git .themes/greyshade
$ echo "\$greyshade: color;" >> sass/custom/_colors.scss //Substitue 'color' with your highlight color
$ rake "install[greyshade]"
$ rake generate</p>

<p>使用完以后别忘记generate/deploy
新浪微博
发现 sina weibo 的添加不只是更改<em>config.yml
首先在</em>config.yml 加上</p>

<p>weibo_user: smallyin00
其次添加“weibo.png” 到 “octopress/source/images/social”
然后加代码到“octopress/sass/parts/_header.scss文件中</p>

<p>&amp;.weibo{
  background: image-url('social/weibo.png') center no-repeat #e32529;
  border: 1px solid #e32529;
  &amp;:hover{
      border: 1px solid darken(#e32529, 10%);
  }
}
最后加代码到octopress/source/_includes/header.html文件中</p>

<p>&lt; a class="weibo" href="http://www.weibo.com/smallyin00" title="Weibo">Weibo</p>