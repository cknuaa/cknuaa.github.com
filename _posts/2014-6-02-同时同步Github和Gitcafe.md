---
layout: post
title:  同时同步Github和Gitcafe
date:   2014-6-02 20:41:29
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
    git push origin master //更新到远程服务器上
</pre>
