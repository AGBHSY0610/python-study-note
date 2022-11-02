# 安装git

前往[git官网](https://git-scm.com/downloads)进行下载

下载完成后，打开git bash，自报家门

    $ git config --global user.name "Your Name" #向git上报名字
    $ git config --global user.email "email@example.com" #向git上报邮箱

# 创建版本库（主要是讲免费仓库github）

## 1. 创建新的空目录

    $ mkdir ?  # 创建？文件夹

    $ cd ? # 进入？文件夹

    $ pwd # 显示当前目录

    $ 

## 2. 把目录转化为git可管理的仓库

    $ git init # 将目录转化为可管理的仓库

    $ ls -ah # 看到隐藏的.git目录

## 3. 向仓库添加文件

    $ git add ?.? # 添加?.?文件到仓库

    $ git commit -m "?" # 告诉git把文件提交到仓库，-m是本次提交的说明

# 远程仓库

## 1. 创建SSH Key

    $ ssh-keygen -t rsa -C youremail@example.com(示例邮箱)

一路回车使用默认值即可，无需设置密码。

完成后，可在用户主目录里可以看到.ssh目录，里面有id_rsa和id_rsa.pub文件，这两个是密钥对，id_rsa是私钥，不能泄露，id_rsa.pub是公钥，可以告诉别人

## 2. 在github导入密钥

登录github，找到右上角头像图标，进入setting，找到SSH and GPG keys，new一个SSH key。把公钥id_rsa.pub用txt文本阅读器打开（可以用`$ open ~/.ssh`命令直接打开），将id_rsa开头的一长串密钥拷贝到github上。利用git和github之间利用SSH进行加密

## 3.