# 正则表达式
## 作用
用来匹配字符串的强有力工具

## 用途
1. 匹配字符串,判断是否合规
2. 对字符串进行分割,更加实用
3. 可以对字符串进行分组,便于提取
4. 可以进行预编译,解决性能问题

## 使用
利用字符描述字符规则

## 规则
### 特殊字符
`\` 
`-`
特殊字符需要使用`\`进行转义

### 规则定义

各个规则项可以进行组合

#### 字符类型
`\d`    : 匹配一个数字
`\w`    : 匹配一个字符或数字   
`\s`    : 匹配一个空格或TAB空白符
`.`     : 匹配任意字符
`[]`    : 表示范围，更精确

#### 字符数量
`*`     : 匹配任意数量字符(包括0个)
`+`     : 匹配至少一个字符
`?`     : 匹配0个或1个字符
`{n}`   : 匹配n个字符
`{n,m}` : 匹配n-m个字符

#### 其他
`A|B`   : 可以匹配A或B
`^`     : 表示行的开头
`$`     : 表示行的结束
`()`    : 定义分组

### 示例
1. `\d{3}\s+\d{3,8}`
分析：使用了\d {n} \s + {n,m}五种规则定义
`\d{3}` 表示需要3个数字
`\s+` 表示至少需要一个空格
`\d{3,8}` 表示需要最少3个、最多8个数字

2. `[0-9a-zA-Z\_]`
分析：使用了范围规则
表示允许0-9、a-z、A-Z、_ 等字符

3. `^py$`
分析：使用了其他规则
表示必须以`py`开头和结尾，因此只能匹配`py`














