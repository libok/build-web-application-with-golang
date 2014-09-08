Title:  夏目接口文档 V1.0 
Author:  Shannon  Zhou
Date:   2014-08-27

# 夏目接口文档

## 配置文件

|  级别 |  名称 |  类型  |  描述  | 
| :------------ | :-----------: | -------------------: | ---- |
|  级别 |  名称 |  类型  |  描述  | 
| M | questId | int | 主线任务ID |
| M | clothes | string | 服装ID, 多件衣服由半角逗号分隔. 如: 10842,11388 |
[Request参数]


| First Header  | Second Header | Third Header         |
| :------------ | :-----------: | -------------------: |
| First row     | Data          | Very long data entry |
| Second row    | **Cell**      | *Cell*               |
| Third row     | Cell that spans across two columns  ||
[Table caption, works as a reference][section-mmd-tables-table1] 

—
The original image is 128x128 and contains no shadow.
![Original icon][img-icon_original]

##换装系统
### 1. dress/grade 	(换装评分)

	换装完成后计算评分和排名, 以及给予对应的奖励
		
| 级别 | 名称 | 类型 | 描述 | 
| :-: | -- | -- | -- |
| M | questId | int | 主线任务ID |
| M | clothes | string | 服装ID, 多件衣服由半角逗号分隔. 如: 10842,11388 |
[Request参数]

| 级别 | 名称 | 类型 | 描述 | 
| :-: | -- | -- | -- |
| M | grade | string | 评级: S, A, B, C, D, F |
| M | score | int | 得分 |
| M | friendRank | int | 在好友中的排名 |
| M | rank | int | 全服排名 |
| M | rewards | list | 奖励列表 |
|||| **type:** int, 奖励类型. (0: 金币, 1: 钻石, 2: 体力, 3: 服装, 4: 道具, 5: 设计图, 6: 抽卡商品)  |
|||| **content:** string, 奖励内容,如设计图ID. 金币/钻石没有留空即可 |
|||| **count:** int, 数量. |
[ Response参数]

->示例:<-
``` javascript
	{
	    "data": {
	    	"grade": "评级 [string]: S, A, B, C, D, F", //评级
	    	"score": 8583,  //分数
	        "friendRank": 7, //好友排名
	        "rank": 759361, //排名	        
	        "rewards": [{
	            "type": 0, //金币
	            "content": "", //171的金币
	            "count": 171
	        }, {
	            "type": 5, //设计图
	            "content": 4, //休闲短裙
	            "count": 1
	        }]
	    },
	    "errcode": 0,
	    "errmsg": ""
	}
```
[Byword Markdown Syntax](http://bywordapp.com/markdown/syntax.html)

[]()



Roses are red,
Violets are blue.

* libok is a good man
* libok is a good man to 
	* libok is good 
	* 
> Email-style angle brackets
> are used for blockquotes.

> > And, they can be nested.

> #### Headers in blockquotes
> 
> * You can quote a list.
> * Etc.
		

是大幅度发
