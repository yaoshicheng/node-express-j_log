参考：https://github.com/ecitlm/js-log-report


      http://www.ruanyifeng.com/blog/2013/01/javascript_source_map.html

本例安装mysql数据库

Mysql建表：

DROP TABLE IF EXISTS `j_log`;
CREATE TABLE `j_log` (
  `id` INT(10) NOT NULL AUTO_INCREMENT COMMENT 'id号',
  `os_version` CHAR(10) DEFAULT NULL COMMENT '系统版本号',
  `msg` VARCHAR(2000) DEFAULT NULL COMMENT '错误信息',
  `error_url` VARCHAR(255) DEFAULT NULL COMMENT '错误所在的url',
  `line` INT(10) DEFAULT NULL COMMENT '错误所在的行',
  `col` INT(10) DEFAULT NULL COMMENT '错误所在的列',
  `error` VARCHAR(255) DEFAULT NULL COMMENT '具体的error对象',
  `url` VARCHAR(255) DEFAULT NULL,
  `browser` VARCHAR(255) DEFAULT NULL COMMENT '浏览器类型',
  `product_name` CHAR(255) CHARACTER SET utf8 DEFAULT '' COMMENT '产品名称',
  `error_time` CHAR(50) DEFAULT NULL COMMENT '时间戳',
  `os` CHAR(10) DEFAULT NULL COMMENT '系统类型',
  `extend` VARCHAR(255) DEFAULT NULL COMMENT '业务扩展字段、保存JSON字符串',
  `ua` VARCHAR(255) DEFAULT NULL,
  PRIMARY KEY (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

Mysql插值：
INSERT INTO j_log 
(id, os_version, msg,error_url,line,col,error,url,browser,product_name,error_time,os,extend,us) 
VALUES 
(1,"学习 PHP", "菜鸟教程", "1213",19,10,"324","ewfw","324","ewfw","324","ewfw","324","ewfw");
