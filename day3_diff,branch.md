#  diff  &  branch & solve conflict

###  比较diff

```bash
git diff a.txt     //默认和index进行比较
```

```bash
git diff HEAD a.txt   //和repository进行比较
```

```bash
git diff HEAD^ a.txt  //和history进行比较
```

```
git diff branch1 branch2 --stat   //显示出所有有差异的文件列表
git diff branch1 branch2 具体文件路径   //显示指定文件的详细差异
git diff branch1 branch2                   //显示出所有有差异的文件的详细差异
```

### branch

```bash
git branch  name    //create branch
```

```bash
git branch -v       //チェック　branch
```

```bash
git checkout name   //切り替える　branch
```

```bash
git merge  b分支    //切换到a分支 去合并b分支(a得到修改，b不变)
```



## solve branch conflict

```bash
//前提：两个分支同时修改一个文件且提交向repository之后
//一个去merge另一个 会出现conflict
PHB:lianxiGit cno.107$ git merge master
Auto-merging apple.txt
CONFLICT (content): Merge conflict in apple.txt
Automatic merge failed; fix conflicts and then commit the result.
```

```bash
//需要手动提交
//その前、ちょっとファイルを見てみよう
vim apple.txt
<<<<<<< HEAD              //HEAD为 current branchの修正
change by hot_fix　　　　　//HEAD为 current branchの修正の内容
=======
change by master　　　　　//master为 master branchの修正の内容　
>>>>>>> master　　　　　　//master为  master branchの修正　

//手动修改到满意并 :wq
```

``` bash
git add apple.txt
git commit -m 'solve conflict'       //ファイル名が要らない　メッセージ必要
```

