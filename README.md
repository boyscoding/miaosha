# 校园选课基础秒杀项目 

![license](https://img.shields.io/github/license/alibaba/dubbo.svg)

|       📘       |       🛫       |         🐱         |           🏛           |             🚀              |
| :-----------: | :-----------: | :---------------: | :-------------------: | :------------------------: |
| [介绍](#介绍) | [演示](#演示) | [技术栈](#技术栈) | [基础项目](#基础项目) | [Quick Start](#QuickStart) |

[【Spring Boot构建电商基础秒杀项目】](https://www.imooc.com/learn/1079)免费课程

## 介绍

<code>miaosha</code>:Java实现的秒杀网站，基于Spring Boot 2.X。 

**谢谢您对本项目的支持** <br/>
**请点击此处进行**[Star](https://github.com/boyscoding/jseckill/stargazers)

**GitHub** 地址为[https://github.com/liushaoming/jseckill](https://github.com/boyscoding/jseckill)

建议访问GitHub以获取更多分布式项目源码[https://github.com/boyscoding?tab=repositories](https://github.com/liushaoming?tab=repositories)

## 技术栈

- Spring Boot 2.X
- MyBatis
- Redis, MySQL
- Thymeleaf + Bootstrap
- RabbitMQ
- Zookeeper, Apache Curator

# 基础项目

[Spring Boot构建电商基础秒杀项目笔记](https://github.com/boyscoding/miaosha/blob/master/docs/base.md)

* 效果展示
  * 注册
  * 商品列表
  * 商品详情
* 项目架构
* 要点和细节
  * Data Object/Model/View Object
  * 通用返回对象
  * 处理错误信息
  * 异常拦截器处理自定义异常
  * 跨域问题
  * 优化校验规则
    * 校验规则
    * 封装校验结果
    * 创建校验器/使用校验
  * 用户业务
    * 短信发送业务
    * 注册业务
    * 登录业务
  * 商品业务
    * 商品添加业务
    * 获取商品业务
    * 查询所有商品
  * 交易业务
    * 下单业务
    * 订单ID的生成
  * 秒杀业务
    * 秒杀DO/Model和VO
    * 升级获取商品业务
    * 活动商品下单业务
* 改进

# 进阶项目

[性能优化，打造亿级秒杀系统项目笔记 【上】](https://github.com/boyscoding/miaosha/blob/master/docs/advance_p1.md)

- 前言
- 进阶项目核心知识点
- 基础项目回顾
  - 项目结构—数据模型
  - 项目结构—DAO/Service/Controller结构
  - 全局异常处理类
- 项目云端部署
  - 数据库部署
  - 项目打包
  - deploy启动脚本
- jmeter性能压测
- 单机服务器并发容量问题和优化
  - 项目架构
  - 发现并发容量问题
  - Spring Boot内嵌Tomcat线程优化
  - Spring Boot内嵌Tomcat网络连接优化
  - 小结
  - 优化后的效果
  - 接下来的优化方向
- 分布式扩展优化
  - 项目架构
  - Nginx部署前端静态资源
  - Nginx反向代理处理Ajax请求
  - 开启Tomcat Access Log验证
  - Nginx反向代理长连接优化
  - 分布式扩展后的效果
  - Nginx高性能原因—epoll多路复用
  - Nginx高性能原因—master-worker进程模型
    - Ngxin进程结构
    - Master-worker高效原理
  - Nginx高性能原因—协程机制
  - 小结
  - 接下来的优化方向
- 分布式会话
  - 基于Cookie传输SessionId
  - 基于Token传输类似SessionId
  - 小结
  - 接下来的优化方向
- 查询优化之多级缓存
  - 项目架构
  - 优化商品查询接口—单机版Redis缓存
    - 序列化格式问题
    - 时间序列化格式问题
  - 优化商品查询接口—本地热点缓存
    - 本地缓存缺点
  - 缓存优化后的效果
  - Nginx Proxy Cache缓存
    - Nginx Proxy Cache缓存效果
  - Nginx lua脚本
    - lua脚本实战
  - OpenResty—Shared dic
    - Shared dict缓存效果
  - 小结
  - 接下来的优化方向
- 查询优化之页面静态化
  - 项目架构
  - CDN
    - CDN使用
    - CDN优化效果
    - CDN深入—cache controll响应头
      - 选择缓存策略
      - 有效性验证
      - 请求资源流程
    - CDN深入—浏览器三种刷新方式
      - a标签/回车刷新
      - F5刷新
      - CTRL+F5强制刷新
    - CDN深入—自定义缓存策略
    - CDN深入—静态资源部署策略
      - 部署窘境
      - 解决方法
  - 全页面静态化
    - phantomJS实现全页面静态化
  - 小结
  - 接下来的优化方向
- 优化效果总结
  - Tomcat优化
  - 分布式扩展优化
  - 缓存优化
  - CDN优化

------

[性能优化，打造亿级秒杀系统项目笔记 【下】](https://github.com/boyscoding/miaosha/blob/master/docs/advance_p2.md)

- 交易优化之缓存库存
  - 交易接口瓶颈
  - 交易验证优化
    - 用户校验缓存优化
    - 活动校验缓存优化
    - 缓存优化后的效果
  - 库存扣减优化
    - 索引优化
    - 库存扣减缓存优化
      - RocketMQ
      - 同步数据库库存到缓存
      - 同步缓存库存到数据库（异步扣减库存）
      - 异步扣减库存存在的问题
  - 小结
  - 接下来的优化方向
- 交易优化之事务型消息
  - 异步消息发送时机问题
    - 解决方法
  - 事务提交问题
    - 解决方法
  - 事务型消息
    - 更新下单流程
  - 小结
  - 接下来的优化方向
- 库存流水
  - 下单操作的处理
  - UNKNOWN状态处理
  - 库存售罄处理
  - 小结
    - 可以改进的地方
  - 接下来的优化方向
- 流量削峰
  - 业务解耦—秒杀令牌
  - 限流—令牌大闸
    - 令牌大闸限流缺点
  - 限流—队列泄洪
  - 小结
  - 接下来的优化方向
- 防刷限流
  - 验证码技术
  - 限流方案—限并发
  - 限流方案—令牌桶/漏桶
    - 令牌桶
    - 漏桶
    - 区别
  - 限流力度
  - 限流范围
  - RateLimiter限流实现
  - 防刷技术
    - 传统防刷技术
    - 黄牛为什么难防
    - 防黄牛方案
  - 小结
