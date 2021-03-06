---
---

# 光盒连 VPC

本篇指南旨在帮助用户使用光格 SD-WAN 服务实现光盒客户端与云平台 VPC 私有网络主机网络互通。 

## 总览

下图展示了本指南所要构建的网络拓扑。

![](../_images/cpe_connect_vpc_topology.png)

## 操作

第一步: 创建 WAN 网。


WEB 控制台，点击左边导航条中的“光格 SD-WAN”，接着在右边区域点击“创建企业广域网”按钮, 输入名称即可创建专属 WAN 网。

[![](../_images/create_wan_net.png)](../_images/create_wan_net.png)

    注意：此步骤只针对首次使用光格 SD-WAN 服务的用户。

第二步: 创建光盒接入点。


用户把光盒插入电源, 并将 Internet 链路插入光盒WAN口, 然后登录 WEB 平台, 
点击左边导航条中的“光格 SD-WAN -> 总览”, 接着在右边区域点击"创建接入点", 选择"光盒"类型并填入相应的信息即可。

[![](../_images/create_wan_cpe.png)](../_images/create_wan_cpe.png)

    注意：光盒序列号在光盒背面可以找到, 格式类似: 1c2c997dfb81。

第三步: 配置光盒。


点击创建好的接入点, 进入详情页即可配置光盒。
    
[![](../_images/describe_wan_cpe.png)](../_images/describe_wan_cpe.png)   

通常, 配置 LAN 口, 设置好光盒的 LAN 网段、网关地址并启动 DHCP 即可。 
    
[![](../_images/lan_config.png)](../_images/lan_config.png)

    注意：配置之后需要点击"应用修改＂以生效。

第四步: 创建边界路由器。


WEB 控制台，点击左边导航条中的“网络与 CDN -> 边界路由器”, 点击"创建"即可创建边界路由器。

[![](../../network/_images/intranet_router.png)](../../network/_images/intranet_router.png)

第五步: 将 VPC 私有网络关联到边界路由器。


点击创建好的边界路由器进入边界路由器详情页, 然后点击"关联 VPC 私有网络", 选择主机所在私有网络以关联边界路由器。

[![](../_images/intranet_router_vxnet2.png)](../_images/intranet_router_vxnet2.png)

第六步: 为 VPC 私有网络配置内网路由策略。


在边界路由器详情页, 点击"路由设置", 进入到内网路由策略配置页面, 设置内网路由策略。

[![](../_images/intranet_router_detail_rule.jpg)](../_images/intranet_router_detail_rule.jpg)

    注意：
    1. 内网路由策略中的边界路由器类型选物理边界路由器。
    2. 内网路由策略中的目标网段设置为光盒的 LAN 网段。
    3. 设置好内网路由策略后,需要点击"应用修改＂以生效。

如果需要批量添加光盒网络到内网路由策略，可以参考：[基于光盒目录添加内网路由策略](cpe_directory.html)。

第七步: 创建网关接入点。


WEB 控制台， 点击左边导航条中的“光格 SD-WAN -> 总览”, 接着在右边区域点击"创建接入点", 
选择"网关"类型, 并选择刚才配置的边界路由器, 然后填入相应信息即可创建网关接入点。

[![](../_images/create_vpc_wan_access.png)](../_images/create_vpc_wan_access.png)

完成以上步骤后, 光盒客户端即可与 VPC 私有网络主机互通。
