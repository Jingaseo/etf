# 黄金ETF实验平台

> 移动端学术问卷系统

本页面概述面向大学生的线上情境实验平台，旨在研究理财信息信源与偶遇式接触对投资意愿的影响。

## About

Build a mobile-first Chinese H5 academic survey platform for a university communication research experiment.

IMPORTANT LANGUAGE REQUIREMENT:
All participant-facing content must be in natural Simplified Chinese.

This includes:
	•	page titles
	•	navigation text
	•	buttons
	•	informed-consent text
	•	survey instructions
	•	survey questions
	•	answer options
	•	validation messages
	•	experimental scenario text
	•	simulated social media post content
	•	completion page

Do not show English text to participants unless it is an unavoidable technical term.

Internal code, database fields, variable names, comments, API configuration, and developer-facing labels may use English.

PROJECT TITLE:
“谁在影响大学生投资意愿？——理财信息信源与偶遇式接触的传播效应”

RESEARCH TYPE:
Quantitative research using an online situational experiment.

RESEARCH DESIGN:
A 3 × 2 between-subjects randomized experiment.

INDEPENDENT VARIABLE 1 — SOURCE TYPE:
	1.	专业财经媒体
	2.	财经类自媒体
	3.	非财经类生活 / 美食博主

INDEPENDENT VARIABLE 2 — EXPOSURE TYPE:
	1.	主动搜索
	2.	偶遇式接触

Each eligible participant must be randomly assigned to exactly one of six experimental groups:

Group 1:
专业财经媒体 × 主动搜索

Group 2:
专业财经媒体 × 偶遇式接触

Group 3:
财经类自媒体 × 主动搜索

Group 4:
财经类自媒体 × 偶遇式接触

Group 5:
非财经类生活 / 美食博主 × 主动搜索

Group 6:
非财经类生活 / 美食博主 × 偶遇式接触

Store the following hidden variables:
	•	group_id
	•	source_type
	•	exposure_type

⸻

SURVEY FLOW

STEP 1 — INFORMED CONSENT

Create a clean Chinese informed-consent page.

The participant-facing text should explain that:
	•	this is an academic study for a university communication research methods course
	•	participation is voluntary
	•	the survey is anonymous
	•	the study does not collect names, student IDs, phone numbers, email addresses, or other directly identifying information
	•	data will only be used for academic statistical analysis
	•	participants will see a simulated social media post
	•	there are no correct or incorrect answers
	•	participants should answer according to their actual feelings
	•	participants should not search for additional information while answering

Include:
“我已阅读上述说明，自愿参加本研究。”

The participant must agree before continuing.

⸻

STEP 2 — PARTICIPANT SCREENING

Question:
“您目前是否为在校大学生？”

Options:
	1.	是，目前为在校本科生
	2.	是，目前为在校硕士研究生
	3.	是，目前为在校博士研究生
	4.	否

Logic:
If the participant selects option 4, end the survey politely.

End-page text:
“感谢您的关注。本研究的调查对象为目前在校大学生，根据您的回答，本次问卷到此结束。”

If the participant selects 1, 2, or 3, continue.

⸻

STEP 3 — RANDOM ASSIGNMENT

Randomly assign each eligible participant with equal probability to one of the six experimental groups.

The participant must NOT see:
	•	group number
	•	source_type
	•	exposure_type
	•	any words such as “实验组”“控制组”“自变量”“操纵”

Store these values invisibly.

⸻

STEP 4 — EXPERIMENTAL SCENARIO

ACTIVE SEARCH CONDITION:

Show this participant-facing Chinese scenario:

“请设想以下情境：

你想主动了解‘黄金ETF’相关信息，于是打开一个平时使用的内容平台，并在搜索框中输入‘黄金ETF’进行搜索。

接下来呈现的是你在搜索结果中看到的一则帖子。

请按照你平时浏览平台内容时的方式阅读，不需要刻意记忆，也不需要额外查询资料。”

INCIDENTAL EXPOSURE CONDITION:

Show:

“请设想以下情境：

你正在像平时一样随手浏览一个常用的内容平台，并没有特意寻找投资理财信息。

浏览过程中，平台向你推荐了下面这则帖子。

请按照你平时浏览平台内容时的方式自然阅读，不需要刻意记忆，也不需要额外查询资料。”

The only meaningful difference between the two scenario conditions should be whether the participant intentionally searched for financial information.

Do NOT add:
	•	“you have spare money”
	•	“you urgently need investment advice”
	•	“you are planning to invest soon”

These would introduce additional motivational variables.

⸻

STEP 5 — SIMULATED SOCIAL MEDIA POST

Display a Xiaohongshu-style simulated mobile social media post.

The post must look realistic but should not directly copy an existing real account.

Across all six conditions, KEEP IDENTICAL:
	•	post title
	•	Gold ETF body text
	•	main visual structure
	•	publication time
	•	like count
	•	favorite count
	•	comment count
	•	hashtags
	•	post length

ONLY CHANGE:
	•	avatar
	•	account name
	•	account description / identity

POST TITLE:

“黄金ETF：普通投资者需要关注哪些因素？”

POST BODY:

“黄金ETF是一类跟踪黄金价格表现的交易型基金，可以通过证券账户进行交易。相比直接购买实物黄金，黄金ETF在交易和持有方面相对便利，流动性也相对较好。

与此同时，黄金ETF的价格会受到国际金价走势、利率水平、汇率变化以及市场预期等多种因素影响，因此仍然存在价格波动以及本金损失的可能。

是否适合配置黄金ETF，需要结合个人的资金安排、风险承受能力和投资期限等因素综合考虑。”

HASHTAGS:

#黄金ETF
#投资理财
#基金知识
#资产配置

ENGAGEMENT NUMBERS:
Likes: 1172
Favorites: 493
Comments: 93

SOURCE CONDITION 1 — PROFESSIONAL FINANCIAL MEDIA

Account name:
“财经观察社”

Account description:
“财经资讯与市场观察｜提供专业的金融市场信息”

SOURCE CONDITION 2 — FINANCIAL SELF-MEDIA CREATOR

Account name:
“阿远聊投资”

Account description:
“财经领域创作者｜分享市场观察与投资知识”

SOURCE CONDITION 3 — NON-FINANCIAL LIFESTYLE / FOOD CREATOR

Account name:
“栗子爱吃喝”

Account description:
“美食探店｜生活分享｜认真吃喝也认真生活”

Do not add additional personal stories or recommendations to the third source condition.
The core post content must remain identical across source conditions.

⸻

STEP 6 — INFORMATION ELABORATION

Use a 5-point Likert scale:

1 = 非常不同意
2 = 比较不同意
3 = 一般
4 = 比较同意
5 = 非常同意

Questions:

ELAB1
“阅读刚才的信息时，我认真思考了其中提供的理由。”

ELAB2
“阅读刚才的信息时，我仔细判断了其中内容是否具有说服力。”

ELAB3
“阅读刚才的信息时，我将其中的信息与自己的投资判断联系起来进行了思考。”

⸻

STEP 7 — RISK PERCEPTION

Same 5-point Likert scale.

RISK1
“我认为黄金ETF存在本金损失的可能。”

RISK2
“我认为黄金ETF未来的投资收益具有较大的不确定性。”

RISK3
“我认为黄金ETF的价格可能出现较明显的波动。”

RISK4
“总体而言，我认为投资黄金ETF具有一定风险。”

⸻

STEP 8 — INVESTMENT INTENTION

Same 5-point Likert scale.

INT1
“阅读上述信息后，我愿意进一步了解黄金ETF。”

INT2
“如果目前有可以自由支配的资金，我会考虑配置黄金ETF。”

INT3
“如果条件允许，我愿意尝试投资黄金ETF。”

⸻

STEP 9 — EXPOSURE MANIPULATION CHECK

Same 5-point Likert scale.

SEARCH
“在刚才的情境中，我是在有明确理财信息需求的情况下看到这则内容的。”

INCIDENTAL
“在刚才的情境中，这则理财信息是在我原本没有主动寻找相关内容的情况下出现的。”

⸻

STEP 10 — SOURCE IDENTITY CHECK

Question:
“您认为刚才发布这则黄金ETF信息的账号最接近以下哪一种类型？”

Options:
	1.	专业财经媒体
	2.	主要发布财经内容的个人自媒体
	3.	主要发布美食、生活等非财经内容的个人博主
	4.	无法判断 / 没有注意

Store as:
sourcecheck

⸻

STEP 11 — SOURCE CREDIBILITY

Use a 7-point semantic differential scale.

CRED1:
1 = 非常不专业
7 = 非常专业

CRED2:
1 = 缺乏相关知识
7 = 具有丰富相关知识

CRED3:
1 = 非常不可信
7 = 非常可信

CRED4:
1 = 非常不可靠
7 = 非常可靠

⸻

STEP 12 — INVESTMENT EXPERIENCE

Question:
“在本次调查之前，您是否有过使用真实资金进行投资或理财的经历？”

Options:
	1.	有
	2.	没有

Store as:
experience

CONDITIONAL LOGIC:

Only if participant selects “有”, show:

“您曾实际接触或配置过以下哪些投资理财产品？（可多选）”

Options:
	•	银行理财产品
	•	基金
	•	ETF
	•	股票
	•	黄金或黄金相关投资产品
	•	债券
	•	其他

Store each multiple-choice option as separate binary variables if possible.

⸻

STEP 13 — FINANCIAL INFORMATION EXPOSURE

Question:
“平时您接触投资理财类信息的频率如何？”
	1.	从不
	2.	很少
	3.	偶尔
	4.	经常
	5.	非常频繁

Store as:
fininfo

⸻

STEP 14 — GOLD ETF FAMILIARITY

Question:
“在参加本次调查之前，您对‘黄金ETF’的了解程度如何？”
	1.	完全不了解
	2.	不太了解
	3.	一般
	4.	比较了解
	5.	非常了解

Store as:
familiar

⸻

STEP 15 — GENERAL RISK ATTITUDE

Use a 5-point Likert scale.

RISKATT1:
“与完全没有波动的理财方式相比，我能够接受一定程度的短期价格波动，以获得潜在更高的收益。”

RISKATT2:
“如果某项投资可能带来较高收益，但同时存在一定亏损风险，我仍可能考虑参与。”

RISKATT3:
“在投资决策中，相比追求更高收益，我通常更加看重本金安全。”

Mark RISKATT3 as a reverse-coded item for later statistical analysis.
Do not reverse the displayed options in the survey interface.

⸻

STEP 16 — DEMOGRAPHICS

Gender:

“您的性别是：”
	1.	男
	2.	女
	3.	其他 / 不便回答

Age:

“您的年龄是：”

Use integer input.

Education stage:

“您目前所在的教育阶段是：”
	1.	本科
	2.	硕士研究生
	3.	博士研究生

Grade:

Options:
	1.	本科一年级
	2.	本科二年级
	3.	本科三年级
	4.	本科四年级及以上
	5.	硕士一年级
	6.	硕士二年级及以上
	7.	博士研究生

Major category:
	1.	哲学
	2.	经济学
	3.	法学
	4.	教育学
	5.	文学
	6.	历史学
	7.	理学
	8.	工学
	9.	农学
	10.	医学
	11.	管理学
	12.	艺术学
	13.	其他

⸻

STEP 17 — PILOT TEST FEEDBACK

This section is for the pilot study only.

REALISM:

“您认为刚才呈现的平台帖子在现实中是否自然、可信？”
	1.	非常不自然
	2.	比较不自然
	3.	一般
	4.	比较自然
	5.	非常自然

SOURCEFIT:

“您是否觉得刚才呈现的账号发布这类黄金ETF内容显得不自然？”
	1.	完全不觉得
	2.	不太觉得
	3.	一般
	4.	比较觉得
	5.	非常觉得

Open feedback:

“如果您认为问卷中存在表述不清、难以理解或其他需要改进的地方，请填写：”

Use optional text input.

⸻

DATA STORAGE

Connect to the existing Supabase project:

gold-etf-survey

Create or use a table named:

survey_responses

Generate one anonymous UUID response_id for every valid participant.

Store at least:

response_id
group_id
source_type
exposure_type
student
elab1
elab2
elab3
risk1
risk2
risk3
risk4
int1
int2
int3
search
incidental
sourcecheck
cred1
cred2
cred3
cred4
experience
investment_products
fininfo
familiar
riskatt1
riskatt2
riskatt3
gender
age
education_stage
grade
major
realism
sourcefit
feedback
started_at
submitted_at
duration_sec

⸻

DATA SECURITY

Do not collect:
	•	name
	•	student ID
	•	phone number
	•	email
	•	IP address for research analysis
	•	precise location

Use Row Level Security.

Anonymous survey participants should only be able to INSERT a new response.

They must NOT be able to:
	•	read other responses
	•	update submitted responses
	•	delete responses

Do not expose Supabase service-role secrets in frontend code.

⸻

DESIGN REQUIREMENTS

The participant-facing interface must be entirely in Simplified Chinese.

Design style:
	•	mobile-first
	•	suitable for WeChat and mobile browser
	•	clean academic visual style
	•	simple white or light-gray background
	•	one logical section per screen
	•	clear progress indicator
	•	large touch-friendly options
	•	no unnecessary animations
	•	accessible typography
	•	responsive layout

The simulated social media post should visually resemble a modern Chinese lifestyle content platform, but should not copy protected branding or logos exactly.

⸻

COMPLETION PAGE

After successful submission show:

“提交成功，感谢您的参与！

您的回答已被匿名记录，仅用于本次学术研究的统计分析。”

Do not show the participant their experimental group.

⸻

BUILD PRIORITY

First build a reliable working version.

Prioritize:
	1.	correct random assignment
	2.	correct conditional logic
	3.	correct Supabase data submission
	4.	complete Chinese questionnaire
	5.	mobile usability
	6.	clean visual design

Do not add unnecessary features before the core research workflow is working.

## Development

A single static `index.html` — no build step, no dependencies.

```bash
npx serve .
```

---

Generated by [Muse](https://usemuse.dev).
