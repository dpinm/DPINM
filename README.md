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
1. 客户端Master 多线程访问，完成度 90%    
>> 3/07<客户端测试代码已完成，目前同时插入语句dpinm会发生死锁，debuging> 发生死锁修改了全部底层调用接口，发现死锁后就abort事务，目前测试仍未通过。<br \> 
>> 3/10日，死锁问题已解决，测试instance0831.txt，把文件从中间分开两份，两个线程来插入，发现实例部分段错误，已告诉马杨。 
>> 还有两点问题：1 实例bug，2 query 客户端的反序列化。 告一段落。
2. Replication <原型代码ing> 完成度 15%
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
###需要完成的功能
1. organization detecting新的设计策略实现  完成度30%
2. organization unifying新的设计策略实现  完成度0%
3. 测试与文档  完成度0%

##徐晶
1. 查询新处理流程实现  完成度45%
2. 查询类图以及处理流程文档  完成度0%

##陈诗雅
1. 大对象拆分工作   完成度80%
2. 说明文档   完成度0%
