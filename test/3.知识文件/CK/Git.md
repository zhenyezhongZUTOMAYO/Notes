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


2025-09-04 10:44

