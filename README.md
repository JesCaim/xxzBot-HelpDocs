

# 小小奏帮助文档



> *pjsk查询服务：[分布式unibot帮助文档](https://bot.unijzlsx.com/)

> 部分插件源自网络，侵删

> 全局命令前缀：'/'   '小小奏'   ‘@小小奏’

> 邀请进群联系Mas：1920578206



## 文档格式

**服务基础信息**

- 名称: `(服务名称)`

- 说明: `(服务说明)`

- 权限: `e.g. 超级用户、群管理`

---

**(命令)**

- 说明: `(命令说明)`

- 权限: `(命令所需权限)`
- 需要at: `e.g. 否`       //**需要at表示该命令需要命令前缀('/' or '小小奏' or ‘@小小奏’)**
- 更多别名: `e.g. 无`

---



## 模块概览

- Bot基础模块
  - [bot管理](#bot管理)
  - [广播](#广播)
  - [反馈  (**必看**)](#反馈)
- 其他模块
  - [自定义问答  (**new**)](#自定义问答)
  - [kimo](#kimo)
  - [涩图](#涩图)
  - [B站动态推送](#B站动态推送)
  - [随个人](#随个人)
  - [今日人品](#今日人品)
  - [漂流瓶](#漂流瓶)
  - [头像表情包](#头像表情包)
  - [随机龙图](#随机龙图)
  - [今天吃什么 ](#今天吃什么)
  - [VITS语音合成 ](#VITS语音合成)
  - [早晚安   (**new**)](#早晚安)

---



## bot管理

- 名称: `管理`
- 说明: `控制bot的各项服务`
- 权限: `Master、群管理`

---

### 禁用

- 说明: `针对触发人所在群禁用某服务（模块）`
- 权限: `Master、群管理`
- 需要at: `否`
- 更多别名: `无`

![image-20221121221530527](https://jescaim-personal-images.oss-cn-hangzhou.aliyuncs.com/image-20221121221530527.png)

### 启用

- 说明: `针对触发人所在群启用某服务（模块）`
- 权限: `Master、群管理`
- 需要at: `否`
- 更多别名: `无`

### 追踪

- 说明: `获取报错信息`
- 权限: `所有人`
- 需要at: `否`
- 更多别名: `/track`

---



## 广播

- 名称: `广播`
- 说明: `通过bot向其所在群推送消息`
- 权限: `Master、群管理`

---

### 广播

- 说明: `向bot所在群推送消息，有1～3s随机延迟`
- 权限: `Master`
- 需要at: `是`
- 更多别名: `bc`

### 拒绝广播

- 说明: `拒绝广播推送，仅对当前群生效`
- 权限: `Master、群管理`
- 需要at: `是`
- 更多别名: `无`


### 接受广播

- 说明: `接受广播推送，仅对当前群生效`
- 权限: `Master、群管理`
- 需要at: `是`
- 更多别名: `无`

---



## 反馈

- 名称: `反馈`
- 说明: `向Master发送错误反馈/意见`
- 权限: `所有人`

---

### 反馈

- 说明: `向Master发送错误反馈/意见`
- 权限: `所有人`
- 需要at: `否`
- 更多别名: `无`

![image-20221121221553709](https://jescaim-personal-images.oss-cn-hangzhou.aliyuncs.com/image-20221121221553709.png)

---



## 自定义问答

- 名称: `自定义问答`
- 说明: `支持模糊匹配、全匹配、正则匹配的自定义词库`
- 权限: `所有人`

---

### 问答教学

- 设置词条命令由`问句`和`答句`组成。设置之后, 收到`消息`时触发。所有人都可以设置本群词条，管理员可以删除。

- 格式`[模糊|正则|@]问...答...`

  - `模糊|正则` 匹配模式中可任性一个或`不选`, `不选` 表示 `全匹配`
  - `@` 可与以上匹配模式组合使用，表示被艾特，回复，私聊时才会触发。

- 支持图片回复

- 可以使用换行或空格隔开问，答

  - 例如

    ```
    使用换行的情况下：
    问
    123
    答
    456
    
    使用空格的情况下：
    问 123 答 456
    ```

![image-20221224151636273](https://jescaim-personal-images.oss-cn-hangzhou.aliyuncs.com/image-20221224151636273.png)

![image-20221224152149025](https://jescaim-personal-images.oss-cn-hangzhou.aliyuncs.com/image-20221224152149025.png)

- 问答句中的首尾空白字符会被自动忽略



#### 问句选项

- `问...答...` 全匹配模式, 必须全等才能触发答

- `模糊问...答...` 当`问句`出现在`消息`里时则会触发

- `正则问...答...`, 当`问句`被`消息`正则捕获时则会匹配（正则表达式为纯文本，不会正则的话**不建议使用**）

- 例如: 正则问[他你]不理答你被屏蔽了

  | 消息     | 回复       |
  | -------- | ---------- |
  | 他不理   | 你被屏蔽了 |
  | 他不理我 | 你被屏蔽了 |
  | 你不理我 | 你被屏蔽了 |

- `@问...答...`, 只有 `event.tome` 时才会触发，如**被@、被回复时或在私聊中**，可以和以上几种组合使用

  - 例如: `模糊@问 晚安 答 不准睡`

- 问句可包含`at` 即在 QQ 聊天中手动 at 群友

  - 建议只在`问...答...`中使用
  - 例如: `问 @这是群名称 答 老婆!`

#### 答句选项

- `/at` + `qq号`, 当答句中包含`/at` + `qq号`时将会被替换为@某人

  - 例如: `问 群主在吗 答 /at 123456789在吗`

- `/self`, 当答句中包含`/self`时将会被替换为发送者的群昵称
  - 例如: `问 我是谁 答 你是/self` (群昵称为: 我老婆)

- `/atself`, 当答句中包含`/atself`时将会被替换为@发送者
  - 例如: `问 谁是牛头人 答 @这是群昵称`

![image-20221224152854730](https://jescaim-personal-images.oss-cn-hangzhou.aliyuncs.com/image-20221224152854730.png)

### 删除词条

- 仅限群管理，群主，Master使用
- `删除[模糊|正则|@]词条` + 需要删除的`问句`
  - 例如: `删除全局模糊@词条 你好`
- 删除词库: 删除当前群聊/私聊词库(本群所有自定义问答)

  - 例如: `/删除词库`

### 查询词条

- 查询本群指定词库

  - `查询[模糊|正则]词库`
  - 例如 `查询词库`

---



## kimo

- 名称: `kimo`
- 说明: `涩涩的词库`
- 权限: `所有人`

![image-20221121222506884](https://jescaim-personal-images.oss-cn-hangzhou.aliyuncs.com/image-20221121222506884.png)



---



## 涩图

- 名称: `涩图`
- 说明: `hso!（已屏蔽R18标签）`
- 权限: `所有人`

---

### 来点涩图

- 说明: `来张随机涩图，冷却2分钟`
- 权限: `所有人`
- 需要at: `否`
- 更多别名: `涩图来、来点涩图、来份涩图`

![image-20221121230439261](https://jescaim-personal-images.oss-cn-hangzhou.aliyuncs.com/image-20221121230439261.png)

### 来\[张点丶份](.*?)的[涩色]图

- 说明: `根据提供的tag查找涩图，冷却2分钟`
- 权限: `所有人`
- 需要at: `否`
- 更多别名: `无`

![image-20221121222931243](https://jescaim-personal-images.oss-cn-hangzhou.aliyuncs.com/image-20221121222931243.png)

### 涩值检测

- 说明: `自动检测图片消息的涩值，鉴定为涩图则提示。`~~并转发给Mas~~
- 权限: `所有人`
- 需要at: `被动触发`
- 更多别名: `无`

![image-20221121222749529](https://jescaim-personal-images.oss-cn-hangzhou.aliyuncs.com/image-20221121222749529.png)

---



## B站动态推送



- 名称: `b站动态订阅`
- 说明: `b站动态订阅助手～`
- 权限: `所有人`

**推荐订阅Project_SEKAI资讯站：/bd.add 13148307**

![image-20221121223402208](https://jescaim-personal-images.oss-cn-hangzhou.aliyuncs.com/image-20221121223402208.png)

---

### /bd.add

- 说明: `添加b站up主订阅`
- 权限: `Master、群管理`
- 需要at: `否`
- 更多别名: `无`

### /bd.del

- 说明: `删除b站up主订阅`
- 权限: `Master、群管理`
- 需要at: `否`
- 更多别名: `无`

### /bd.list

- 说明: `获取b站up主订阅列表`
- 权限: `所有人`
- 需要at: `否`
- 更多别名: `无`

---



## 随个人



- 名称: `随个人`
- 说明: `随机艾特一位群友满足你的要求！`
- 权限: `所有人`

---

### 随个人(XXX)

- 说明: `随机艾特一位群友满足你的要求！`
- 权限: `所有人`
- 需要at: `否`
- 更多别名: `无`

![image-20221121223451198](https://jescaim-personal-images.oss-cn-hangzhou.aliyuncs.com/image-20221121223451198.png)

---



## 今日人品

- 名称: `今日人品`
- 说明: `查看你的今日人品！`
- 权限: `所有人`

---

### jrrp

- 说明: `查看你的当天的人品值~(0-100)`
- 权限: `所有人`
- 需要at: `否`
- 更多别名: `/jrrp`

![image-20221121223517483](https://jescaim-personal-images.oss-cn-hangzhou.aliyuncs.com/image-20221121223517483.png)

---



## 漂流瓶

- 名称: `漂流瓶`
- 说明: `群与群互通的漂流瓶！`
- 权限: `所有人`

---

### 扔漂流瓶 [文本/图片]

- 说明: `扔出一个漂流瓶~`
- 权限: `所有人`
- 需要at: `否`
- 更多别名: `无`

![image-20221121223717918](https://jescaim-personal-images.oss-cn-hangzhou.aliyuncs.com/image-20221121223717918.png)

### 捡漂流瓶

- 说明: `若捡到的漂流瓶存在回复，则只会显示最近三条，使用'查看漂流瓶'查看所有回复`
- 权限: `所有人`
- 需要at: `否`
- 更多别名: `无`

![image-20221121223835536](https://jescaim-personal-images.oss-cn-hangzhou.aliyuncs.com/image-20221121223835536.png)

### 查看漂流瓶 [漂流瓶序号]

- 说明: `查看指定序号漂流瓶内容（为了确保随机性，无法查看无评论漂流瓶）`
- 权限: `所有人`
- 需要at: `否`
- 更多别名: `无`

![image-20221121223917487](https://jescaim-personal-images.oss-cn-hangzhou.aliyuncs.com/image-20221121223917487.png)

### 评论漂流瓶 [漂流瓶序号] [文本]

- 说明: `评论指定序号漂流瓶`
- 权限: `所有人`
- 需要at: `否`
- 更多别名: `无`

![image-20221121224011737](https://jescaim-personal-images.oss-cn-hangzhou.aliyuncs.com/image-20221121224011737.png)

![image-20221121224035775](https://jescaim-personal-images.oss-cn-hangzhou.aliyuncs.com/image-20221121224035775.png)

### 举报漂流瓶 [漂流瓶序号]

- 说明: `举报指定序号漂流瓶，五次后将自动删除`
- 权限: `所有人`
- 需要at: `否`
- 更多别名: `无`

---



## 头像表情包

- 名称: `头像表情包`
- 说明: `便捷合成与头像有关的表情包()`
- 权限: `所有人`

### 头像表情包

- 说明: `发送'头像表情包'获得如下图帮助图片`
- 权限: `所有人`
- 需要at: `否`
- 更多别名: `无`

![img](https://jescaim-personal-images.oss-cn-hangzhou.aliyuncs.com/V_U1W%5BN(%5DF8ZWZC5)B46%60%5BF.PNG)

![image-20221121224134998](https://jescaim-personal-images.oss-cn-hangzhou.aliyuncs.com/image-20221121224134998.png)

---



## 随机龙图

- 名称: `随机龙图`
- 说明: `顾名思义(图库越1500张)`
- 权限: `所有人`

### 随机龙图

- 说明: `抽取一张龙图`
- 权限: `所有人`
- 需要at: `否`
- 更多别名: `无`

![image-20221213005336149](https://jescaim-personal-images.oss-cn-hangzhou.aliyuncs.com/image-20221213005336149.png)

### 添加随机龙图 [图片]

- 说明: `添加一张龙图到库中(支持回复图片)`
- 权限: `管理员，Master`
- 需要at: `否`
- 更多别名: `无`

![image-20221213005549733](https://jescaim-personal-images.oss-cn-hangzhou.aliyuncs.com/image-20221213005549733.png)

![image-20221213005737108](https://jescaim-personal-images.oss-cn-hangzhou.aliyuncs.com/image-20221213005737108.png)





------

## 今天吃什么

- 名称: `今天吃什么`
- 说明: `选择恐惧症？让小小奏建议你今天吃/喝什么！`
- 权限: `所有人`

### (今天|\[早中午晚][上饭餐午]|早上|夜宵|今晚)(吃|喝)(什么|啥|点啥)(帮助)

- 说明: `让小小奏建议你今天吃/喝什么！`
- 权限: `所有人`
- 需要at: `否`
- 更多别名: `无`

![image-20221219142721790](https://jescaim-personal-images.oss-cn-hangzhou.aliyuncs.com/image-20221219142721790.png)

### (开启|关闭)小助手

- 说明: `吃饭小助手：每天7、12、15、18、22点群发问候语提醒群友吃饭/摸鱼/下班(bot重启后会自动关闭所有群小助手)`
- 权限: `管理员`
- 需要at: `否`
- 更多别名: `无`

![image-20221219142950175](https://jescaim-personal-images.oss-cn-hangzhou.aliyuncs.com/image-20221219142950175.png)

### 添加 [菜品]

- 说明: `群管理可自行添加或移除群特色菜单`
- 权限: `管理员`
- 需要at: `否`
- 更多别名: `无`



![image-20221219143350820](https://jescaim-personal-images.oss-cn-hangzhou.aliyuncs.com/image-20221219143350820.png)

---



## VITS语音合成

- 名称: `VITS语音合成`
- 说明: `基于VITS模型合成角色语音`
- 权限: `所有人`

> 在[Gal-Voice-Bot](https://github.com/TheKOG/Gal-Voice-Bot)的代码基础上复写了PJSK模型的部分。（PJSK模型由@nya提供，[项目地址](https://github.com/Kanade-nya/PJSK-MultiGUI)）

> 目前支持的chara有：
>
> PJSK：
>
> knd|mfy0(营业版)|mfy1(黑化版)|ena|mzk|
>
> emu|nene|rui|tks|
>
> akt|an|khn|toya|
>
> airi|hrk|mnr|szk|
>
> saki|ick|hnm|shiho
>
> ATRI My Dear Moments：亚托莉
>
> 柚子社：宁宁|爱瑠|芳乃|茉子|丛雨|小春|七海
>
> 原神：派蒙|凯亚|安柏|丽莎|琴|香菱|枫原万叶|迪卢克|温迪|可莉|早柚|托马|芭芭拉|优菈|云堇|钟离|魈|凝光|雷电将军|北斗|甘雨|七七|刻晴|神里绫华|戴因斯雷布|雷泽|神里绫人|罗莎莉亚|阿贝多|八重神子|宵宫|荒泷一斗|九条裟罗|夜兰|珊瑚宫心海|五郎|散兵|女士|达达利亚|莫娜|班尼特|申鹤|行秋|烟绯|久岐忍|辛焱|砂糖|胡桃|重云|菲谢尔|诺艾尔|迪奥娜|鹿野院平藏

### \[chara名](片假)\[说|文件][文本]

- 说明: `合成角色语音/发送wav文件`
- 权限: `所有人`
- 需要at: `否`
- 更多别名: `无`

> 使用日语模型"说"+[中文]支持自动翻译为日语(翻译源为有道)

> "片假说"+[中文]即中文转片假名谐音。原神(中文)模型不支持"片假说"。

> 语音合成失败的原因可能是文本中出现了不合法的标点符号

> 请勿频繁使用该功能或文本使用超长句子，服务器cpu占用率长时间100%可能炸服

![image-20221219151146924](https://jescaim-personal-images.oss-cn-hangzhou.aliyuncs.com/image-20221219151146924.png)

---



## 早晚安

- 名称: `早晚安`
- 说明: `和小小奏说早晚安，记录睡眠时间，培养良好作息`
- 权限: `所有人`

### 早/晚安

- 说明: `记录睡眠时间，培养良好作息`
- 权限: `所有人`
- 需要at: `否`
- 更多别名: `小小奏早/晚安`

![image-20221224015458162](https://jescaim-personal-images.oss-cn-hangzhou.aliyuncs.com/image-20221224015458162.png)

### 我的作息

- 说明: `每周一显示上周睡眠信息统计，其他时间显示本周信息`
- 权限: `所有人`
- 需要at: `否`
- 更多别名: `无`

![image-20221224015642666](https://jescaim-personal-images.oss-cn-hangzhou.aliyuncs.com/image-20221224015642666.png)

### 群友作息

- 说明: `看看今天几个群友睡觉或起床了，每周一显示上周睡觉王`
- 权限: `所有人`
- 需要at: `否`
- 更多别名: `无`

![image-20221224015804046](https://jescaim-personal-images.oss-cn-hangzhou.aliyuncs.com/image-20221224015804046.png)

### 早晚安设置

- 说明: `查看本群早晚安配置`
- 权限: `所有人`
- 需要at: `否`
- 更多别名: `无`

### 早安/晚安设置

- 说明: `设置功能的参数`
- 权限: `管理员、Master`
- 需要at: `否`
- 更多别名: `无`



------

**特别感谢**

- ATRI@Kyomotoi提供的基础框架
- @TheKOG提供的[VITS合成框架](https://github.com/TheKOG/Gal-Voice-Bot)
- @nya提供的PJSK_VITS模型

