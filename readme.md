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




