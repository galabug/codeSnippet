```
#切换到任意非test master分支分支
git checkout dev

#删除本地的test分支
git branch -D test
git branch -D master

#删除本地残留的远程跟踪分支
重命名
git branch rd origin/test
删除
git branch -D rd

重命名
git branch rd origin/master
删除
git branch -D rd

#如果本地test还有缓存，可以先执行下面命令再 checkout
git gc --prune=now

#更新远程仓库最新信息
git fetch --all

#重新拉取服务最新  master分支代码
git checkout master

#重新新建开发分支
git checkout -b dev-func
```
