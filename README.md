免费 IPv6 大学
1.注册azure学生优惠（需要edu邮箱）
白嫖微软学生福利——通过Azure学生订阅创建一台免费的云服务器（每年可续期）-CSDN博客

手把手教你白嫖微软Azure学生免费服务器及配置教程（IPv4+IPv6）_azure ipv6-CSDN博客

2.创建虚拟机及配置（ipv4 + ipv6）
将双堆栈网络添加到现有虚拟机 - Azure Virtual Network | Microsoft Learn

ssh连接虚拟机运行代码：
1.更新系统并安装依赖
sudo apt update -y && sudo apt upgrade -y
sudo apt 更新 -y && sudo apt 升级 -y

sudo apt install -y curl socat wget

2.使用 wget 或直接下载运行脚本
wget -qO- https://raw.githubusercontent.com/vaxilu/x-ui/master/install.sh | sudo bash
wget -qO- https://raw.githubusercontent.com/vaxilu/x-ui/master/install.sh |须藤巴什

3.开放防火墙端口
sudo ufw allow 54321/tcp sudo ufw allow 12345/tcp sudo ufw allow 22/tcp sudo ufw enable # 如果未启用防火墙 sudo ufw reload
sudo ufw 允许 54321/tcp sudo ufw 允许 12345/tcp sudo ufw 允许 22/tcp sudo ufw 启用 #如果未启用防火墙 sudo ufw reload

4.启用 BBR
echo "net.core.default_qdisc=fq" | sudo tee -a /etc/sysctl.conf echo "net.ipv4.tcp_congestion_control=bbr" | sudo tee -a /etc/sysctl.conf sudo sysctl -p
回显“net.core.default_qdisc = fq”| sudo tee -a /etc/sysctl.conf 回显“net.ipv4.tcp_congestion_control = bbr”| sudo tee -a /etc/sysctl.conf sudo sysctl -p

5.检查 BBR 是否生效
lsmod | grep bbr

6.重启
sudo reboot  sudo 重启

浏览器运行x-ui(ip:54321)
默认用户名和密码：admin

3.使用X-ui和v2rayN进行虚拟机代理
实现校园网IPv6免流量上网与科学上网 | V2ray教程：X-ui与v2rayN ~ 极星网
