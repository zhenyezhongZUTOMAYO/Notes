## 这是什么？

版本控制器方式
集中式版本控制工具
SVN 和CVS

分布式版本控制工具
Git
每个人的电脑都存储着自己的版本库


## 操作
GitBash: 在任意文件管理器右键点击更多选项找到GitBash即可打开
第一步配置用户名和用户邮箱

```
git config --global user.name "用户名"
git config --global user.email "用户邮箱"
```

#### 创建本地仓库
选择文件夹在当前文件夹下打开GitBash
```
git init
```
#### Git基本操作

![[Drawing 2025-09-04 14.04.02.excalidraw]]

###### add(将修改提交到暂存区)

```
git add 某个文件名
或
git add 通配符
```
将所有修改添加都加入暂存区
```
git add .
```


###### commit（将修改从暂存区提交到本地仓库）
```
git commit -m "提交说明"
```

###### log(查看提交日志)

```
git log [option]
```
可以通过这个查看commitID

###### status(查看状态)
```
git status
```
###### 版本回退
```
git reset --hard commitID
```
	查看已经删除的记录  git reflog
###### 忽略部分文件
在文件夹下创建 .gitignore文件
```
touch .gitignore
```
每一行为要忽略的文件名或通配符

#### 分支
###### 查看分支
```
git branch
```
###### 创建分支
```
git branch 分支名
```
###### 切换分支
```
git checkout 分支名
```
```
git checkout -b 分支名 #创建并切换分支
```
###### 合并分支
```
git merge 分支名 #将当前分支与指定分支名合并
```
###### 删除分支
```
git branch -d 分支名 #删除分支时需要做各种检查
git branch -D 分支名 #强制删除
```
注:不能删除当前分支

###### 解决冲突
在对两个文件进行合并出现冲突会出现这样的提示
```
Auto-merging Count.txt
CONFLICT (add/add): Merge conflict in Count.txt          #这里提示的就是冲突的位置
Automatic merge failed; fix conflicts and then commit the result.
```

在冲突文件里会看见
```
<<<<<<< HEAD
count = 2
=======
count = 1
>>>>>>> dev
```
<<<<<<< HEAD 这里指向为当前文件

\>>>>>>> dev 这里为要合并的文件

保留一个就行了

之后添加到暂存区
提交到本地仓库即可
合并只会在当前分支显示


#### 分支使用原则
![[Drawing 2025-09-04 17.47.47.excalidraw]]


###### master (生产)分支
线上分支,主分支,中小规模作为线上运行的应用
###### develop (开发)分支
一般作为开发部门的主要开发分支,如果没有其他并行开发不同期线上要求,都可以在此版本进行开发
###### feature/xxxx分支
一般是同期并行开发
###### hotfix/xxxx分支
从master派生的分支,一般作为线上bug修复使用
2025-09-04 10:44
