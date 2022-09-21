# Command

Created: June 6, 2022 3:17 PM
Last Edited Time: August 22, 2022 6:33 AM
Status: In Progress 🙌
Type: linux

# WSL

1. wsl没有systemctl指令
2. WSL开启ssh (Ubuntu):`sudo /etc/init.d/ssh start`
3. 利用WSL2作为测试环境在局域网访问
    1. [链接参考](https://blog.csdn.net/cf313995/article/details/108871531)
    2. `netsh interface portproxy add v4tov4 listenaddress=192.168.92.163 listenport=9426 connectaddress=172.30.135.225 connectport=9426`
        1. 192.168.92.163:本机ip，172.30.135.225：wsl2 ip
    3. `netsh interface portproxy show all`
        1. 查看所有端口转发信息
    4. `netsh interface portproxy delete v4tov4 listenport=9426 protocol=tcp`
        1. 删除端口9426的端口转发