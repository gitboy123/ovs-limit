# ovs-limit
容器在ovs环境下的限速,可以做到限制上传和下载的流量

# 使用说明
将ovs-limit脚本 复制到/usr/local/sbin 下，执行chmod +x /usr/local/sbin/ovs-limit
cp ovs-limit /usr/local/sbin & chmod +x /usr/local/sbin/ovs-limit

限制容器某个网卡的带宽，单位为：Mbps
ovs-limit is limit container nic commands, bandwidth default Mbps

ovs-limit  limit <container name> <container_nic> <bandwidth>
ovs-limit  ulimit <container name> <container_nic>

例子：
限制容器gw-8.254容器的eth2带宽为5M
Example limit container gw-8.254 eth2 5M:
  ovs-limit  limit gw-8.254 eth2 5
  
解除容器gw-8.254容器的eth2带宽限制
Example clear network limit:
  ovs-limit  ulimit  gw-8.254 eth2
  
  
