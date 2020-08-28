# fire数据库文档

**数据库名：** springcloud

**文档版本：** 0.0.1-SNAPSHOT

**文档描述：** 数据库文档生成
| 表名                  | 说明       |
| :-------------------- | :--------- |
| [tb_user](#tb_user) |  |
**表名：** <a id="tb_user">tb_user</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   bigint   | 19 |   0    |    N     |  Y   |       |   |
|  2   | user_name |   varchar   | 100 |   0    |    Y     |  N   |       | 用户名  |
|  3   | password |   varchar   | 100 |   0    |    Y     |  N   |       | 密码  |
|  4   | name |   varchar   | 100 |   0    |    Y     |  N   |       | 姓名  |
|  5   | age |   int   | 10 |   0    |    Y     |  N   |       | 年龄  |
|  6   | sex |   bit   | 1 |   0    |    Y     |  N   |       | 性别，1男性，2女性  |
|  7   | birthday |   date   | 10 |   0    |    Y     |  N   |       | 出生日期  |
|  8   | note |   varchar   | 255 |   0    |    Y     |  N   |       | 备注  |
|  9   | created |   datetime   | 19 |   0    |    Y     |  N   |       | 创建时间  |
|  10   | updated |   datetime   | 19 |   0    |    Y     |  N   |       | 更新时间  |
