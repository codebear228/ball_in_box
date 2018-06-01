# ball_in_box lab1

## envs

    requirements.txt
    大部分主机上自带

    ide:pycharm
    ball_in_box/area_sum 是程序入口
    ball_in_box/ballinbox_random 是简单的随机算法,来每次找一个最大圆
    ball_in_box/ballinbox_iter 是枚举点,每次找一个半径最大圆
    ball_in_box/ballinbox 是枚举之后在随机移动局部最优解,希望找到比贪心更好的方案,类似退火算法

## problem description

    二维平面上,有一个(-1,1) (1,-1)的正方形,与m个坐标(mxi,myi)
    已知有n个可变半径的 无边界圆(或者"空") 可供放置在正方形内,但不能交叠,同时不能包含上面的m个坐标;
    求所有圆的最大面积

## 朴素想法
已知把该问题圆面积变成圆周长,是个未解决的开放问题
所以如何快速得到更优解才是需要考虑的
    
1. 用了一些必要的优化以供暴力迭代,并且把图绘出来了
2. 还做了一点微小的贡献就是让运行的时间稳定在1s内,用ax^b拟合
3. 通过特例发现,贪心算法是错误的
4. 同时随机算法不知道为什么发挥的不好

# 测试

m |blockers| ans | tar
--- | --- |---| ---
1|[]|3.140071 | pi |
2|[]|3.20655|3.23407|