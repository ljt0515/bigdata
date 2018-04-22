修改 /etc/inittab 文件，将“id:5:initdefault:”这一行的"id:"后的数字（默认为5）改为 3即可。
Linux将X-Window（简称X）仅仅视作一个程序，而不捆绑于其内核之中。在UNIX/Linux中一般将运行级别分为7级（一说九级，但实际应用为六级，保留一级）：
0 系统停机
1 单用户模式
2 多用户模式
3 网络多用户模式
4 保留
5 X11模式（即进入图形界面模式）
6 重起
要想修改Linux开机的启动模式（控制台或图形界面等），只需修改/etc/inittab文件。
/etc/inittab文件（部分）：
# Default runlevel. The runlevels used by RHS are:
#   0 - halt (Do NOT set initdefault to this)
#   1 - Single user mode
#   2 - Multiuser, without NFS (The same as 3, if you do not have networking)
#   3 - Full multiuser mode
#   4 - unused
#   5 - X11
#   6 - reboot (Do NOT set initdefault to this)
# 
id:5:initdefault:
要想修改启动级别，将“id:5:initdefault:”这一行的"id:"后的数字（默认为5）改为你要的级别即可。
注意：不要改为0，0表示关机；也不要改为6，否则开机就不停的重启了~