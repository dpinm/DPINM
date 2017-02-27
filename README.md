# DPINM
##The develop inmformation about dpinm
###3月份目标:
1. 支持分布式、并发以及数据备份的INMD。
2. 支持organization-based数据分割
3. 支持distributed transaction

###目标成果：
1. runnable DPINM system：insert与query语句，数据划分与事务
2. 项目文档：类图（以及说明类的基本用途），各模块处理流程，重要函数方法的注释

##张剑

###需要完成的功能
1. 客户端Master 多线程访问 完成度 20%
2. Replication 完成度 0%
3. 打印元数据统计信息 完成度 0%
4. 测试 and 文档  完成度 0%
5. 单机版INM client 合并 完成度 0%

###接口
1. inm.cfg文件中，静态参数与动态参数区分开
2. 需添加参数：
2.1 query_processing_mode （1 or 2）指明查询处理采用的方法
2.2 object_division （true or false）是否拆分大对象
2.3 organization_unification_method （1 or 2）指明采用的organization detection的方法

###其它模块需要接口

##马杨
1. organization detecting新的设计策略实现  完成度30%
2. organization unifying新的设计策略实现  完成度0%
##徐晶
1. 查询新处理流程实现  完成度45%
2. 查询类图以及处理流程文档  完成度0%
##陈诗雅
