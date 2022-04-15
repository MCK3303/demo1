 git笔记

进度P13

git：分布式版本管理
代码托管中心（远程库）

git add：工作区（类似vscode工作目录的文件夹） 提交到暂存区
![](C:\Users\MCK\Pictures\notepics\git笔记图\git add笔记1.png)

git commit：暂存区 （临时存储代码的地方）提交到本地库
基本语法：git commit -m "日志信息"  文件名
![](C:\Users\MCK\Pictures\notepics\git笔记图\git commit笔记1.jpg)
git log：查看版本信息

黄色字commit后面的 是完整的版本号
下面是用户签名

git status：查看状态

git reflog：查看引用日志信息

git push：（推送）本地库 提交到远程库

git pull：远程库拉取代码到本地库

git用户签名只是本地的，跟github以及在线网站没有关系

### 版本穿梭

git reset --hard 7位版本号 ![](C:\Users\MCK\Pictures\notepics\git笔记图\git reset笔记1.jpg)

Git切换版本，底层其实是移动HEAD指针
可以看到图中当版本从第3个版本回到第2个版本时，(HEAD->master)指向了第2个版本
![](C:\Users\MCK\Pictures\notepics\git笔记图\git切换版本图.jpg)

Git分支操作：
git branch：创建分支
git branch -v：查看分支
git checkout：切换分支

![](C:\Users\MCK\Pictures\notepics\git笔记图\git分支笔记1.jpg)

![](C:\Users\MCK\Pictures\notepics\git笔记图\git分支2.jpg)

可以看到分支从master主分支切换到了hot-fix
在新的分支修改完代码后，记得git status查看状态、git add提交暂存区以及git commit等等

合并分支：分为正常合并 和 冲突合并
git merge （要合并的分支）
？head指针主要指向分支（比如经常见的(HEAD->master))
而master指针主要指向的是具体版本

创建远程库：
上github网站，右上角加号 + ，New repository

把本地库代码推到远程库：
![git push1](C:\Users\MCK\Pictures\notepics\git笔记图\git push1.png)

git push 本地库别名 分支名

远程库拉取到本地库 也是一样的（本地库与远程库保持同步状态）
git pull ...