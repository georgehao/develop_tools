1. 添加子目录，建立与luka项目的关联。(--squash 禁止用)
git remote add -f content-console ssh://git@gitlab.superman2014.com:10022/php/content-console.git
git subtree add --prefix=ext/Content/Console content-console master
语法
git remote add -f <子仓库名> <子仓库地址>
git subtree add --prefix=<子目录名> <子仓库名> <分支> 
-f 意思是在添加远程仓库之后，立即执行fetch。
--prefix之后的=等号也可以用空格，或者-P 。
2. 从远程仓库更新子目录core
git fetch content-console master 
git subtree pull --prefix=ext/Content/Console content-console master 
语法 
git fetch <远程仓库名> <分支>
git subtree pull --prefix=<子目录名> <远程分支> <分支>
3. 从子目录push到远程仓库(根目录操作)
git subtree push --prefix=ext/Content/Console content-console master
语法
git subtree push --prefix=<子目录名> <远程分支名> 分支
