# ReplyChef 人味回复指南

来源：网上被读者夸「像真人」的餐厅老板回差评实例（TripAdvisor、Toast、Reddit 热帖的新闻转载等），加上被读者骂「一看就是 AI」的反例，归纳出来的。这份规则同时写进了 demo 的 prompt，也是 demo 里「人味检查」的打分依据。

## 一、真人回复长什么样（对照反例）

| 真人 | AI / 模板 |
|---|---|
| 开头直接叫名字，或者直接开讲："So, we're glad you enjoyed the brisket." | "Dear valued customer, thank you for your feedback" |
| 前两句就复述评论里的具体细节：菜名、等了多久、前台说了什么 | 一段话换到任何评论下面都能用 |
| 到处是缩写：I'm, we've, didn't, that's | 一个缩写都没有，全是 "We are", "I would like to" |
| 有 "I"："That's on me." "I've talked to the server." | 从头到尾都是 "we / our team / management" |
| 说清楚到底发生了什么："It was a night where it seemed to snowball." "It was her first day." | "fell below the standards we strive to maintain" |
| 道歉一次，最多两次 | 连着道歉五次，读起来像在慌 |
| 句子长短不一，有很短的："But I won't." "Yeah." | 每句都 12 到 18 个词，节奏像机器 |
| 2 到 3 个短段落 | 一整块，或者带 bullet / 标题 |
| 署名是真名："Andy" "Rik, Director of Operations" "Brad K." | "Management" "The Team" "Guest Relations" |
| 偶尔有小瑕疵：漏个逗号、"a epic fail"、用 & | 语法完美，措辞像公关稿 |
| 一个口头禅就够："Honestly," "Yeah," "to be fair" | 要么没有，要么堆一堆显得刻意 |
| 邀请回访很具体："come try the shake the way it's supposed to be made" | "we'd love another chance to exceed your expectations" |

## 二、禁用短语（读者点名过的）

- We apologize for any inconvenience / sorry for the inconvenience / any inconvenience this may have caused
- Your feedback is important to us / We value your feedback / valuable feedback
- We strive to... / the standards we strive to maintain
- We take this very seriously
- This isn't our usual standard（后面不说到底怎么了的时候）
- We're sorry you feel that way / sorry if...（给感受道歉，不给事情道歉）
- Rest assured
- Please accept our sincerest apologies
- Please contact our customer service team
- We pride ourselves on...（开头用就是套话）
- Dear valued customer / Dear Guest
- not only meet but exceed expectations / measures of improvement / training tool
- 防御型："We've never had this problem before"

## 三、可以机器检查的规则（demo 里的「人味检查」）

1. 缩写：差评回复 60 词以上至少 2 个，60 词以下至少 1 个；25 词以下的好评短回复不要求
2. 禁用短语：0 个
3. sorry / apologize：不超过 2 次
4. 长度：差评回复 35 到 110 词；好评回复 60 词以内
5. 分段：差评回复至少 2 段
6. 前 80 个字符里出现顾客的名字，且不以 Dear 开头
7. 最后一行是短署名（4 个词以内），含经理的名字
8. 差评回复里至少有一个 "I"

demo 里每条草稿下面会实时显示这 8 项过了几项，Andy 手动改的时候也会跟着变。

## 四、写法模板（不是套话模板，是结构）

**1 到 2 星，确实出了问题**
1. 名字 + 复述他遇到的具体事（1 句）
2. 认账，用大白话（"That's on me." / "no good answer for that"）
3. 说发生了什么 + 一个跟他投诉相关的改进（2 到 3 句）
4. 邀请直接联系经理本人（邮箱），不公开送东西
5. 真名署名

**3 星，评价公允**
2 到 4 句就够：谢他说得具体、说一件会做的事、署名。不要长篇道歉。

**1 星但事实有误（比如把 calzone 当成半个披萨）**
心平气和纠正一次，为「让你困惑」道歉一次，不争论。

**4 到 5 星**
1 到 3 句，点名他夸的那道菜或那个细节。

## 五、demo 里 prompt 的关键部分

- 餐厅事实只从「餐厅资料」页取，禁止编造改进措施
- 「Andy 说话的习惯」字段：口头禅、对厨房 / 前台的叫法、引以为傲的菜，AI 会模仿
- 署名给 3 个可选，每条随机换，避免所有回复结尾一模一样（被 reputation 圈子点名为「模板特征」）
- 两个 few-shot 例子展示目标口吻，内容和 Chef Fei 无关，防止照抄
- 最后一条：朗读测试。如果这句话当面对顾客说会显得可笑，删掉

## 六、平台方自己的建议（简要）

- Google：用名字称呼，回应具体内容，对话式而非营销式，真诚道歉，复杂问题转私下解决
- Yelp：先公开回复再私信；不要请求对方改评分；一天内个性化回复的商家，用户升级评分的可能性高 33%
- TripAdvisor：短、专业、正面；「像当面说话那样写」

## 来源

- https://www.aol.com/news/woman-bad-review-backfires-restaurant-211623623.html （bay leaf 回复）
- https://scoop.upworthy.com/shop-owners-response-to-1-star-review-over-homeless-man-outside-the-store-offers-a-valuable-lesson （Nomad Donuts）
- https://pos.toasttab.com/blog/on-the-line/how-to-respond-to-negative-review-of-your-restaurant （Boloco）
- https://www.tripadvisor.com/business/insights/restaurants/resources/responding-to-negative-reviews
- https://www.tripadvisor.com/business/insights/restaurants/success-stories/get-inspired-management-responses
- https://www.tripadvisor.com/ShowUserReviews-g155019-d6762792-r564833016-Cluny_Bistro-Toronto_Ontario.html
- https://ronntorossian.medium.com/responding-to-negative-reviews-without-sounding-robotic-01f89b45d9f3
- https://dinereplies.com/blog/respond-negative-restaurant-review
- https://www.ionhospitality.com/2026/09/06/respond-to-bad-reviews/
- https://support.google.com/business/answer/3474122?hl=en
- https://business.yelp.com/resources/articles/tips-for-responding-to-reviews-on-yelp/
- https://business.yelp.com/resources/articles/how-to-respond-to-online-reviews?domain=restaurants
