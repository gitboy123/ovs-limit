# ovs-limit
<p>容器在ovs环境下的限速,可以做到限制上传和下载的流量</p>

# 使用说明
<p>1.将ovs-limit脚本 复制到/usr/local/sbin 下,执行chmod +x /usr/local/sbin/ovs-limit</p>

  <p>cp ovs-limit /usr/local/sbin & chmod +x /usr/local/sbin/ovs-limit</p>

 <p>2.限制容器某个网卡的带宽，单位为：Mbps</p>
  <p> ovs-limit is limit container nic commands, bandwidth default Mbps</p>
 <p>3.命令使用方法</p>
 <p>ovs-limit  limit <container name> <container_nic> <bandwidth></p>
 <p>ovs-limit  ulimit <container name> <container_nic></p>

 <p>例子：</p>
 <p>限制容器gw-8.254容器的eth2带宽为5M</p>
 <p>Example limit container gw-8.254 eth2 5M:</p>
 <p>  ovs-limit  limit gw-8.254 eth2 5</p>
  
 <p>解除容器gw-8.254容器的eth2带宽限制</p>
 <p>Example clear network limit:</p>
 <p>  ovs-limit  ulimit  gw-8.254 eth2</p>
  
  
