## 本项目实现的最终作用是基于JSP实现一个C语言教学网站平台
## 分为2个角色
### 第1个角色为教师角色，实现了如下功能：
 - 公告管理
 - 发布作业
 - 在线自测管理
 - 提交留言
 - 教学视频管理
 - 教师登录
 - 留言板管理
 - 观看视频
 - 资料下载
 - 资料下载管理
### 第2个角色为学生角色，实现了如下功能：
 - 在线自测
 - 学生登录
 - 提交留言
 - 查看首页
 - 观看教学视频
## 数据库设计如下：
# 数据库设计文档

**数据库名：** cyuyanstudysite

**文档版本：** 


| 表名                  | 说明       |
| :---: | :---: |
| [t_admin](#t_admin) | 管理员表 |
| [t_banji](#t_banji) |  |
| [t_doc](#t_doc) |  |
| [t_gonggao](#t_gonggao) |  |
| [t_jiandati](#t_jiandati) |  |
| [t_kecheng](#t_kecheng) |  |
| [t_liuyan](#t_liuyan) |  |
| [t_shipin](#t_shipin) |  |
| [t_stu](#t_stu) |  |
| [t_tea](#t_tea) |  |
| [t_timu](#t_timu) |  |
| [t_user](#t_user) | 用户表 |
| [t_zhuanye](#t_zhuanye) |  |
| [t_zuoye](#t_zuoye) |  |

**表名：** <a id="t_admin">t_admin</a>

**说明：** 管理员表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | UserId |   int   | 10 |   0    |    N     |  Y   |       | 用户ID  |
|  2   | username |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 用户名  |
|  3   | userPw |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 密码  |

**表名：** <a id="t_banji">t_banji</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       | 自增主键  |
|  2   | name |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 名字  |
|  3   | zhuanye_id |   int   | 10 |   0    |    Y     |  N   |   NULL    | 专业ID  |
|  4   | del |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 是否删除  |

**表名：** <a id="t_doc">t_doc</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | ID |   varchar   | 255 |   0    |    N     |  Y   |       | 主键  |
|  2   | title |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 标题  |
|  3   | content |   text   | 65535 |   0    |    Y     |  N   |   NULL    | 内容  |
|  4   | fujian |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 附件  |
|  5   | fujianYuanshiming |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 附件原名  |
|  6   | shijian |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 时间  |
|  7   | del |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 是否删除  |

**表名：** <a id="t_gonggao">t_gonggao</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | ID |   varchar   | 255 |   0    |    N     |  Y   |       | 主键  |
|  2   | title |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 标题  |
|  3   | content |   varchar   | 5000 |   0    |    Y     |  N   |   NULL    | 内容  |
|  4   | shijian |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 时间  |

**表名：** <a id="t_jiandati">t_jiandati</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       | 自增主键  |
|  2   | name |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 名字  |
|  3   | daan |   varchar   | 5000 |   0    |    Y     |  N   |   NULL    | 答案  |
|  4   | del |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 是否删除  |

**表名：** <a id="t_kecheng">t_kecheng</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       | 自增主键  |
|  2   | name |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 名字  |
|  3   | jieshao |   varchar   | 5000 |   0    |    Y     |  N   |   NULL    | 介绍  |
|  4   | del |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 是否删除  |

**表名：** <a id="t_liuyan">t_liuyan</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   varchar   | 255 |   0    |    N     |  Y   |       | 主键ID  |
|  2   | title |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 标题  |
|  3   | content |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 内容  |
|  4   | shijian |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 创建时间  |
|  5   | user_id |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 用户ID  |

**表名：** <a id="t_shipin">t_shipin</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   varchar   | 255 |   0    |    N     |  Y   |   ''    |   |
|  2   | title |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 标题  |
|  3   | content |   varchar   | 5000 |   0    |    Y     |  N   |   NULL    | 内容  |
|  4   | fujian |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 附件  |
|  5   | fujianYuanshiming |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 附件原名  |
|  6   | shijian |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 创建时间  |
|  7   | del |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 是否删除  |

**表名：** <a id="t_stu">t_stu</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       | 自增主键  |
|  2   | xuehao |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 学号  |
|  3   | name1 |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 名称  |
|  4   | sex |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 性别  |
|  5   | age |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 年龄  |
|  6   | banji_id |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 班级ID  |
|  7   | ruxueshijian |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  8   | del |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 是否删除  |

**表名：** <a id="t_tea">t_tea</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       | 自增主键  |
|  2   | bianhao |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 编号  |
|  3   | name |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 名字  |
|  4   | sex |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 性别  |
|  5   | age |   int   | 10 |   0    |    Y     |  N   |   NULL    | 年龄  |
|  6   | del |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 是否删除  |

**表名：** <a id="t_timu">t_timu</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       | 自增主键  |
|  2   | NAME |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 名字  |
|  3   | xuanxianga |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | A选项  |
|  4   | xuanxiangb |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | B选项  |
|  5   | xuanxiangc |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | C选项  |
|  6   | xuanxiangd |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | D选项  |
|  7   | daan |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 答案  |
|  8   | fenshu |   int   | 10 |   0    |    Y     |  N   |   NULL    | 分数  |
|  9   | del |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 是否删除  |

**表名：** <a id="t_user">t_user</a>

**说明：** 用户表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | ID |   varchar   | 255 |   0    |    N     |  Y   |       | 主键  |
|  2   | loginname |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 登录名称  |
|  3   | loginpw |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 登录密码  |
|  4   | xuehao_jiaoshihao |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 学生教师关联ID  |
|  5   | type |   int   | 10 |   0    |    Y     |  N   |   NULL    | 类型  |

**表名：** <a id="t_zhuanye">t_zhuanye</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       | 自增主键  |
|  2   | name |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 名字  |
|  3   | jieshao |   text   | 65535 |   0    |    Y     |  N   |   NULL    | 介绍  |
|  4   | del |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 是否删除  |

**表名：** <a id="t_zuoye">t_zuoye</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | ID |   varchar   | 255 |   0    |    N     |  Y   |       | 主键  |
|  2   | mingcheng |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 名称  |
|  3   | fujian |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 附件  |
|  4   | fujianYuanshiming |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 附件原名  |
|  5   | shijian |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 时间  |
|  6   | del |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 是否删除  |

**运行不出来可以微信 javape 我的公众号：源码码头**
