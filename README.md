# ubuntu_network
解决 ubuntu20.04vm虚拟机nat模式下网络出现问号无法上网的问题
主要就是添加DNS服务器

命令行输入如下内容
sudo vi /etc/resolv.conf

然后按a或i进入编辑模式，在最后一行添加如下内容，分别是首选DNS服务器和备选DNS服务器
nameserver 8.8.8.8
nameserver 114.114.114.114

esc，然后输入
：wq   保存退出

最后重启网络服务
service network restart
应该可以解决问题
