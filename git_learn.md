# Git使用



## 创建版本库

```c
/*创建空目录*/
$ mkdir doucment_name
$ cd doucment_name
$ pwd          /*显示当前目录位置*/

$ git init     /*把这个目录变成Git可以管理的仓库*/  /*然后就回多一个.git的子目录，不要动*/

/*写一个文件，放到仓库目录(或子目录)下*/
$ git add 文件名.后缀    /*将文件添加到仓库*/  /*可以添加多个文件再提交到仓库*/
$ git commit -m"自己写做了什么改动，如：wrote a new file"    /*将文件提交到仓库*/

$ git status  /*查看仓库当前状态，如：某文件被修改过，但还没有准备提交修改*/
$ git diff  /*查看具体修改内容*/
/*提交修改和提交新文件是一样的，add + commit 命令*/

/*版本回退*/
$ git log  /*查看历史版本改动记录*/  /*有版本号(commit id),作者，改动时间，改动描述*/
$ git log --pretty=oneline  /*一个版本显示一行，只显示版本号和改动描述*/
$ git reset --hard HEAD^  /*回退到上个版本，几个^就表示往上第几个版本，HEAD~100表示往上第100个版本*/
    /*回退之后又想回到最新的版本*/
$ git reset --hard 1094a(版本号，前几位即可)
/*找不到版本号了*/  $ git reflog  /*查看每一次命令*/
```

