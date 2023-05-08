# PHarr

现任集训队队长

CodeForces：`PHarr_`

AtCoder：`PHarr_`

email：xin.mai@forxmail.com

[博客](https://www.cnblogs.com/PHarr)

[Templates](https://gitee.com/PHarr/pharr-xcpc-templates/blob/master/out/main.pdf)

[题解目录](https://zhuanlan.zhihu.com/p/601815556)

---

## 易错点

1. 在需要用差分维护区间修改的情况下，如果要进行离散化，离散化的值不应该是$[l,r]$而是$[l,r+1]$。
2. 在 CF 上`unordered_map`会被Hack，导致复杂度退化到$O(N)$。
3. `multiset::erase()`函数可以接受三种参数
    1. `void erase (iterator position_of_iterator);`删除特定位置的参数
    2. `size_type erase (const value_type& contant_value);`删除所有此值的实例
    3. `void erase (iterator starting_iterator, iterator ending_iterator);`删除两个迭代器之间的所有元素
4. 对于并查集本身就可以维护父节点的。如果要维护有向无环图，并且只需要知道祖先节点是谁的话，完全可以使用并查集来维护，可以使用路径压缩，但不能用按秩合并，并且注意合并的顺序不能错

## 获奖情况

- 2018 NOIP 省二
- 2019 CSP-S 省一
- 2022 蓝桥杯 国二
- 2022 RoboCom-CAIP 国三
- 2023 CCCC-GPLT 个人国二

## 目标

- 2023 蓝桥杯 国一
- 2023 RoboCom-CAIP 国一
- 2024 CCCC-GPLT 个人国二

## 比赛记录

**4.8 十四届蓝桥杯省赛**

省一

感觉难度大幅度下降了，虽然还是省一但实际上的排名相比去年下降了。

**4.16 21st UESTC Programming Contest**

Silver Medalist Solver 4 problems

第一次进 985 大学，体验很好。封榜后出了一题很开心。题目没有的读完是比较 sad 的。赛后想了想可以出I和 K。

比较惊喜的是 E 题想要用 python 写，但是没有安装 python 的 IDE，最后用记事本加命令行写完了这道题。

**4.22 2023 CCCC-GPLT**

个人国三、团体国三、校省银

首先反思自己，这场比赛赛场环境比较差，但是没有完全发挥出水平，赛时忘记看榜了，导致硬磕了好久的 L2-3直到最后也只有 3 分，没有去写更好做的 L3-2。

今年是学校的滑铁卢了，我作为队长也有很大的责任，没能很好的起到带头作用，在日常训练的中对队员的要求太低了。我认为首先应该提高自己的训练强度，其次严格要求各位队员。希望明年可以重新夺回四川省冠军。

## 训练记录

### 2023 Winter

**2.8 2022 CCPC 女生赛 6T**

[题解](https://www.cnblogs.com/PHarr/p/17112120.html)

这套题目6题手快有金，感觉比去年的女生赛要难一点，太菜了，女生赛都拿不了金。

**2.10 2019 ICPC 雅加达 4T**

同步赛有759有效参赛人数，我的名次是133铜牌。[现场赛](https://competition.binus.ac.id/icpc2019/final.html) 16名是6题，我能排21还是有不小的差距的。K题看题解是矩阵快速幂，可是我矩阵快速幂已经忘完了快。

**2.11 2022 ICPC Poland 1T**

现场赛要7T才能拿铜，不得不说自己的水平离拿牌还有很大的差距，并且这套题的英文也是很难懂的。

**2.11 AtCoder Beginner Contest 289 5T**

[题解](https://www.cnblogs.com/PHarr/p/17121235.html)

这套比赛总体来说打的中规中矩把，但是E题的写法我写的太复杂了，导致被卡了参数不得不使用了更优秀的剪枝和更好的哈希函数。然后这套比赛的B题 也是我打过的atc中读题比较困难的，可能跟没有文化背景有关？今天一天读题都不太顺~~

**2.13 蓝桥杯模拟赛 4**

[题解](https://www.cnblogs.com/PHarr/p/17118367.html)

这套题总体还算简单，一共用了三个小时差不多就做完了

**2.15 2020 CCPC Henan 4T**

[题解](https://www.cnblogs.com/PHarr/p/17124729.html)

比赛中规中矩吧。不过中间因为离散化的问题WA了一发比较可惜，看了一眼现场赛的榜应该是金尾，没能解出5题还是比较可惜。

**2.17 The 4th Hangzhou Normal University Freshman**

[题解](https://www.cnblogs.com/PHarr/p/17131773.html)

几乎是卡着最后的时间AK了，看了看榜似乎现场赛可以夺冠？不过新生赛罢了，看cf上的大哥三个小时就能ak了，前期做题有点慢说实话。

### 2023 Spring

**3.4 SMU Spring 2023 Recover Contest Round 1 7T**

[题解](https://www.cnblogs.com/PHarr/p/17180708.html)

恢复性训练第一场，读题一般手感一般，还是需要联系读题和手速

**3.4 2022 ICPC Taoyuan（UCUP）3T**

这套算是着这几场比较简单的了，可惜时间不太充足只做了三道题，如果时间给够组队打应该有5到6题的水平

**3.4 AtCoder Beginner Contest 292 4T**

[题解](https://www.cnblogs.com/PHarr/p/17181619.html)

今天的最后一套比赛，感觉没有打出该有的水平。f是一个比较巧妙的计算几何，而且还有比较高的精度要求。

补题的时候发现E题想复杂了，其实可以不用 Flyod 直接用用 bfs 就行。

**3.7 SMU Spring 2023 Trial Contest Round 2 4.95T**

[题解](https://www.cnblogs.com/PHarr/p/17190077.html)

一套来自 OI的题目，前期做的不太顺利，这套题的 B 题我倒是想出来了最简单的最优秀的算法。

补题的时候发现G题是我CSP-S 2019时写过的题目，并且我赛场上拿到了95分，但是今天只拿到了50分，我是不是智商退化了？

**3.9 AtCoder Beginner Contest 052 AK**

[题解](https://www.cnblogs.com/PHarr/p/17199169.html)

拿来练手速的题目，感觉写的还是有点慢了。D题一开始想错了以为是 DP,但实际上是贪心。

**3.9 2023 CCCC-GPLT USST 选拔赛 68分**

感觉这场除了赛制和天梯类似其他根本和天梯就不一样把，好难！！

不过这套题让我 觉得最有意思的点就是F题，在要维护两种权值的情况下，可用类似字符串哈希的方式把两个全职合并成一个权值。

**3.9 AtCoder Beginner Contest 293 4T**

[题解](https://www.cnblogs.com/PHarr/p/17234336.html)

打这套题的时候好困，这把狠狠的掉分了。补题的时候发现其实E题还是蛮简单的。

**3.13 Hello 2023 3T**

[题解](https://www.cnblogs.com/PHarr/p/17220292.html)

这套题算是正常发挥了吧，唯一有点可惜的就是 umap 被卡掉了，问了群友得到的结论是，因为 umap 的哈希函数是固定的，所以可以通过制造哈希冲突的方式使得 umap 的复杂度退化为$O(N)$。

**3.20 Codeforces Round 859 (Div. 4) 7T**

[题解](https://www.cnblogs.com/PHarr/p/17237610.html)

好久没有打 cf 了还有点手生，今天这套题目总体不难，交互题把二分的答案输错了，白吃一个罚时。G题猜了一个结论，但是没想明白怎么证明。学妹好强哇，要加训了。

**3.21 SMU Spring 2023 Trial Contest Round 1 AK**

[题解](https://www.cnblogs.com/PHarr/p/17241435.html)

题目来自远古 cf，果然早期的 cf 还是比较典的算法题。H题被卡 dfs是比较讨厌的，明明思路一样的但是 bfs 却可以跑的飞快。F题四分钟吃了四个罚时有点抽象，现在想想当时还是太紧张了点。至于G题似乎可以计算一下偏移量，但是似乎计算偏移量的不能压缩空间，感觉还是两次 01背包比较好玩。

**3.23 Educational Codeforces Round 145 (Rated for Div. 2) 2T**

[题解](https://www.cnblogs.com/PHarr/p/17284145.html)

有点可惜，赛时只能做两题，其实C题感觉还是比较简单的了

补题的时候发现 D题的 DP 其实不太难想，主要是状态的设计。

**3.25 西南民族大学2023天梯选拔赛 196分**

[题解](https://www.cnblogs.com/PHarr/p/17258657.html)

题目来说还是比较简单的，就是两道模拟题卡的有点久，最后给L3 剩下的时间自由 20 分钟了，还是要多熟悉一下天梯的赛制。其次就是 L2-4 赛时没有反应过来可以用搜索的方式有点可惜

**3.25 AtCoder Beginner Contest 295 4T**

[题解](https://www.cnblogs.com/PHarr/p/17266778.html)

这套题做起来手感还行，前四题没什么障碍，只是 EF看完之后完全没思路，但是这是我少有的看到 G题能出思路，只是一直都在写并查集的按秩合并忘记了并查集实际上还是可以为父亲节点的。

补题的时候仔细想了想其实E题的难点主要是在期望计算的转换上，这种方式之前确实没有遇到过，还是比赛打的太少了。

**3.20-3.26 第一周题单 DP 专题**

[题解](https://www.cnblogs.com/PHarr/p/17262905.html)

都是一些比较板的 DP 题，然后复习了一下用 `long long` 手动实现 `__int128`。并且刷题单的过程中找到了 kuangbing 的博客，可以翻翻里面有没有什么好东西。

**3.29 AtCoder Beginner Contest 245 6T**

[题解](https://www.cnblogs.com/PHarr/p/17270716.html)

这套题算是 vp 的手感还是很好的，早上起来打比赛思路似乎并没有什么影响。

结合上一场 abc 的表现，水平似乎是在提高。不过这次的 G 题标答的解法还是有点难写，抄了 dls 的代码学会了一个新的小技巧。

**4.1 21st UESTC Programming Contest - Preliminary 8T**

队友实力带飞，总榜 rk47，顺利挺进决赛。

**4.2 西南民族大学 春季 2023 训练赛 3**



**4.4 西南民族大学 春季 2023 训练赛 4 7T**

[题解](https://www.cnblogs.com/PHarr/p/17289568.html)

赛时差一题 ak，这套蓝桥杯赛制的题目还是给的比较简单。最后一道 dp其实也不太难吧，只是网上的题解写的太烂了吧。本质上还是数据结构优化 DP

**4.4 Codeforces Round 863 (Div. 3) 4T**

[题解](https://www.cnblogs.com/PHarr/p/17289813.html)

赛时只出四题，水平还是欠点，能出 E 但是不能出 D 比较悲伤。赛时我的思路是直接去拼矩形，但是几位大佬的思路都是去减矩形，思维还是略有欠缺。

**4.6 Educational Codeforces Round 146 (Rated for Div. 2) 2T**

[题解](https://www.cnblogs.com/PHarr/p/17297514.html)

好困，看到 unr 写了两题就直接去睡觉了，但是赛后看了看 C题可能赛时 20 分钟就能出。

**4.9 西南民族大学 春季 2023 训练赛 5**

[题解](https://www.cnblogs.com/PHarr/p/17304398.html)

L3-1读错题了，丢到了 12 分，L3-2比赛时没有仔细想忘记写最暴力的 01 背包丢到 19 分。如果把所有的分数的拿满应该是国二的

**4.9 AtCoder Beginner Contest 297**

[题解](https://www.cnblogs.com/PHarr/p/17307631.html)

赛时做出来 E 题，应该是这场比赛比较简单的原因，赛后发现 E F其实都不太难。

**4.11 西南民族大学 春季 2023 训练赛 6**

[题解](https://www.cnblogs.com/PHarr/p/17311365.html)

这套比赛是去年的比赛题，印象中去年赛场上只能拿到 160+，今年可以稳国二，还是有进步的吧。教练说今年的难度会下调，希望可以拿到国二。

再说比赛本身，L3-1感觉题目描述还是比较烦的，太不好懂了。

**4.15 西南民族大学 春季 2023 训练赛 7 **

[题解](https://www.cnblogs.com/PHarr/p/17321411.html)

L3-1 看漏的一个重要条件有向图，痛失12分，不然这场是有可能拿到第一的。还是要多认真读题。

**4.15 Codeforces Round 866 (Div. 2)**

[题解](https://www.cnblogs.com/PHarr/p/17331571.html)

比较顺利的开出了C题，感觉还是小有进步的。

**4.15 AtCoder Beginner Contest 298**

[题解](https://www.cnblogs.com/PHarr/p/17334309.html)

好困写了四题就下班了。

补题的时候发现 F 题其实很简单，分类讨论一下就好了。E 题时候概率 dp，还是得学一学。

**4.18 西南民族大学 春季 2023 训练赛 8**

[题解](https://www.cnblogs.com/PHarr/p/17331203.html)

L3-1被假题意演了，最近几次的发挥都还算值比较稳定的可以上 200 分，希望今天天梯赛至少捞一个国三吧。听说难度会下降，希望有国二的。

**4.21 牛客小白月赛71**

[题解](https://www.cnblogs.com/PHarr/p/17350629.html)

赛时被精度搞心情，最后还是用 python 水过去了，整体来说难度不太高，但是 EF感觉还是一眼没思路。

**4.23 SMU Spring 2023 Trial Contest Round 9**

[题解](https://www.cnblogs.com/PHarr/p/17346626.html)

1h 不到 AK了比 18 年的 j 神快一点，总体来说难度不高。

**4.24 Codeforces Round 867 (Div. 3)**

[题解](https://www.cnblogs.com/PHarr/p/17357141.html)

赛时的状态不太好，只做了四道题，E 题赛时的做法其实已经八九不离十了，但是没有坚持写完。F题赛时的做法也是只差一点了，sad。而且这次的 G1其实很好写的，G2赛后想想其实也不难。

**4.25 SMU Spring 2023 Trial Contest Round 10**

[题解](https://www.cnblogs.com/PHarr/p/17352861.html)

这套题感觉难度还是比上一套要高一些，白吃两个罚时比较弱智。而且还是 WA1，这种问题在正式比赛中绝对不能出现。

**4.26 Educational Codeforces Round 1**

[题解](https://www.cnblogs.com/PHarr/p/17364305.html)

之后要多刷 Edu Round，每周至少一套吧。

这套题我自己独立可以写到 C 题，然后看题解补到了 E。不得不说 Edu还是套路多些。

**4.29 2023牛客五一集训派对day1**

**AtCoder Beginner Contest 231**

[题解](https://www.cnblogs.com/PHarr/p/17365559.html)

这套比赛是 vp 的，感觉难度还挺高的。

**4.29 AtCoder Beginner Contest 300**

[题解](https://www.cnblogs.com/PHarr/p/17369742.html)

赛时没出 E 题，还是比较悲伤的。上分失败了。

怎么说呢，赛后整理的时候发现这场暴力很多呀。

**5.2 SMU Spring 2023 Contest Round 1**



很有难度的一套比赛，赛后看了牛客的榜感觉自己还有很大的差距。

**5.3 2022-2023 ICPC Asia Pacific - Taoyuan Regional Contest**



桃园区域赛，感觉还是比大陆赛区似乎友好一些？看了原榜应该是铜牌比较靠前的。

这题有两个地方比较难吧，一个是 B 题的推式子，另一个是 D 题的读题。

**5.4 AtCoder Beginner Contest 242**

[题解](https://www.cnblogs.com/PHarr/p/17378464.html)

vp 了一下，只能做四道题还是很丢脸。G是莫队模板？但是不会好焦虑。

**5.7 Codeforces Round 871 (Div. 4)**

[题解](https://www.cnblogs.com/PHarr/p/17382967.html)

赛时倒开写了两道就睡觉了，赛后补了一下，感觉 div4似乎在逐渐上强度。

**5.7 2023 SMU RoboCom-CAIP 选拔赛**

[题解](https://www.cnblogs.com/PHarr/p/17382968.html)

这套题是我提前验题，总体感觉不太难，但是大家的分数有点低了

**5.7 XJTUPC2023**

现场赛金牌，但是同步赛没有榜，没法跟榜做，有些可惜。

## To Do List

- [x] 2022 CCPC 女生赛 补题
- [x] vp Hello 2023
- [ ] 2023 牛客寒假营
    - [x] 1 补题
    - [x] 2 补题
    - [x] 3 补题
    - [ ] 4 补题
    - [ ] 5 补题
    - [ ] 6 补题
- [ ] 重新学习KMP
- [ ] 重新学习Tire

