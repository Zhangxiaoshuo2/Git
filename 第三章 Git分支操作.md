#### 4.1 查看分支

`git branch -v`（*、绿色代表当前所在的分区）

![06c7b4e93bf99fa6fab6aa48a09230b.png](C:\Users\南极星\AppData\Local\Temp\WeChat%20Files\06c7b4e93bf99fa6fab6aa48a09230b.png)

#### 4.2 创建分支

`git branch 分支名`  

![903605cdfe5028e5fc792439e43bd62.png](C:\Users\南极星\AppData\Local\Temp\WeChat%20Files\903605cdfe5028e5fc792439e43bd62.png)

#### 4.3 切换分支

`git checkout 分支名`

![aa3ba192379295f3d771b2f0acde23c.png](C:\Users\南极星\AppData\Local\Temp\WeChat%20Files\aa3ba192379295f3d771b2f0acde23c.png)

![0d0de01912bf6d2783709070c8994e8.png](C:\Users\南极星\AppData\Local\Temp\WeChat%20Files\0d0de01912bf6d2783709070c8994e8.png)

#### 4.4 合并分支

`git merge 分支名`将指定的分支合并到当前分支上

合并前：

<img src="file:///C:/Users/南极星/AppData/Roaming/marktext/images/2023-03-14-16-02-10-image.png" title="" alt="" width="212">

合并后：当前分支是master，指定分支是hot-fix

<img src="file:///C:/Users/南极星/AppData/Roaming/marktext/images/2023-03-14-16-03-48-image.png" title="" alt="" width="218">

#### 4.5 产生冲突

发现了一篇超级棒的文章！！

[详解Git合并冲突——原因及解决 “Automatic merge failed； fix conflicts and then commit the result.“_JiangHao Lan的博客-CSDN博客](http://t.csdn.cn/WjDlz)

###### 4.5.1 why产生冲突？

      <mark>两个分支在同一文件的同一位置做了不同的修改</mark>，Git无法替我们决定使用哪一个，必须<mark>人为决定</mark>新代码的内容。

###### 4.5.2 制造一个冲突

1、在master分支修改hello.txt文件，添加到暂存区并提交修改；

<img src="file:///C:/Users/南极星/AppData/Roaming/marktext/images/2023-03-14-17-16-53-image.png" title="" alt="" width="241">

2、切换到hot-fix分支，修改文件，添加并提交修改；

<img src="file:///C:/Users/南极星/AppData/Roaming/marktext/images/2023-03-14-17-23-38-image.png" title="" alt="" width="246">

3、切换到master分支，合并分支，发生冲突

![](C:\Users\南极星\AppData\Roaming\marktext\images\2023-03-14-17-24-42-image.png)

###### 4.5.3 如何查看冲突？

触发冲突之后，进入了合并的中间状态MERGING。

`git status`告诉我们以下信息：

- “You have unmerged paths”：我们现在正处于合并的中间状态，有一些没有合并的文件；

- “Unmerged paths”：下面**列出了所有未合并的文件**，都显示为红色。可以看到，`hello.txt`没有合并，因为两个分支都更改了它（“`both modified`”），发生了冲突。

![](C:\Users\南极星\AppData\Roaming\marktext\images\2023-03-14-17-28-47-image.png)

查看冲突。用vim打开hello.txt

<img title="" src="file:///C:/Users/南极星/AppData/Local/Temp/WeChat%20Files/51af3396044063fb43914200209153e.png" alt="51af3396044063fb43914200209153e.png" width="232">

![](C:\Users\南极星\AppData\Roaming\marktext\images\2023-03-14-17-34-39-image.png)

###### 4.5.4 如何解决冲突？

![](C:\Users\南极星\AppData\Roaming\marktext\images\2023-03-14-17-36-16-image.png)

<img src="file:///C:/Users/南极星/AppData/Roaming/marktext/images/2023-03-14-17-38-39-image.png" title="" alt="" width="232">
