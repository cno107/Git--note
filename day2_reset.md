# day2 查历史,前后进,找回删除文件

1.  git log
   git log  --pretty=oneline   一行
   git log  --oneline          一行&缩短哈希值  

2. git reflog

   42a1dc9 (**HEAD ->** **master**) HEAD@{0}: commit: third

   58c7b65 HEAD@{1}: commit: my second commit

   **HEAD@{1}移动到当前版本需要1步**  

3. 前后进   index     ^     ~
   git  reset   --hard   index(哈希)

   ^  :后退  git reset --hard HEAD^^    (后退两步)
   ~ :后退  git reset --hard HEAD～2    (后退两步)

4. reset参数
     --soft     (Does not touch the index file缓存区 or the working tree )只动本地库
     --mixed   (Resets the index but not the working tree) 本地库+暂存区
     --hard      (Resets the index and working tree)

   soft后退一步 相当于index & working tree 前进一步  所以git status状态为绿 及本地库和暂存区有变动
   mixed后退一步 相当于working tree 前进一步    所以git status状态为红 及本地库和暂存区无变动 

5. 文件删除并找回
   前提：删除前，文件存在时的状态已经提交到了repository
   操作：git reset --hard  [pointer]
        删除操作已提交到本地库 ：pointer    point   history
       删除操作尚未确定提交到本地库 ：pointer  use   HEAD  

   