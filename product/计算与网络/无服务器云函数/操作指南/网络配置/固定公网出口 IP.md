## 操作场景
当用户在云函数中访问数据库、微信公众号的 API 接口或其他第三方的服务时，可以使用云函数的固定公网出口 IP 功能，实现云函数网络配置的控制与管理。

云函数的固定公网出口 IP 功能具有以下特点：
- 当云函数启用固定公网出口 IP 功能后，该云函数将会获得一个随机分配的弹性公网 IP。该云函数访问公网的流量，将会基于该弹性公网 IP 统一进行转发。
- 当在云函数同时开启公网访问、内网访问并启用固定公网出口 IP 功能时，访问公网的流量会基于弹性公网 IP 进行转发，访问内网的流量会基于私有网络进行转发。

## 使用限制
- 弹性公网 IP 在同一账号的同一地域下共享。
 - 同一账号的同一地域下，已开启固定公网出口 IP 功能的云函数将共享弹性公网 IP。
 - 同一账号的同一地域下的云函数需更换固定出口 IP 时，所有云函数需关闭固定公网出口 IP 功能。再次开启此功能时，会随机产生一个新的弹性公网 IP。
- 弹性公网 IP 基于私有网络的子网共享。
 某个云函数配置了私有网络，且同时开启了固定公网出口 IP 功能，则该云函数会获得一个随机分配的弹性公网 IP。同一私有网络子网下的云函数在开启固定出口 IP 功能时，会共享此固定出口 IP。

#### 示例
为了便于您理解固定公网出口 IP 的使用限制，以下为您进行一个简单的示例说明。

假设您的账号在某地域有如下场景：
- 命名空间 A 下已创建了云函数 a 和云函数 b。
- 命名空间 B 下已创建了云函数 c 和云函数 d。
- 弹性公网 IP-x、弹性公网 IP-y 分别表示两个不同的弹性公网 IP。
 
它们的弹性公网 IP 和云函数的绑定关系如下表所示：
<table>
<tr><th rowspan=2 align="center"><b>网络配置</b></th><th colspan=2 align="center"><b>命名空间 A</b></th><th colspan=2  align="center"><b>命名空间 B</b></th></tr>
<tr><th align="center"><b>函数 a</b></th><th align="center"><b>函数 b</b></th><th align="center"><b>函数 c</b></th><th align="center"><b>函数 d</b></th></tr>
	<tr>
	</tr>
	<tr>
	<td>仅公网访问</td>
	<td>无弹性公网 IP</td>
	<td>无弹性公网 IP</td>
	<td>无弹性公网 IP</td>
	<td>无弹性公网 IP</td>
	</tr>
		<tr>
	<td>仅内网访问 </td>
	<td>无弹性公网 IP</td>
	<td>无弹性公网 IP</td>
	<td>无弹性公网 IP</td>
	<td>无弹性公网 IP</td>
	</tr>
			<tr>
	<td>公网访问且固定公网出口 IP </td>
	<td>弹性公网 IP-x</td>
	<td>弹性公网 IP-x </td>
	<td>弹性公网 IP-x </td>
	<td>弹性公网 IP-x</td>
	</tr>
			<tr>
	<td>同一私有网络访问且固定公网出口 IP </td>
	<td>弹性公网 IP-y</td>
	<td>弹性公网 IP-y</td>
	<td>弹性公网 IP-y </td>
	<td>弹性公网 IP-y</td>
	</tr>
</table>

## 操作步骤
>!每个用户在每个地域固定 IP 限额为5个。
>
1. 登录 [云函数控制台](https://console.cloud.tencent.com/scf/index?rid=19)，单击左侧导航栏中的**函数服务**。
2. 在页面上方选择云函数所在地域，单击函数名。
3. 进入“函数配置”页签，单击右上角的**编辑**。
4. 根据您的实际需求，进行该云函数的网络配置。如下图所示： 
>!
>- 云函数开启公网访问后，才可选择开启固定公网出口 IP。
>- 您无法手动选择或编辑随机生成的弹性公网 IP。
>
![](https://main.qcloudimg.com/raw/adedb9d862ec5d22a9df64b8ffdb2a01.png)
配置完成后，单击**保存**即可。

