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

## 获奖情况

- 2018 NOIP 省二
- 2019 CSP-S 省一
- 2022 蓝桥杯 国二
- 2020 RoboCom-CAIP 国三

## 目标

- 2023 蓝桥杯 国一

- 2023 RoboCom-CAIP 国一

- 2023 GPLT 个人国三

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

## To Do List

- [x] 2022 CCPC 女生赛 补题
- [x] vp Hello 2023
- [ ] 2023 牛客寒假营
    - [ ] 1 补题
    - [ ] 2 补题
    - [ ] 3 补题
    - [ ] 4 补题
    - [ ] 5 补题
    - [ ] 6 补题
- [ ] 重新学习KMP
- [ ] 重新学习Tire

