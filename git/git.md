# git常用指令



- git clone：把远程仓库复制到本地
- git init：初始化git仓库（就是创建.git文件夹）
- git branch：查看分支
- git checkout [-b] master：切换分支（-b的作用是如果没有这个分支就创建一个）
- git add filename ：将本次修改加入到本次提交中
- git commit -m “说明”：提交本次记录的所有修改
- git push：将本地仓库更新到远端
- git remote：查看远程仓库信息



### 在GitHub创建一个新仓库的步骤

1. 在GitHub上开一个仓库，拿到远程仓库链接，如：https://github.com/burning846/rookie-helper.git。（注意不要选择自动创建README.md的选项，不然要涉及merge操作。）
2. 在你想创建仓库的最顶层文件夹使用 `git init` 命令，建立.git本地仓库
3. 使用 `git add .` 命令将文件夹下所有文件加入本次记录
4. 使用 `git commit -m 'init'` 命令将本次修改提交
5. 使用 `git remote add origin https://github.com/burning846/rookie-helper.git` 将远程仓库链接加入到本地仓库记录的信息中
6. 使用 `git push -u origin master` 命令将本地仓库同步到远程仓库，其中 `-u origin master` 的作用是将你的本地分支和远程master分支连接。
7. 刷新一下GitHub就能看到你的新仓库了~