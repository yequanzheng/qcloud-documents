## 操作场景
本文介绍如何通过控制台，将专用宿主机上的云服务器 CVM 实例转换为共享宿主机 CVM 实例，满足业务灵活部署的需求。

## 注意事项
待迁移实例需注意以下事项：
- 实例需处于“已关机”状态。
- 不支持使用本地盘的实例进行迁移。可参考 [调整硬盘介质](https://cloud.tencent.com/document/product/213/31978)，将本地盘调整为云硬盘。
- 若实例已挂载增强型 SSD 型云硬盘，则可能会因硬盘本身限制导致无法选择目标实例。具体限制请参见云硬盘类型中的 [注意事项](https://cloud.tencent.com/document/product/362/2353#.E6.B3.A8.E6.84.8F.E4.BA.8B.E9.A1.B9)。

目标 CVM 需满足：与待迁移 CVM 需处于同一账号、同一地域、同一可用区下。

## 操作步骤
1. 登录云服务器控制台，选择左侧导航栏中的 **[专用宿主机](https://console.cloud.tencent.com/cvm/cdh/index)**。
2. 在“专用宿主机”页面上方，选择宿主机所在地域。
3. 选择待转换实例所属的宿主机名，进入该宿主机详情页面，单击**实例列表**页签。
4. 单击需转换实例所在行右侧的**转换为CVM实例**。如下图所示：
![](https://main.qcloudimg.com/raw/f279485cfb48b76593347e5aa7b1f3e8.png)
<dx-alert infotype="explain" title="">
如需批量迁移实例，请在列表中勾选实例后，选择列表上方的**更多操作** > **实例设置** > **转换为CVM实例**。
</dx-alert>
5. 在弹出的“转换为CVM实例”窗口中，进行如下配置。
 1. 在“选择目标配置”中，选择目标实例规格后单击**下一步**。如下图所示：
 ![](https://main.qcloudimg.com/raw/78d31a32efae843141eded58e6da86d3.png)
 2. 在”选择计费类型“中，选择目标计费类型，确认费用明细后单击**下一步**。如下图所示：
 ![](https://main.qcloudimg.com/raw/ad542b37c7eb33586b8cd2c71145e869.png)
 3. 在“关机提示”中，确认关机提示并单击**开始调整**即可。
 实例转换完成后将自启动，状态为“运行中”。您可前往 [云服务器控制台](https://console.cloud.tencent.com/cvm/instance/index) 页面查看。
