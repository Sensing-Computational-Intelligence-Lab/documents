# Room类

## 私有变量
### \<time\> __timer 计时器
### \<board\> __board 棋盘

## 公有变量
### \<player\> players[] 玩家列表

## 成员方法
### init(class boardtype, int totaltime)
初始化房间

#### 参数
\<class\> boardtype 传入的是 board的种类
\<int\> totaltime 传入的是 每人可使用的最大时间

#### 返回值
\<object\> room

### addplayer(object player)
添加玩家

#### 参数
\<object\> player 传入的是玩家的这个对象

#### 返回值
\<string\> 给这个玩家分配的ID，例如‘A’，‘B’，‘C’

### removeplayer(object player)
删除玩家

#### 参数
\<object\> player 传入的是玩家的这个对象

#### 返回值
\<int\> 状态： 0 失败，1 成功

### start(void)
开始游戏，并且开始计时
#### 参数
无
#### 返回值
\<dict\> {“A”:3600, "B":3400, "C":3000}
返回的是当前剩余时间

### status(void)
获取当前比赛的状态
#### 参数
无
#### 返回值
\<dict\> {"status":0,"messages":{}}
##### status列表
###### 0 未开局
###### 1 已开局
###### 2 比赛暂停
###### 3 已结束
###### 4 比赛重置

##### messages可包含参数
具体制定

### move(player, location , *kw)
#### 参数
- [String] player
- [Dict] location

#### 参数说明
- player 必须要传入一个字符 'A' 或 'B' ，我们规定 A 为先手方
- location 是一个字典类型格式为['from' : int, 'to' : int]

#### 返回值
success:
返回一个tuple，即为(棋局, 输赢) 棋局为一维数组
fail:
抛出异常
具体制定

#### 例子
返回值 ([1, 1, 0, 0, 1, 0], 'A')
