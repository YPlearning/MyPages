# Picture Upload

- Process

```mermaid
graph LR
获取照片名称 --> 保存照片到指定位置
保存照片到指定位置 --> 打开post网络接口上传照片
打开post网络接口上传照片 --> 照片消息写入服务器
```

## Serve

### Get the car information

- Car number
- Picture timestamp
- File and Data

### Local file path

- the file path can be access from web, and record the path as: http://(address)/pic/(car number)/(file name)
- Example: http://yp.yplearning.cn/pic/C01/C01_1621264092.Jpeg

### 数据库写入

- 数据库写入
- SQL语句：INSERT INTO `car_pic_C01` (`time`, `physicalpath`, `webpath`) VALUES ('时间', '文件地址', '文件网页访问地址');

## 客户端



### 照片命名规则

- 叉车编号 + _ + 日期时间（精确到秒）+ .Jpeg

  - 示例：C01_1621262524.Jpeg

    