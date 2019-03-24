#  github---push,clone,pull

!!!区别仓库名(origin)和远程分支名(master)和本地分支名(master)

``` 
$ git remote -v
$ git remote add [远程仓库名] [远程git服务器地址]
$ git remote rm [远程仓库名]
$ git remote remove  [远程仓库名]          //delete
```

### push

```
$ git push [远程仓库名] [本地分支名称]
$ git push [远程仓库名]  本地分支:远程仓库分支 
$ git push [远程仓库名]  远程仓库分支 
$ git push -p   //强制推送
//error时检查文件是否提交到了本地库 或者 有没有branch conflict
https://blog.csdn.net/u011957758/article/details/50901122
https://blog.csdn.net/kiddd_fu/article/details/78247290
```

### clone

```
$ git clone [url]                //download   创建origin远程地址别名  初始化本地库
```

### pull = fetch + merge

``` 
 $ git fetch [远程仓库名] [远程仓库分支]        //仅抓取
 $ git checkout [远程仓库名/远程仓库分支]     //查看抓取的分支
 $ git merge  [远程仓库名/远程仓库分支] 
 ||
 $  git pull [远程仓库名]  [本地分支]
```





