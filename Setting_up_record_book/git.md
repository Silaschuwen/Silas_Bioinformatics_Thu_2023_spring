*This file will briefly describe my process of installing git in MacOS*   

**Apple M1 Macbook Pro 2021** **Ventura 13.2.1**


## What is git?  

linux是开源系统，需要很多开发者来开发和维护，这避免不了有很版本的迭代和更新，**git就是这样一个工具，它能够保存代码的各个版本**  
每个版本文件的修改，删除，Git 都会跟踪，以便任何时候都可以追踪历史或者在将来某一时刻可以还原  
说的通俗易懂一点：**git可以帮助你记录每一次代码改动的情况，可以随时恢复、复制某一时刻的代码**

<img width="716" alt="image" src="https://user-images.githubusercontent.com/111068556/221395561-bf5860ec-4338-43f3-bba6-d3958b867b21.png">


## Git installation  
1. **git的官方网址链接:  https://git-scm.com/download 点击macOS。**

<img width="681" alt="image" src="https://user-images.githubusercontent.com/111068556/221395641-849be433-797d-473f-b9cb-ab60818feb99.png">

2. **选择安装方式，因为我没有homebrew，选择文件直接安装。**
<img width="673" alt="image" src="https://user-images.githubusercontent.com/111068556/221395648-2890dfb9-abe1-4529-81be-341865761288.png">

3. **点击download并完成安装**  
***注意使用安装器安装pkg，直接安装会失败***
<img width="596" alt="image" src="https://user-images.githubusercontent.com/111068556/221395757-54201955-e6ea-4260-af67-1a4649ccaf41.png">

4. **在终端中输入git --version出现版本号即可**
<img width="397" alt="image" src="https://user-images.githubusercontent.com/111068556/221395872-09884f4a-1602-45a9-8e76-cadab867e16d.png">


## The way git used  
### Workflow
<img width="694" alt="image" src="https://user-images.githubusercontent.com/111068556/221395995-1d22ea0e-c879-4a51-8d15-339a3b0d1d02.png">

1. 工作区：即你在你本机电脑上初始化创建的一个包含.git文件的目录,或者说写代码的地方 

2. Stage暂存区：版本库就是.git文件，包含版本信息，使用add可以将本地工作区的版本信息添加到stage中，但并未到分支中  

3. Commit本地库：本地库，用于存储文件的历史版本 

### Initial configuration
1. 配置用户名
 
`git config --global user.name "sials"`

2. 配置用户邮箱

`git config --global user.email "silaschw0817@gmail.com"`


3. 配置大小写敏感

`git config --global core.ignorecase false`

4. 查看Git的配置信息可以用下面的命令：

`git config --list`

<img width="570" alt="image" src="https://user-images.githubusercontent.com/111068556/221397910-e5f71ba1-dfe8-490f-90e5-ab1b9e15c986.png">


5. 创建git本地仓库

`git init`

<img width="564" alt="image" src="https://user-images.githubusercontent.com/111068556/221398014-03a891b3-f446-4774-bc66-444892b2b65a.png">

### Adds a file to the local repository

1. 在刚才git init的目录下创建一个txt文档，里面写上文本

<img width="332" alt="image" src="https://user-images.githubusercontent.com/111068556/221398113-48b9dc20-670e-4ad1-be3e-4c3dbf18c250.png">

2. 查看工作区结果

<img width="551" alt="image" src="https://user-images.githubusercontent.com/111068556/221398148-25671500-8242-46a6-8683-3f519914f716.png">

发现为未提交状态，尝试提交

3. 提交到stage缓冲区中

`#添加到缓冲区`

`git add test.txt`


`#撤出缓冲区`

`git rm --cached test.txt`

发现已经成功添加到缓冲区

<img width="500" alt="image" src="https://user-images.githubusercontent.com/111068556/221398251-f7dd8c71-9fe6-4663-8ac3-1fbb46c6cbe9.png">

目前文件提交到了stage中，但并未commit到本地版本库，使用如下命令添加到本地版本库

`git commit test.txt`

添加之后，会出现下图提交注释页面

<img width="486" alt="image" src="https://user-images.githubusercontent.com/111068556/221398304-9fc45b0f-6b8d-46ac-a565-2edad326e5cd.png">

添加注释，点击【i】进入编辑状态,点击esc退出编辑状态,按【shift + ;】输入:,输入【wq】保存, 出现如下界面

<img width="565" alt="image" src="https://user-images.githubusercontent.com/111068556/221398714-787d233d-228d-48e2-becd-b3993289ae51.png">


### Viewing historical versions

`#查看历史版本-详细信息`

`git log`

`#查看历史版本-一行`

`git log --pretty=oneline`

`#以哈希值为标识显示`

`git log --oneline`

`#可以看见head的版本`

`git reflog --oneline`


查看详细信息
<img width="472" alt="image" src="https://user-images.githubusercontent.com/111068556/221398809-bb090cbd-5248-4b0b-a709-7e6c70d0d952.png">

查看历史版本的简略信息(一行一条版本信息)
<img width="783" alt="image" src="https://user-images.githubusercontent.com/111068556/221398845-a7391d86-e18d-448c-a88c-37461ec5c724.png">

以哈希值为表示显示版本信息
<img width="528" alt="image" src="https://user-images.githubusercontent.com/111068556/221398859-7a4c5028-71ef-445c-9eb7-ce6f4e3eef0f.png">

### Version forward and backward
1. 首先需要使用git reflog查看所有的版本和索引

2. 后退
`#后退一个版本`

`git reset --hard HEAD^ `

`#后退两个版本 `

`git reset --hard HEAD^^`

`#后退n个版本（可以用～来选择多步）`

`git reset --hard HEAD～n`

3. 根据索引选择版本

‘git reset --hard 哈希索引’


### Delete the local library file

1. rm的命令

`rm <filename>.txt `

2. 此时，删除文件在缓冲区中

3. git要求将删除文件也记录下来

`#首先提交缓冲区删除的文件`

`git add delet.txt`

`#然后commit到本地库`

`git commit -m 'delete file' delet.txt`


### Files comparison  

可以比较文件名

`git diff 文件名`




## Branch  

### What is a branch?  

是指在版本开发的过程中，使用多条线同时推进多个任务

同时并行推进多个功能的开发

分支中出现问题，可以及时停止，不会对主分支产生影响

<img width="647" alt="image" src="https://user-images.githubusercontent.com/111068556/221403155-3bbb1f66-f8f1-4a77-a210-bb2f66d729eb.png">

### Branch operation  

`#查看分支`

`git branch -v`

`#创建分支`

`git branch 分支名`

`#切换分支 `

`git checkout 分支名`

`#合并分支`

`git merge 分支名`

## Connect to remote library 


登陆github，点击加号选择new repository

远程库的地址：https://github.com/...... 在github上复制

git可以给地址取别名

`#展示所有地址别名`

`git remote -v `

`#给地址赋别名`

`git remote add 别名 url `

`#例如`

`git remote add silaschw https://github.com/xxxxxxxx/myfirsttest.git`


### Link the local rep to the remote rep

`git push mygithuburl master`


### Clone a remote the as a local rep   

`git clone 远程库的url`

 

