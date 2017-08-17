---
title: 带江湾飞起来
date: 2017-08-17 10:02:52
tags:
---




Unix的哲学是“没有消息就是好消息“






创建密钥
ssh-keygen -t rsa -C "youremail@example.com"

ssh -T git@git.oschina.net
ssh -T git@github.com

--查看远程仓库的信息
$ git remote	|	git remote -v
git remote -v # 查看远程服务器地址和仓库名称
--远程仓库管理-origin远程仓库的名字
git remote add osc git@git.oschina.net:xx252016/blog.git
git remote add gh  git@github.com:xx252016/xx252016.github.io.git
git remote rm <repository> # 删除远程仓库
git remote set-url gh git@github.com:xx252016/xx252016.github.io.git # 设置远程仓库地址(用于修改远程仓库地址)
git remote show gh # 查看远程服务器仓库状态

---------------------------------------------------------------------------------------------------------git-http://git-scm.com
--只能跟踪文本文件的改动，比如TXT文件，网页，所有的程序代码等等》（word 二进制格式）
sudo apt-get install git
--源码
./config，make，sudo make install
--windows Cygwin+git--》msysgit
$ git config --global user.name "xx252016"
$ git config --global user.email "xx252016@163.com"
$ git config --global color.ui true
$ git config --global alias.st status
$ git config --global alias.co checkout
$ git config --global alias.ci commit
$ git config --global alias.br branch
$ git config --global alias.unstage 'reset HEAD'
$ git config --global alias.last 'log -1'
git config --global alias.lg "log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit"

$ mkdir learngit
$ cd learngit
$ pwd
--把这个目录变成Git可以管理的仓库：
git init
--查看所有，包含隐藏
ls -ah

git add <file>
git commit 	[-m ]

git status
git diff
git log
$ git reset --hard HEAD^
$ git reset --hard commit_id
git reflog
git checkout -- file
--远程仓库



$ git push [-u] origin master
$ git clone git@github.com:xx252016/gitskills.git


--创建分支
$ git checkout -b dev==><$ git branch dev+$ git checkout dev>
--查看分支
$ git branch
--切换回master分支后
$ git checkout master
$ git merge dev
----no-ff参数，表示禁用Fast forward
$ git merge --no-ff -m "merge with no-ff" dev
--删除分支
$ git branch -d dev
--bug分支
$ git stash
$ git status
$ git stash list
$ git stash pop(==>git stash apply+git stash drop)
$ git stash list

$ git push origin master
$ git push origin dev
--创建标签
$ git tag v1.0
$ git tag v0.9 6224937
$ git show v0.9
git tag -a <tagname> -m "blablabla..."可以指定标签信息；
git tag -s <tagname> -m "blablabla..."可以用PGP签名标签；
--可以查看所有标签。
git tag
    命令git push origin <tagname>可以推送一个本地标签；
    命令git push origin --tags可以推送全部未推送过的本地标签；
    命令git tag -d <tagname>可以删除一个本地标签；
    命令git push origin :refs/tags/<tagname>可以删除一个远程标签。


https://github.com/michaelliao/gitskills.git
git@github.com:xx252016/gitskills.git
