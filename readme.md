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
git branch <branch name> # 创建分支
git branch -d <branch name> # 删除分支
git switch <branch name> # 切换分支
git switch -c <branch name> # 创建并切换分支
```

# 变基
> 在开发中除了通过merge来合并分支外, 还可以通过变基(rebase)来完成分支的合并
> 我们通过merge合并分支时, 在提交记录中会将所有的分支创建和分支合并的过程全部显示出来, 这样当项目比较复杂,开发过程比较波折时, 我们必须
> 反复地创建、合并、删除分支. 这样一来将会使我们代码的提交记录变得极为混乱

> 原理 (变基时发生了什么)
* 1. 当我们发起变基时,git会首先找到两条分支的最近的共同祖先
* 2. 对比当前分支相对于祖先的历史提交, 并且将他们提取出来存储到一个临时文件
* 3. 将当前部分指向目标的基地
* 4. 以当前基地开始, 重新执行历史操作


