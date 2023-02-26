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


### Viewing historical versions


### Version forward and backward


### Delete the local library file


### Files comparison  



## Branch  
### What is a branch?  
### Branch operation  

## Connect to remote library 
### Push the local rep to the remote rep
### Clone a remote the as a local rep   

## Reference

 
