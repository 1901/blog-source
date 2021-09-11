---
title: "Sqlite 基础知识"
date: 2012-10-14T14:49:48+08:00
tags: ["sqlite", "database"]
categories: ["技术相关"]
# bookComments: false
# bookSearchExclude: false
---

sqlite官方网站：<a href="http://www.sqlite.org" target="_blank">www.sqlite.org</a>

## 启动 sqlite (打开终端，输入命令)
打开当前目录下的test.db数据库，如果没有这个文件刚创建一个数据库。
```bash
$ sqlite3 test.db
```
    

- 查看sqlite帮助内容
```bash
sqlite> .help
```

- 列出当前数据库中的所有表名
```bash
sqlite> .tables
```

- 执行一个sql文件
```bash
sqlite> .read f.sql
```

- 查看建表语句，指定参数则查看指定表的建表语句，不指定参数时查看所有表的建表语句
```bash
sqlite> .schema
sqlite> .schema table
```


## 建表示例
```sql
CREATE TABLE kxtest(
    id INTEGER PRIMARY KEY AUTOINCREMENT, 
    name VARCHAR(100) NOT NULL,
    sex INTEGER DEFAULT 0,
    date DATE
);
```
    
## 其他
使用自增长字段时，引擎会自动产生一个sqlite_sequence表，用于记录每个表的自增长字段的已使用的最大值。

- 用户可以使用下面的查询语句查询各个表自动增长的记录。
```sql
sqlite> select * from sqlite_sequence;
```
    

- 用户可以使用下面的语句清空自动增长记录。
```sql
sqlite> delete from sqlite_sequence;
```

说明：SQLite中没有 `truncate` 命令清空表，如果需要清空表，可以先删除表中的记录，再从 `sqlite_sequence` 中删除相应的记录
