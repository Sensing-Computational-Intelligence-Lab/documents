# RoomManager

## 私有变量
### \<Room\> __rooms[] 房间列表
### \<int\> __roomsNum 房间数量
### \<int\> __playerNum 玩家数量

## 成员方法
### init()
初始化RoomManager

### AddRoom(Room room)
添加一个房间
#### 参数
\<Room\> room , 传入的是Room类型的变量，直接传入其中一个room的实例。

#### 返回值
\<dict\> 返回一个字典类型。具体格式如下：  
{'roomID':1, 'roomObject': room}  
{'roomID': Int, 'roomObject': object}

### RemoveRoom(Int id)
移除一个房间
#### 参数
\<Int\> id, 传入的是一个整型变量，如果不传入id，则删除最后一个房间。
#### 返回值
\<dict\> 返回一个字典类型的，具体格式如下：  
{'status': true, 'roomNum': 10}   
{'status': boolean, 'roomNum': int}

### ResetRoom()
清空房间

#### 返回值
\<boolean\> true

### GetRoomInfo()
获取所有房间的基础信息

#### 返回值
\<dict\> 字典类型  
{'roomNum': 10, 'playerNun': 11, 'roomList': \[room1,room2,room3\]}  
{'roomNum': int, 'playerNun': int, 'roomList': \[obj,obj,obj\]} 

 