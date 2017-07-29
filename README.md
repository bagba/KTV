# KTV管理系统

主要功能模块

 * 员工管理
 * 会员管理
 * 账务管理
 * 库存管理
 * 包房管理
 * 订单管理

# 数据库设计

## 员工管理

### 员工基本信息

      | 员工ID | 姓名|入职时间 | 薪资 |职位|
      | ------|------ | ------ | ------|------|
      |000001 | 彭焘|20170101 | 100000.0 |董事长|
      | 000002 |李政道| 20170102 | 10.0 |清洁工|

### 员工考勤

      | 员工ID | 上班时间 | 下班时间|客户评分|
      | ------| ------ | ------|------|
      |000001 | 20170101:08:30 | 20170101:18:30 |5|
      | 000002 | 20170102:08:30 | 20170101:18:30|4|


## 客户管理


### 会员基本信息

      | 会员ID | 姓名 |电话|会员等级|会员办理时间|余额|
      | ------|  ------ | ------ | ------|------|------|
      |000001 | 毛线 | 1888888888 |99|20170729|10000000.0|
      | 000002 | 皮鞋 | 13888888888 |88|20170729|9999999.0|


### 会员流水信息

      | 会员ID | 流水订单号 |流水类型|金额|
      | ------|  ------ |------|-------|
      |000001 | 12 |消费|10000|
      | 000002 | 13 |充值|100000|
      | 000001 | 15 |退款|9999|

## 包房管理


### 包房基本信息

      | 房间ID | 房名 |房间价格|房间数|
      | ------|  ------ | ------ | ------|
      |000001 | 公主房 | 998 |2|
      | 000002 | 吃妞房 | 99998 |1|

### 包房状态管理

      | 房间ID | 房间状态 |开始时间|结束时间|订单ID|
      | ------|  ------ | ------ | ------| ------|
      |000001 | 使用中 | 20170728：20：00 |20170728：23：00 |12|
      | 000002 | 空闲| 20170728：20：00  |20170728：23：00 |13|

## 流水管理


### 开房管理

      | 订单ID | 下单时间 |下单方式|房间ID|退房时间|付款金额|会员ID|
      | ------|  ------ | ------ | ------| ------|------|-----|
      |000001 | 20170728：20：00 | 电话预定 |2|20170728：24：00|1000|1|
      | 000002 | 20170728：20：00 | 现场下单|1|20170728：24：00|239|2|


### 其他服务管理
      | 流水ID | 订单ID |类型|金额|下单时间|
      | ------|  ------ | ------ | ------| ----|
      |012| 000001 | 酒水|1000|20170728：24：00|
      | 013|000001|妞 | 9999|20170728：24：00|

### 流水管理

      | 流水ID | 下单时间 |金额|类型|会员ID|
      | ------|  ------ | ------ | ------| ------|
      |000001 | 20170728：20：00 |2000|充值|01||
      | 000002 | 20170728：20：00 | 3000|消费|01|
