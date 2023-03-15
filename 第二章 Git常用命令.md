[Git 详细安装教程（保姆级详细教程）_git安装_Siobhan. 明鑫的博客-CSDN博客](http://t.csdn.cn/hhpXK)

看上面的教程或者尚硅谷的视频

```
git config --global user.name    #设置用户签名
git config --global user.email
```

#### 2.1 初始化本地库

```
git init
```

#### 2.2 查看本地库状态

```
git status
```

#### 2.3 添加到暂存区

```
git add <file>
```

#### 2.4 将暂存区文件提交到本地库，生成历史版本

```
git commit -m "日志信息/日志信息" 文件名
```

<img src="file:///C:/Users/南极星/AppData/Roaming/marktext/images/2023-03-09-18-09-33-image.png" title="" alt="" width="570">

<img src="file:///C:/Users/南极星/AppData/Roaming/marktext/images/2023-03-09-18-13-35-image.png" title="" alt="" width="570">

#### 2.5 修改文件

上述是提交一次的本地库状态变化和日志信息。

如果对hello.txt文件作出修改，会有什么变化呢？

- 修改hello.txt，在第一行后面加上6个2.

- 查看本地库状态，检测到工作区有文件被修改，但是是红色，表示还未添加到暂存区，未被追踪；

- 使用`git add hello.txt`命令将工作区的修改添加到暂存区，再次查看本地库状态，修改文件变绿色了，代表已被追踪；

<img src="file:///C:/Users/南极星/AppData/Local/Temp/WeChat%20Files/91fa34690254d137f86456fc09ad060.png" title="" alt="91fa34690254d137f86456fc09ad060.png" width="562">

- `git commit -m "second commit" hello.txt`将文件提交到本地库

- 查看本地库状态，有未被追踪的文件，但没有什么可提交的文件

- `git reflog`显示可引用的历史版本记录，指针HEAD指向第二个版本

<img src="file:///C:/Users/南极星/AppData/Local/Temp/WeChat%20Files/9834c6a3bab8c5bfc72149bfcccb8d6.png" title="" alt="9834c6a3bab8c5bfc72149bfcccb8d6.png" width="563">

#### 2.6 历史版本

##### 1、 查看历史版本

###### 基本语法

`git reflog`查看精简的版本信息

`git log`查看详细的版本信息

<img src="file:///C:/Users/南极星/AppData/Local/Temp/WeChat%20Files/343335ebcbce69c7ac9f7cf1c3ae768.png" title="" alt="343335ebcbce69c7ac9f7cf1c3ae768.png" width="447">

<img src="file:///C:/Users/南极星/AppData/Local/Temp/WeChat%20Files/6cfef7bdcac10bb9cc0db5cd0311f35.png" title="" alt="6cfef7bdcac10bb9cc0db5cd0311f35.png" width="442">

##### 2、版本穿梭

###### 基本语法

`git reset --hard 版本号`

<img title="" src="file:///C:/Users/南极星/AppData/Local/Temp/WeChat%20Files/d2d5cdfc6883af38665b6a12999c4c0.png" alt="d2d5cdfc6883af38665b6a12999c4c0.png" width="315" data-align="inline">

<img title="" src="file:///C:/Users/南极星/AppData/Local/Temp/WeChat%20Files/3341c9e72f5de0456346349bd513fb2.png" alt="3341c9e72f5de0456346349bd513fb2.png" width="324">
