---
layout: post
title:  同时同步Github和Gitcafe
date:   2014-11-29 00:00:50
category: "lib"
---

<span id="tagline">
首先，在本地项目仓库中.git文件夹中的config文件中添加如下代码
</span>

<pre>
    [remote "cafe"]
    url = git@gitcafe.com:cknuaa/cknuaa.git
    fetch = +refs/heads/*:refs/remotes/cafe/*
</pre>


push到gitcafe的时候用

<pre>
    git push cafe master:gitcafe-pages
</pre>


push到github的时候用

<pre>
    git push origin master
</pre>

好久没用又忘了一些动东西，补充一下，在使用新环境重新部署仓库的时候，首先解决连接远程仓库的问题，需要SSH密匙，我之前的都没有备份，只好重新生成

<pre>
$ ssh-keygen -t rsa -C "your email"
Generating public/private rsa key pair.
Enter file in which to save the key (/Users/your_user_directory/.ssh/id_rsa):<回车就好>
</pre>

得到新的密匙之后分别贴到两个远程仓库管理中去，就可以测试连接了，这一步还是必须的，要不然没有授权会连接不上，测试命令为：

<pre>
$ ssh -T git@github.com //github 连接测试
$ ssh -T git@gitcafe.com //gitcafe 连接测试
</pre>

如果提示

<blockquote>
You've successfully authenticated
</blockquote>

就表明远程仓库已经连接上了，这时就可以进行远程数据拉取到本地的操作，用clone命令就行，然后对本地仓库进行初始化，创建好.git初始文件夹。





