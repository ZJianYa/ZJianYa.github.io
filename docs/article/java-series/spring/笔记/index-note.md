
## 快速了解

Spring Cloud 更多的是体现了一种架构思想，而并不旨在提供具体实现，有一点 cncf 的意思。  
  我们应该先从 Application Context Services 和 Common Abstractions 入手。  
Context 为应用提供了各个挂载点，以便云化应用。  
Common 则提供各种组件的抽象，以便于云化应用。  

大型的数据中心和我们想象的一定是不一样的，一定分了很多区域，既要实现区域自治，又要实现区域协调。  
区域内部时效一定很强，区域之间时效可以稍弱。  

* 什么是微服务，优缺点  
  有点: 解耦，不会关联宕机，更好维护，与组织架构对齐，快速迭代（遵守服务之前的接口）  
  缺点: 分布式的各种问题，服务之间需要通信，服务多了需要治理，需要监控，运维和测试成本增加  
  一个基本原则：业务服务和外围服务分离。外围服务提供基础能力，业务服务提供对业务的支撑，两者之间会有过渡地带。  
* 微服务组件和功能  
  * 业务应用(通常是客户端)
    * 配置外置  
    * 服务注册和发现  
      健康监测  缓存时效  Ribbon  Feign  
    * 断路，降级 （我认为所有的应用程序都不应该有降级，也不应该有缓存，不应该有业务数据）  
      * 异常统计/恢复检测/补偿处理  
    * RPC  
    * 消息订阅  
  * 外围应用（通常是服务端）  
    * 配置中心  
      有时配合网关和服务注册中心实现灰度发布或者滚动发布。  
    * 服务注册、发现、下线、启停、多副本、状态监测中心
    * 网关
      * 限流和服务调用隔离，断路保护，降级  
        流量调度/限流/负载均衡 （客户端负载均衡/服务端负载均衡)  
        容错:网络故障/熔断/降级/多副本(同时可以负载均衡，还需要能自动切换，数据一致性) / 缓存时效/自我健康监测 
    * 消息引擎服务  
      * 充当变速器，缓冲区  
    * 链路  
    * 管理:启停，多副本，扩容，调度，限流  
    * 埋点 手动/agent
    * SSO CAS
    * 监控  
      * 主机的监控 计算、存储、网络资源的监控  
      * app的监控 响应时间 服务状态 内存占用    
* 什么是云原生  
  DevOps  
  持续交付  
  微服务  
  容器  

## 目录

### 挂载点