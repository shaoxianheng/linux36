***一、systemd***

系统初始化程序，系统开始的第一个进程，*pid*为*1*

*![img](https://img-blog.csdn.net/20171107003320459?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvc2t5X19tYW4=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/Center)
*

***\*二、systemctl\**命令**

*systemctl list-units      ##*列出当前系统服务的状态

*systemctl list-unit-files    ##*列出服务的开机状态

*systemctl status sshd      ##*查看指定服务的状态

*systemctl stop sshd       ##*关闭指定服务

*systemctl start sshd       ##*开启指定服务

*systemctl restart sshd     ##*从新启动服务

*systemctl enable sshd      ##*设定指定服务开机开启

*systemctl disable sshd     ##*设定指定服务开机关闭

*systemctl reload sshd      ##*使指定服务从新加载配置

*systemctl list-dependencies sshd  ##*查看指定服务的倚赖关系

*systemctl mask sshd      ##*冻结指定服务

*systemctl unmask sshd      ##*启用服务

*systemctl set-default multi-user.target ##*开机不开启图形

*systemctl set-default graphical.target ##*开机启动图形

*setterm         ##*文本界面设定*color*

*![img](https://img-blog.csdn.net/20171010164347786?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvc2t5X19tYW4=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/Center)
*

**三、服务状态**

*systemctl  status*   服务名称

![img](https://img-blog.csdn.net/20171010164445590?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvc2t5X19tYW4=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/Center)

*loaded       ##*系统服务已经初始化完成，加载过配置

*active*（*running*）    *##*正有一个或多个程序正在系统中执行， *vsftpd*就是这种模式

*atcive*（*exited*）    *##*僅執行一次就正常結束的服務， 目前並沒有任何程序在系統中執行

*atcive*（*waiting*）    *##*正在執行當中，不過還再等待其他的事件才能继续处理

*inactive      ##*服务关闭

*enbaled      ##*服务开机启动

*disabled      ##*服务开机不自启

*static         ##*服务开机启动项不可被管理

*failed         ##*系统配置错误