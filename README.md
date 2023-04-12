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
| user_id | string| 是       |      |      平台用户id  如open id|
|     user_type         |    int              | 是         |      | 用户类型 1.wx     |

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
