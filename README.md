# Themis 
### 功能概述   
Themis,是宜信公司DBA团队开发的一款数据库审核产品。可帮助DBA、开发人员快速发现数据库中结构设计、SQL语句运行质量等问题。
#### 支持数据库
× Oracle(10g及以上)
× MySQL(5.6及以上)
#### 审核维度
× 数据库结构
× SQL文本
× SQL执行计划
× SQL执行特征
### 架构总览   
![架构图](arch.jpg)   
图中主要分为四大块，数据采集、规则解析、任务导出和web管理，存储主要使用mongodb和mysql。mysql主要用来存储pt-query-digest采集的数据，其他的数据，如oracle的采集结果，规则的初始化，任务的生成，解析的结果等都存到mongodb里。 
