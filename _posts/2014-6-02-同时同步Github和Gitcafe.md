---
layout: post
title:  同时同步Github和Gitcafe
date:   2014-6-02 20:40:29
category: "blog"
---
在本地项目仓库中.git文件夹中的config文件中添加

    [remote "cafe"]
	url = git@gitcafe.com:cknuaa/cknuaa.git
	fetch = +refs/heads/*:refs/remotes/cafe/*
	url = git@github.com:cknuaa/cknuaa.github.com.git
	fetch = +refs/heads/*:refs/remotes/origin/*

push的时候用

    git push cafe master
    


