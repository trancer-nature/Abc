### 查询内容

**Path：** `https://{host}/user/chat`

**接口描述：**

 **请求参数**

**Headers**

| 参数名称     | 参数值           | 是否必须 | 示例 | 备注 |
| ------------ | ---------------- | -------- | ---- | ---- |
| Content-Type | application/json | 是       |      |      |
|              |                  |          |      |      |

  **Body**

| 参数名称     | 参数值类型          | 是否必须 | 示例 | 备注 |
| ------------ | ---------------- | -------- | ---- | ---- |
| user_id | string| 是       |      |      平台用户id  如open id|
| user_type | int | 是 |      | 用户类型 1.wx     |
| prompt | string | 是 |      | 文本内容 (搜索详细,也可作为标题)     |
| chat_type | int | 是 |      | 请求类型 1.创作文章标题 2.专业写作 3.普通写作 4.游戏攻略 5.报告 6.检讨 7.美好祝福 8.翻译 9.问答     |
| job | string | 否 |      | 岗位   |

 **返回参数**
  | 参数名称     | 参数值类型          | 是否必须 | 示例 | 备注 |
| ------------ | ---------------- | -------- | ---- | ---- |
| code | int| 是       |      |      返回状态码  |
|     data         |    string              | 是         |      | 返回数据  |
|     message         |    string              | 是         |      | 请求消息    |
|     request_id         |    string              | 是         |      | 请求唯一id   |


### 用户查询

**Path：** `https://{host}/user/info`

**接口描述：**

 **请求参数**

**Headers**

| 参数名称     | 参数值           | 是否必须 | 示例 | 备注 |
| ------------ | ---------------- | -------- | ---- | ---- |
| Content-Type | application/json | 是       |      |      |
|              |                  |          |      |      |

  **Body**

| 参数名称     | 参数值类型          | 是否必须 | 示例 | 备注 |
| ------------ | ---------------- | -------- | ---- | ---- |
| user_id | string| 是 |      |      平台用户id  如open id|
| user_type | int | 是 |      | 用户类型 1.wx     |


  **返回参数**
  | 参数名称     | 参数值类型          | 是否必须 | 示例 | 备注 |
| ------------ | ---------------- | -------- | ---- | ---- |
| code | int| 是       |      |      返回状态码  |
|     data         |    object               | 是         |      | 返回数据  |
|     data.id         |    int               | 是         |      | 内部id  |      
|     data.nick_name         |    string               | 是         |      | 用户类型  |     
|     data.user_type         |    int               | 是         |      | 内部id  |     
|     data.phone         |    string               | 否         |      | 联系方式  |     
|     data.from         |    string               | 否        |      | 来源  |     
|     data.tag         |    string | 是         |    否  | 标记  |     
|     data.openid         |    string | 是         |    否  | 微信openid  |     
|     data.remaining_count         |    int | 是         |      | 次数  |     
|     data.platform_id         |    string | 是         |      | 平台id  |    
|     message         |    string              | 是         |      | 请求消息    |
|     request_id         |    string              | 是         |      | 请求唯一id   |

### 用户分享后调用增加次数

**Path：** `https://{host}/user/share`

**Method：** POST

**接口描述：**

 **请求参数**

**Headers**

| 参数名称     | 参数值           | 是否必须 | 示例 | 备注 |
| ------------ | ---------------- | -------- | ---- | ---- |
| Content-Type | application/json | 是       |      |      |
|              |                  |          |      |      |


 **Body**

| 参数名称     | 参数值类型          | 是否必须 | 示例 | 备注 |
| ------------ | ---------------- | -------- | ---- | ---- |
| user_id | string| 是       |      |      平台用户id  如open id|
|     user_type         |    int              | 是         |      | 用户类型 1.wx     |
|     share_type         |    int              | 是         |      | 1.免费 2.广告    |

  **返回参数**
  | 参数名称     | 参数值类型          | 是否必须 | 示例 | 备注 |
| ------------ | ---------------- | -------- | ---- | ---- |
| code | int| 是       |      |      返回状态码  |
|     data         |    string              | 是         |      | 返回数据  |
|     message         |    string              | 是         |      | 请求消息    |
|     request_id         |    string              | 是         |      | 请求唯一id   |
