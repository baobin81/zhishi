# 如果系统没有screen，得安装
## 安装
    yum install screen
## 安装后，打印帮助信息，可初步了解screen的功能
    screen -h

# 常用操作
## 新建一个叫yourname的窗口
    screen -S yourname 
说明：S 是大写



##打开存在的窗口
### 离开后，忘记名称 查看有几个session窗口
    screen -ls 
### 如何读取session回到离开的状态
    screen -r yourname

只能读取状态是：Detached的session 窗口
不读取Attached



## 离开窗口
###隐藏当前窗口回到终端控制台
  ctrl+a+d  操作说明：按住ctrl键不放，然后按A 然后按D （这个命令是结束当前窗口，返回到终端控制台）
###隐藏当前窗口回到另外一个窗口
screen -d -r yourname -> 结束当前session并回到yourname这个session
## 销毁窗口
1. 进入窗口(screen -r yourname)
2. 执行exit
关闭窗口，相当于windows关闭窗口，这个窗口永完消失