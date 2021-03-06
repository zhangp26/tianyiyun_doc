---
---

# 私有网络[¶](#api-vxnet "永久链接至标题")

通过青云的SDN（软件定义网络）技术，您可以快速地搭建您专属的私有云环境。 相比于基础网络而言，这个网络可以提供100%的安全隔离，而且有丰富的工具帮助您进行自动化管理。 要使用青云网络，请创建一个路由器 ( 路由器相关 API 可参见 [_路由器_](../router/index.html#api-router) )， 然后再创建一个或多个私有网络并连接到这个路由器， 最后创建主机并加入到这些私有网络即可。

私有网络用于主机之间互联，它类似物理世界中使用交换机（L2 Switch）组成的局域网。 私有网络之间是100%隔离的。

青云私有网络有两种类型

受管私有网络： 可以使用青云路由器来配置和管理其网络，使网络搭建更方便快捷。

自管私有网络： 需要您自行配置和管理网络，适用于对底层网络有特殊需求的用户。

*   [DescribeVxnets](describe_vxnets.html)
*   [CreateVxnets](create_vxnets.html)
*   [DeleteVxnets](delete_vxnets.html)
*   [JoinVxnet](join_vxnet.html)
*   [LeaveVxnet](leave_vxnet.html)
*   [ModifyVxnetAttributes](modify_vxnet_attributes.html)
*   [DescribeVxnetInstances](describe_vxnet_instances.html)
