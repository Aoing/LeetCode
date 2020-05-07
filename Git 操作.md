# Git 操作

![image-20200420224153717](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200420224153717.png)

## 1、创建远程仓库

直接  github 上创建仓库

## 2、将本地文件添加到本地仓库

```shell
git add [文件名]
```

## 3、查看历史版本

```shell
git log
```

## 4、回退到某一版本

```shell
git reset --hard [上一步查到的版本号]
```

## 5、强制回退远程仓库到当前版本

```shell
git push -f
```

## 6、从暂存区删除文件，工作区则不做出改变

```shell
git rm --cached <file>
```

## 7、查看暂存区当前状态

```shell
git status -s
```

## 8、查看执行 git status 的结果的详细信息

```shell
#尚未缓存的改动
git diff

#查看已缓存的改动
git diff --cached

#查看已缓存的与未缓存的所有改动
git diff HEAD

#显示摘要而非整个
diff：git diff --stat
```

## 9、将缓存区内容添加到仓库中

```shell
git commit -m '第一次版本提交'	# -m ：注释
```

## 10、配置用户名和邮箱地址，避免每次提交都要输入用户名和密码

```shell
$ git config --global user.name 'Aoing'
$ git config --global user.email 997360720@qq.com
```

## 11、取消已缓存的内容

```shell
git reset HEAD [filename]
```

## 12、从工作目录中手工删除文件

```shell
git rm <file>

#如果删除之前修改过并且已经放到暂存区域的话，则必须要用强制删除选项 -f
git rm -f <file>

#如果把文件从暂存区域移除，但仍然希望保留在当前工作目录中，换句话说，仅是从跟踪清单中删除，使用 --cached 选项即可
git rm --cached <file>
```

## 13、从远程仓库下载新分支与数据

执行 **git fetch [alias]** 告诉 Git 去获取它有你没有的数据

```shell
git fetch [本地分支名] 
```

## 14、从远端仓库提取数据并尝试合并到当前分支

执行 **git merge [alias]/[branch]** 以将服务器上的任何更新（假设有人这时候推送到服务器了）合并到当前分支。

```shell
git merge [alias]/[branch]
```

## 15、推送到远程仓库

```shell
# 将 [branch] 分支推送成为 [alias] 远程仓库上的 [branch] 分支
git push [alias] [branch]
```

## 16、删除远程仓库

```shell
git remote rm [别名]
```

## 17、添加仓库 origin2

```shell
git remote add origin2 git@github.com:tianqixin/runoob-git-test.git
```


# Git 客户端工具
GitKraken

