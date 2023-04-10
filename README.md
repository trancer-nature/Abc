### 加载基本信息

**Path：** `https://{host}/user/share`

**Method：** POST

​	**接口描述：**

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
