### Database Change v0.11.1
1. 增加了tb_module.name的长度，防止过长模块名报错
2. 增加tb_action.disable_cache字段用于自动化禁用cache处理

```sql
ALTER TABLE `rap_db`.`tb_module` CHANGE COLUMN `name` `name` VARCHAR(128) NOT NULL  ;
ALTER TABLE `rap_db`.`tb_action` ADD COLUMN disable_cache TINYINT NOT NULL DEFAULT 0;
```



### Database Change v0.11.0

add mock count Oct.15 2014
增加了MOCK调用次数记录 2014-10-15

```sql
ALTER TABLE tb_project
ADD COLUMN mock_num int(10) NOT NULL
	DEFAULT 0
```

add employee id Oct.1 2014
增加员工ID 2014-10-1

```sql
ALTER TABLE tb_user
    ADD emp_id varchar(128) NULL
```