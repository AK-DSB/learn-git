# git的两种状态
* 未跟踪
* 已跟踪 (暂存, 未修改, 已修改)

## 刚刚添加到项目中的文件处于未跟踪状态
> 未跟踪 ---> 暂存 (git add)
> 暂存 ---> 未修改 (git commit)
> 未修改 ---> 修改 (修改文件内容)


# 常用命令
> git commit -a -m''  提交所有已修改的文件 (未跟踪的文件不会提交)

* 重置文件
> git restore <filename> # 恢复文件
> git restore --staged <filename> # 取消暂存状态 

* 删除文件
> git rm <filename> -f


# 分支
> git在存储文件时, 每一次代码的提交都会创建一个与之对应的节点, git就是通过一个一个的节点来记录代码的状态的,节点会构成一个树状结构,树状结构就意味着这个树会存在分支

```shell
git branch # 查看当前分支
git branch <branch name> 创建分支
git branch -d <branch name> 删除分支
```


