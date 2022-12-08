

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
  - [自定义词库](#自定义词库)
  - [kimo](#kimo)
  - [涩图](#涩图)
  - [B站动态推送](#B站动态推送)
  - [随个人](#随个人)
  - [今日人品](#今日人品)
  - [漂流瓶](#漂流瓶)
  - [头像表情包](#头像表情包)
  - [ChatGPT](#ChatGPT)

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



## 自定义词库

- 名称: `词库管理`
- 说明: `支持模糊匹配、全匹配、正则的自定义回复～支持分群、全局管理，支持群内投票添加 (满4人同意自动通过)`
- 权限: `所有人`

---

### /ts.add

- 说明: `添加本群词条，需审核或投票`
- 权限: `所有人`
- 需要at: `否`
- 更多别名: `无`

![image-20221121221809695](https://jescaim-personal-images.oss-cn-hangzhou.aliyuncs.com/image-20221121221809695.png)

### /ts.add.g

- 说明: `添加本群词条，仅限管理，无需审核`
- 权限: `Master、群管理`
- 需要at: `否`
- 更多别名: `无`

![image-20221121222030590](https://jescaim-personal-images.oss-cn-hangzhou.aliyuncs.com/image-20221121222030590.png)

### /ts.v

- 说明: `对本群内审核中的词条进行投票`
- 权限: `所有人`
- 需要at: `否`
- 更多别名: `无`

![image-20221121221841933](https://jescaim-personal-images.oss-cn-hangzhou.aliyuncs.com/image-20221121221841933.png)

### /ts.del

- 说明: `删除本群词条`
- 权限: `Master、群管理`
- 需要at: `否`
- 更多别名: `无`

![image-20221121222159284](https://jescaim-personal-images.oss-cn-hangzhou.aliyuncs.com/image-20221121222159284.png)

### /ts.del.v

- 说明: `删除本群处于投票中的词条`
- 权限: `Master、群管理`
- 需要at: `否`
- 更多别名: `无`



### /ts.list

- 说明: `查看本群词条`
- 权限: `所有人`
- 需要at: `否`
- 更多别名: `无`

### /ts.list.g

- 说明: `查看全局词条`
- 权限: `所有人`
- 需要at: `否`
- 更多别名: `无`

### /ts.list.v

- 说明: `查看本群待投票词条`
- 权限: `所有人`
- 需要at: `否`
- 更多别名: `无`

### /ts.audit

- 说明: `审核本群处于投票中的词条`
- 权限: `Master、群管理`
- 需要at: `否`
- 更多别名: `无`

### /ts.i

- 说明: `查看本群的词条详情`
- 权限: `所有人`
- 需要at: `否`
- 更多别名: `无`

### /ts.i.g

- 说明: `查看全局的词条详情`
- 权限: `所有人`
- 需要at: `否`
- 更多别名: `无`

### /ts.i.v

- 说明: `查看本群的待审核/投票的词条详情`
- 权限: `所有人`
- 需要at: `否`
- 更多别名: `无`

---



## kimo

- 名称: `kimo`
- 说明: `好像有点涩？`
- 权限: `所有人`

![image-20221121222506884](https://jescaim-personal-images.oss-cn-hangzhou.aliyuncs.com/image-20221121222506884.png)

---

### 叫我

- 说明: `更改kimo时的称呼`
- 权限: `所有人`
- 需要at: `否`
- 更多别名: `无`

![image-20221121222435305](https://jescaim-personal-images.oss-cn-hangzhou.aliyuncs.com/image-20221121222435305.png)

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

## ChatGPT

- 名称: `ChatGPT`
- 说明: `OpenAI的智能对话聊天解答插件,主要针对提问提供专业帮助`
- 权限: `所有人`

### /chat

- 说明: `提问/聊天`
- 权限: `所有人`
- 需要at: `否`
- 更多别名: `无`

![image-20221208232812552](https://jescaim-personal-images.oss-cn-hangzhou.aliyuncs.com/image-20221208232812552.png)

------



**特别感谢**

- ATRI@Kyomotoi提供的基础框架

