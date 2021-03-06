# mybatis-generator
mybatis生成器
> 使用时请删除自动生成文件夹:`com.yangmm.mapper`, `com.yangmm.pojo`, `src/main/resources/mapper` 
> 为了方便查看效果而保留。

# 修改配置generatorConfig.xml  
- 修改数据库连接 
```
        <jdbcConnection driverClass="com.mysql.jdbc.Driver"
                        connectionURL="jdbc:mysql://localhost:3306/my-database"
                        userId="root"
                        password="root">
        </jdbcConnection>
``` 

- 修改导出的表格 
```
<!-- 数据库表 -->
<table tableName="users"></table> 
...
```

- 测试表格的表结构
```
-- ----------------------------
-- Table structure for users
-- ----------------------------
DROP TABLE IF EXISTS `users`;
CREATE TABLE `users` (
  `id` varchar(64) NOT NULL COMMENT '主键id 用户id',
  `username` varchar(32) NOT NULL COMMENT '用户名 用户名',
  `password` varchar(64) NOT NULL COMMENT '密码 密码',
  `nickname` varchar(32) DEFAULT NULL COMMENT '昵称 昵称',
  `realname` varchar(128) DEFAULT NULL COMMENT '真实姓名',
  `face` varchar(1024) NOT NULL COMMENT '头像',
  `mobile` varchar(32) DEFAULT NULL COMMENT '手机号 手机号',
  `email` varchar(32) DEFAULT NULL COMMENT '邮箱地址 邮箱地址',
  `sex` int(11) DEFAULT NULL COMMENT '性别 性别 1:男  0:女  2:保密',
  `birthday` date DEFAULT NULL COMMENT '生日 生日',
  `created_time` datetime NOT NULL COMMENT '创建时间 创建时间',
  `updated_time` datetime NOT NULL COMMENT '更新时间 更新时间',
  PRIMARY KEY (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COMMENT='用户表 ';
``` 

