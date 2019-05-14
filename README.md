# Airport-toolkit
各類方便機場主進行安裝維護的shell腳本    
安裝使用指南請參見 [此鏈接](https://github.com/Anankke/ss-panel-v3-mod_Uim/wiki/%E5%90%8E%E7%AB%AF%E4%B8%80%E9%94%AE%E5%AE%89%E8%A3%85%E8%84%9A%E6%9C%AC)
支持系统：CentOS 7 x64 & Ubuntu 18.04 x64
脚本功能：

可选配置节点为WebAPI模式或MySQL模式
可选配置单端口多用户
可选启用BBR（using mainline kernel）
可选注册为系统服务
使用指南
安装 For CentOS 7 x64
yum install wget -y && wget https://raw.githubusercontent.com/SuicidalCat/Airport-toolkit/master/ssr_node_c7.sh && chmod +x ssr_node_c7.sh && ./ssr_node_c7.sh

安装 For Ubuntu 18.04 x64
apt-get install wget -y && wget https://raw.githubusercontent.com/SuicidalCat/Airport-toolkit/master/ssr_node_u18.sh && chmod +x ssr_node_u18.sh && ./ssr_node_u18.sh

卸载
systemctl disable ssr_node && \rm /usr/lib/systemd/system/ssr_node.service && \rm -rf /soft/shadowsocks

设置开机启动
systemctl enable ssr_node

服务启动
systemctl start ssr_node

服务停止
systemctl stop ssr_node
