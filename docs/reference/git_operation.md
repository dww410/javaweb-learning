# GIT常用命令

### GIT 分支操作

#### 远程分支更新获取
1. 远程主机的更新全部取回本地：git fetch
2. 远程分支：git branch -a 发现远程的分支已经可见了
3. 拉取远程分支到本地：git checkout -b 远程分支名 origin/远程分支

#### 本地删除了分支，远程也想删除。
1. 使用git branch -d 分支名来删除本地分支。
2. 使用git push origin -d 分支名直接来删除远程分支。在次使用git branch -a,发现分支已经不存在了。
或者
3. 使用git branch -d 分支名来删除本地分支。

#### 远程删除了分支，本地也想删除。
1. git branch -a查看远程分支，红色的是本地远程远程分支记录。
2. 执行下面命令查看远程仓库分支和本地仓库的远程分支记录的对应关系：git remote show origin  
3. 会看到：refs/remotes/origin/远程仓库已经删除的分支名              stale (use 'git remote prune' to remove)
   其中：Local refs configured for 'git push':  命令下面的分支是本地仓库的远程分支记录中仍存在的分支，但远程仓库已经不存在。
4. 输入git remote prune origin来删除远程仓库已经删除过的分支
5. 验证 git branch -a 此时可以看到本地远程分支记录已经和远程仓库保持一致了。