# git基本命令
- `ssh-keygen -t rsa -C "youremail@example.com"`: 用来生成秘钥
- `git config --global user.email "你申请github用的邮箱"`
- `git config --global user.name "你的github用户名"`
- `git config user.name` 查看用户名
- `git config user.email` 查看邮箱
- `git clone 项目地址`
- `git clone 项目地址 -v 别名`
- `git add *`
- `git commit -m "asdfasdf"`
- `git push`
- `git rm filename`: 删除文件
- `git pull`: 拉下来最新的代码

- `git diff`: 查看提交了些什么
- `git log`: 查看提交历史
- `git show`: 查看改变
- `git branch`: 查看本地的分支
- `git status`: 查看本分支的文件情况

- `git checkout -b develop`: 新建并切换到develop分支
- `git checkout master`: 切换到master分支
- `git merge develop`: 将develop分支合并到当前分支

- `git reset --hard HEAD^`: 版本回退
- `git reset --hard commitid`: 回退到commitid这个版本，使用`git log查看`commitid
- `git checkout 版本号`：切换到版本号对应的代码版本
- `git checkout finename`: 在`git add *`之前，可以反悔撤销。
- `git log --graph --pretty=oneline --abbrev-commit`: 查看漂亮的代码提交历史
- `git push --set-upstream origin develop`: 当远程仓库github中没有develop分支时，将本地的develop分支提交到仓库里面。
- `git branch -d develop`: 删除本地的develop分支
- `git push -d origin develop`: 删除远程的develop分支
- `git push origin --delete develop`: 同上
- `git branch -D develop`: 强行删除develop分支
- `git stash`: 缓存工作区内容
- `git stash list`: 查看缓存中的工作区内容
- `git stash pop`: 恢复工作区
- `git rebase -i commitid`: 将commitid后面的所有commit合并成一个commit提交
- `git push --force`: 强制提交
- `git tag` 打标签
- `git tag -a 标签名 -m 说明 commitid` 为 目标提交 打标签
- `git add -f 文件名` 忽略忽略，强制提交
- `git check-ignore -v 文件名` 检查忽略
- `git tag -d` 标签名 删除标签
- `git push origin` 标签名 推送标签到远程
- `git push origin --tags` 推送所有为推送的本地标签
- `git push origin :refs/tags/标签名` 删除远程tag(先删除本地的)
- `git reset HEAD file` 撤销暂存区
# 配置别名
- `git config --global alias.st status`
- `git config --global alias.co checkout`
- `git config --global alias.ci commit`
- `git config --global alias.br branch`
- `git config --global alias.unstage 'reset HEAD'`
- `git config --global alias.last 'log -1'`
- `git config --global alias.lg "log --color --graph --pretty=format:'%Cred%h%Creset -%C(auto)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit"`

# 配置文件
项目：项目路径/.git/config
用户：家目录/.gitconfig

层级优先：项目级 > 用户级 > 系统级

# 参考资料
[廖雪峰-git](https://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000)  
[pro git(码云)](https://gitee.com/progit/)
