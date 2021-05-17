# MQTT服务

## 服务端

### Broker

- 云服务器 mosquito

## 客户端

### 设备端

```
clientID：设备编号
serverAddress：yplearning.cn
port：1883
```

- 订阅主题
  - Topic：全局主题，首先订阅
  - Command：由后端发布消息，设备端作相应调整

- 发布消息

| 主题   | 说明                     | 格式 | 示例                                                         |
| ------ | ------------------------ | ---- | ------------------------------------------------------------ |
| Status | 叉车实时状态，1s发布一次 | JSON | {"time":"2021/5/17 13:55:01","clientID":"C01","status":"0","load":"50.1","position":{"X":"29.9","Y":"26.9"}} |

### 后端

```
clientID：Admin
serverAddress：yplearning.cn
port：1883
```

- 订阅主题
  - Topic：全局主题，首先订阅
  - Status：由设备发布消息，读取消息并解析至数据库
- 发布消息
  - 暂无

### 前端

























