# 2019-Future-Food-Challenge
天池数据竞赛

# Qualification Round - Task
- Training set: 与食品安全事件相关的新闻事例，例如产品召回、欺诈活动或食源性疾病爆发。
 				与同一事件有关的事件用相同的事件ID标记，该事件ID是任意选择的数字。使用培训集来了解本次竞赛范围内食品安全事件的含义。至少需要3个包含同一事件信息的个人新闻才能定义事件。
- 基于Training set 开发**无监督**或**半监督算法**，该算法:
	- 识别测试集中所有与食品安全相关的事件，并将涉及同一事件的新闻分组。我们还要求您
	- 确定检测到事件的最早时间戳。还可以在较早的时间戳找到可能具有关于所描述的事件的信息的新数据源。
- 测试集包含来自不同时间段的数据，并且无法在testset中找到和trainingset中相同的事件。

# 数据描述
### Training set
- 包含4183条新闻纪录，分别来自2019-1-23至2019-2-7的社交媒体和**各种语言**的官方数据库；
- 确定了16个主要的食品安全相关事件，这些事件已被标记为任意标识符（Event-ID）1-16。与食品安全不相关的事件没有分配事件ID。

|Field	|Data type	|Example value	|Description|
|-------|-----------|---------------|-----------|
|Date	|Date	|2019-02-07	|Date from timestamp|
|Time	|Time	|08:37:32	|Time from timestamp|
|Training / Test	|String	|Training	|Denotes whether the news item is part of the Training or the Test Set.|
|Event ID	|Integer	|1	|Arbitrarily chosen number to classify news items belonging to the same food-safety-related event.|
|Title	|String	|Pet owners warned of dog food recall https://t.co/gzFn2esLwX|	Title of the news item|
|Link	|String	|https://twitter.com/tweet/status/1093428536595992576	|URL of the news item|
|Abstract	|String	|Pet owners warned of dog food recall https://t.co/gzFn2esLwX https://t.co/USmPcA8iF1	|Abstract / summary of the news item|

# Submission
#### Three files: 
1. Prediction on test set
2. Summary and description of identified events: 1-page
   format:
   
   |Event ID|Number of news items|Timestamp of first news item|Description of the event|
   |----|----|----|----|
   |1   |245 |03.02.201916:00:20	|Canned dog food has been recalled due to excessive levels of Vitamin D.|
   |2	|39	 |05.02.201903:31:32|Pita chips have been recalled due to undeclared milk.|
3. A short report about your findings:
	- Describe the challenge in your words.
	- Describe your overall strategy to tackle the challenge
	- Specify the tools, libraries and algorithms you have used. Try to be as specific as possible.
	- Summarize your findings, i.e. food safety events you have detected.
	- Summarize any challenges that you could not solve and why.
	- Specify any additional data sources that you have used for the challenge, in particular to find earlier news items related to the events than present in the test set.
