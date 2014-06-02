---
layout: post
title:  同时同步Github和Gitcafe
date:   2014-6-02 20:40:29
category: "lib"
---
在本地项目仓库中.git文件夹中的config文件中添加

    [remote "cafe"]
    url = git@gitcafe.com:cknuaa/cknuaa.git
    fetch = +refs/heads/*:refs/remotes/cafe/*

push到gitcafe的时候用

    git push cafe master:gitcafe-pages

push到github的时候用
    
    git push origin master //更新到远程服务器上

    


