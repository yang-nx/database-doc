# 数据库文档

**数据库名：** changgou_config

**文档版本：** 0.0.1-SNAPSHOT

**文档描述：** 数据库文档生成
| 表名                  | 说明       |
| :-------------------- | :--------- |
| [oauth_access_token](#oauth_access_token) |  |
| [oauth_approvals](#oauth_approvals) |  |
| [oauth_client_details](#oauth_client_details) |  |
| [oauth_client_token](#oauth_client_token) |  |
| [oauth_code](#oauth_code) |  |
| [oauth_refresh_token](#oauth_refresh_token) |  |
| [tb_address](#tb_address) |  |
| [tb_areas](#tb_areas) | 行政区域县区信息表 |
| [tb_cities](#tb_cities) | 行政区域地州市信息表 |
| [tb_freight_template](#tb_freight_template) |  |
| [tb_provinces](#tb_provinces) | 省份信息表 |
| [tb_user](#tb_user) | 用户表 |
| [undo_log](#undo_log) |  |
**表名：** <a id="oauth_access_token">oauth_access_token</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | token_id |   varchar   | 256 |   0    |    Y     |  N   |       |   |
|  2   | token |   blob   | 65535 |   0    |    Y     |  N   |       |   |
|  3   | authentication_id |   varchar   | 48 |   0    |    N     |  Y   |       |   |
|  4   | user_name |   varchar   | 256 |   0    |    Y     |  N   |       |   |
|  5   | client_id |   varchar   | 256 |   0    |    Y     |  N   |       |   |
|  6   | authentication |   blob   | 65535 |   0    |    Y     |  N   |       |   |
|  7   | refresh_token |   varchar   | 256 |   0    |    Y     |  N   |       |   |
**表名：** <a id="oauth_approvals">oauth_approvals</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | userId |   varchar   | 256 |   0    |    Y     |  N   |       |   |
|  2   | clientId |   varchar   | 256 |   0    |    Y     |  N   |       |   |
|  3   | scope |   varchar   | 256 |   0    |    Y     |  N   |       |   |
|  4   | status |   varchar   | 10 |   0    |    Y     |  N   |       |   |
|  5   | expiresAt |   timestamp   | 19 |   0    |    N     |  N   |   CURRENT_TIMESTAMP    |   |
|  6   | lastModifiedAt |   timestamp   | 19 |   0    |    N     |  N   |   CURRENT_TIMESTAMP    |   |
**表名：** <a id="oauth_client_details">oauth_client_details</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | client_id |   varchar   | 48 |   0    |    N     |  Y   |       | 客户端ID，主要用于标识对应的应用  |
|  2   | resource_ids |   varchar   | 256 |   0    |    Y     |  N   |       |   |
|  3   | client_secret |   varchar   | 256 |   0    |    Y     |  N   |       | 客户端秘钥，BCryptPasswordEncoder加密  |
|  4   | scope |   varchar   | 256 |   0    |    Y     |  N   |       | 对应的范围  |
|  5   | authorized_grant_types |   varchar   | 256 |   0    |    Y     |  N   |       | 认证模式  |
|  6   | web_server_redirect_uri |   varchar   | 256 |   0    |    Y     |  N   |       | 认证后重定向地址  |
|  7   | authorities |   varchar   | 256 |   0    |    Y     |  N   |       |   |
|  8   | access_token_validity |   int   | 10 |   0    |    Y     |  N   |       | 令牌有效期  |
|  9   | refresh_token_validity |   int   | 10 |   0    |    Y     |  N   |       | 令牌刷新周期  |
|  10   | additional_information |   varchar   | 4096 |   0    |    Y     |  N   |       |   |
|  11   | autoapprove |   varchar   | 256 |   0    |    Y     |  N   |       |   |
**表名：** <a id="oauth_client_token">oauth_client_token</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | token_id |   varchar   | 256 |   0    |    Y     |  N   |       |   |
|  2   | token |   blob   | 65535 |   0    |    Y     |  N   |       |   |
|  3   | authentication_id |   varchar   | 48 |   0    |    N     |  Y   |       |   |
|  4   | user_name |   varchar   | 256 |   0    |    Y     |  N   |       |   |
|  5   | client_id |   varchar   | 256 |   0    |    Y     |  N   |       |   |
**表名：** <a id="oauth_code">oauth_code</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | code |   varchar   | 256 |   0    |    Y     |  N   |       |   |
|  2   | authentication |   blob   | 65535 |   0    |    Y     |  N   |       |   |
**表名：** <a id="oauth_refresh_token">oauth_refresh_token</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | token_id |   varchar   | 256 |   0    |    Y     |  N   |       |   |
|  2   | token |   blob   | 65535 |   0    |    Y     |  N   |       |   |
|  3   | authentication |   blob   | 65535 |   0    |    Y     |  N   |       |   |
**表名：** <a id="tb_address">tb_address</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       |   |
|  2   | username |   varchar   | 50 |   0    |    Y     |  N   |       | 用户名  |
|  3   | provinceid |   varchar   | 20 |   0    |    Y     |  N   |       | 省  |
|  4   | cityid |   varchar   | 20 |   0    |    Y     |  N   |       | 市  |
|  5   | areaid |   varchar   | 20 |   0    |    Y     |  N   |       | 县/区  |
|  6   | phone |   varchar   | 20 |   0    |    Y     |  N   |       | 电话  |
|  7   | address |   varchar   | 200 |   0    |    Y     |  N   |       | 详细地址  |
|  8   | contact |   varchar   | 50 |   0    |    Y     |  N   |       | 联系人  |
|  9   | is_default |   varchar   | 1 |   0    |    Y     |  N   |       | 是否是默认1默认0否  |
|  10   | alias |   varchar   | 50 |   0    |    Y     |  N   |       | 别名  |
**表名：** <a id="tb_areas">tb_areas</a>

**说明：** 行政区域县区信息表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | areaid |   varchar   | 20 |   0    |    N     |  Y   |       | 区域ID  |
|  2   | area |   varchar   | 50 |   0    |    N     |  N   |       | 区域名称  |
|  3   | cityid |   varchar   | 20 |   0    |    N     |  N   |       | 城市ID  |
**表名：** <a id="tb_cities">tb_cities</a>

**说明：** 行政区域地州市信息表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | cityid |   varchar   | 20 |   0    |    N     |  Y   |       | 城市ID  |
|  2   | city |   varchar   | 50 |   0    |    N     |  N   |       | 城市名称  |
|  3   | provinceid |   varchar   | 20 |   0    |    N     |  N   |       | 省份ID  |
**表名：** <a id="tb_freight_template">tb_freight_template</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       | ID  |
|  2   | name |   varchar   | 50 |   0    |    Y     |  N   |       | 模板名称  |
|  3   | type |   char   | 1 |   0    |    Y     |  N   |       | 计费方式  |
**表名：** <a id="tb_provinces">tb_provinces</a>

**说明：** 省份信息表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | provinceid |   varchar   | 20 |   0    |    N     |  Y   |       | 省份ID  |
|  2   | province |   varchar   | 50 |   0    |    N     |  N   |       | 省份名称  |
**表名：** <a id="tb_user">tb_user</a>

**说明：** 用户表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | username |   varchar   | 50 |   0    |    N     |  Y   |       | 用户名  |
|  2   | password |   varchar   | 60 |   0    |    N     |  N   |       | 密码，加密存储  |
|  3   | phone |   varchar   | 20 |   0    |    Y     |  N   |       | 注册手机号  |
|  4   | email |   varchar   | 50 |   0    |    Y     |  N   |       | 注册邮箱  |
|  5   | created |   datetime   | 19 |   0    |    N     |  N   |       | 创建时间  |
|  6   | updated |   datetime   | 19 |   0    |    N     |  N   |       | 修改时间  |
|  7   | source_type |   varchar   | 1 |   0    |    Y     |  N   |       | 会员来源：1:PC，2：H5，3：Android，4：IOS  |
|  8   | nick_name |   varchar   | 50 |   0    |    Y     |  N   |       | 昵称  |
|  9   | name |   varchar   | 50 |   0    |    Y     |  N   |       | 真实姓名  |
|  10   | status |   varchar   | 1 |   0    |    Y     |  N   |       | 使用状态（1正常0非正常）  |
|  11   | head_pic |   varchar   | 150 |   0    |    Y     |  N   |       | 头像地址  |
|  12   | qq |   varchar   | 20 |   0    |    Y     |  N   |       | QQ号码  |
|  13   | is_mobile_check |   varchar   | 1 |   0    |    Y     |  N   |   0    | 手机是否验证（0否1是）  |
|  14   | is_email_check |   varchar   | 1 |   0    |    Y     |  N   |   0    | 邮箱是否检测（0否1是）  |
|  15   | sex |   varchar   | 1 |   0    |    Y     |  N   |   1    | 性别，1男，0女  |
|  16   | user_level |   int   | 10 |   0    |    Y     |  N   |       | 会员等级  |
|  17   | points |   int   | 10 |   0    |    Y     |  N   |       | 积分  |
|  18   | experience_value |   int   | 10 |   0    |    Y     |  N   |       | 经验值  |
|  19   | birthday |   datetime   | 19 |   0    |    Y     |  N   |       | 出生年月日  |
|  20   | last_login_time |   datetime   | 19 |   0    |    Y     |  N   |       | 最后登录时间  |
**表名：** <a id="undo_log">undo_log</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :--: | :--- | :------: | :----: | :----: | :------: | :--: | :----: | :--: |
|  1   | id |   bigint   | 19 |   0    |    N     |  Y   |       |   |
|  2   | branch_id |   bigint   | 19 |   0    |    N     |  N   |       |   |
|  3   | xid |   varchar   | 100 |   0    |    N     |  N   |       |   |
|  4   | rollback_info |   longblob   | 2147483647 |   0    |    N     |  N   |       |   |
|  5   | log_status |   int   | 10 |   0    |    N     |  N   |       |   |
|  6   | log_created |   datetime   | 19 |   0    |    Y     |  N   |       |   |
|  7   | log_modified |   datetime   | 19 |   0    |    Y     |  N   |       |   |
|  8   | ext |   varchar   | 100 |   0    |    Y     |  N   |       |   |
