# Time类
## init(int total)
### 初始化时间并开始对A计时
#### 参数
\<int\> total 每个人允许的总时间

#### 返回值
\<object\> Time


## toggle(string player)
### 转换计时器到player这个玩家，我们规定player必须传入“A”,"B"，“C”，A为先手

#### 参数
\<string\> player 字符串，A或者B
如果字典中没有D这个玩家，那么就让D加入到字典中

#### 返回值
\<dict\> {"A":3600, "B":3400, "C":3000}
返回的时间以s为单位，返回的是剩余时间

## timeout(string player)
### 获取玩家当前剩余时间

#### 参数
\<string\> player 必须传入当前字典中存在的A，B，C

#### 返回值
\<dict\> {"A":3600, "B":3400, "C":3000}
返回的时间以s为单位，剩余时间