物联网 SaaS 托管为用户提供更适合物联网场景的一站式、高可用的 SaaS 托管服务，用户可以通过物联网 SaaS 托管快速部署自研节点与 MySQL 节点。



## 自研节点

物联网 SaaS 托管自研节点通过流量驱动的自动弹性扩缩容能力，可有效降低用户的服务器成本与运维投入。同时支持托管任意语言和框架编写的物联网 SaaS，存量迁移几乎不需要改造代码。

### 功能特性

#### 自动部署

上传镜像即可一键开始部署您的服务，无需提前规划资源容量、购买服务器，也无需安装、运维、扩展您的集群管理基础设施。

#### 支持任意语言、任意容器镜像

您可以使用任何语言、任何框架编写应用，甚至直接使用公共的容器镜像。

#### 弹性伸缩

实例（容器）数量可根据服务的实际流量大小纵向扩容或缩减，当无任何请求时，实例（容器）数量甚至可以被缩减到0，不产生任何资源消耗。这一动态扩缩过程由系统自动完成，无需人工管理，最终您只需为实际使用的所有实例（容器）资源进行付费。

#### 对外域名
每个服务都包含一个系统自动生成的默认域名（您也可额外绑定自定义域名），可被用于访问和传入请求。请求方无需感知该服务具体有几个版本，而是将服务视为一个整体。
#### 流量分配
当有请求传入服务时，根据您事先配置的流量分配模式和规则，系统将本次请求路由到对应的版本。

### 服务版本说明

每个服务都可创建多个版本，每个版本对应着一组实例（容器）资源。用户可通过流量分配为不同版本指定不同的流量百分比，即可一键完成灰度。适用于快速回滚、灰度发布等场景。本文以服务 TestA、TestB 域名为例进行说明，如下图所示：
<img src="https://main.qcloudimg.com/raw/2d449c076b4162bf42345efa584c3c53.png" style="width: 718px;"></img>

## MySQL 节点

物联网 SaaS 托管 MySQL 节点提供了腾讯云自研的新一代高性能高可用的企业级分布式云数据库。融合了传统数据库、云计算与新硬件技术的优势，可实现超百万级 QPS 的高吞吐，128TB 海量分布式智能存储，保障数据安全可靠。

### 功能特性

#### 完全兼容

物联网 SaaS 托管 MySQL 节点将开源数据库的计算和存储分离，存储构建在腾讯云分布式云存储服务之上，计算层全面兼容开源数据库引擎 MySQL 5.7、8.0，业务无需改造即可平滑迁移。

#### 超高性能

单节点百万 QPS 的超高性能，可以满足高并发高性能的场景，保证关键业务的连续性，并可进一步提供读写分离以及读写扩展性。

#### 海量存储

最高128TB的海量存储，无服务器 Serverless 架构，自动扩缩容，自动故障检测修复，并按实际使用量计费，不用不计费，轻松应对业务数据量动态变化和持续增长。自动维护数据多个副本，保障数据安全可靠。

#### 秒级故障恢复

计算节点实现了无状态，支持秒级的故障切换和恢复，即便计算节点所在的物理机宕机也可以在一分钟之内恢复。
