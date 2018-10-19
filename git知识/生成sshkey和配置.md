
# 生成ssh key
## 第1步：
创建SSH Key。在windows下查看[c盘->用户->自己的用户名->.ssh]下是否有id_rsa、id_rsa.pub文件，如果没有需要手动生成。

 `ssh-keygen -t rsa -C "baobin81@qq.com"`
### 运行这个命令说明
1. 运行这个命令的前提条件：windows中必须在git bash中运行 ，直接cmd不能运行
2. Enter file in which to save the key 公私钥保存的路径，windows默认是 C:\Users\Administrator\.ssh
3. 这个命令关键是获得公私钥，公钥放在github上，私钥给不同的工具，和github签权


## 第2步：
登录github。打开setting->SSH keys，点击右上角 New SSH key，把生成好的公钥id_rsa.pub放进 key输入框中，再为当前的key起一个title来区分每个key。


# 配置
## 显示当前的Git配置
       git config --list

## 显示全局配备
    git config --global --list


## 编辑Git配置文件

    git config -e [--global]

## 设置提交代码时的用户信息

    git config user.name  "包彬"

    git config  user.email "baobin81@qq.com"
## 设置全局提交代码时的用户信息

    git config --global user.name "包彬"

    git config --global user.email "baobin81@qq.com"