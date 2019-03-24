# git start!!!

1. Create local  repository   目录下初期化 **git init**
   会出现一个 .git 隐藏文件  查看方法：
   mac ： defaults write com.apple.finder AppleShowAllFiles TRUE   然后重启Finder
   linux :  ls -lA

2. Sign (user & email)
   作用：区分开发人员
   命令：一 ，项目/仓库级别 ：当前项目/仓库 (.git/config) 
              二，   系统级别； 当前系统        (家目录 ls -lA | grep .gitconfig)
    级别就近生效（有项目仓库则不用系统 ，**不允许都没有**）
              **git config user.name  ???**        **git config  --global user.name  ???** 
               **git config user.email  ???.com**       **git config   --global user.emai  ???.com **

3. Add & submit & check status
   仓库下用 git status

   **git add file **

   **git rm --cached file**
   **git commit file**        进入vim编写修改信息

   **git commit -m 'my second commit' file**    用-m后面 ‘  ’写信息（不用进vim了）

   

   

   

   

   

   

   

   

