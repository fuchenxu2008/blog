---
title: Linear Regression and Cost Function
date: "2018-12-29T18:31:44.933Z"
spoiler: "Get the best line so that the average squared vertical distances of the points from the line will be the least."
---

### Cost Function
![](https://ws4.sinaimg.cn/large/006tNbRwly1fynsezngurj31ck0qw0z6.jpg)
![](https://ws3.sinaimg.cn/large/006tNbRwly1fynsfmdx71j30i60aatak.jpg)

Our objective is to get the best possible line. The best possible line will be such so that the average squared vertical distances of the scattered points from the line will be the least. Ideally, the line should pass through all the points of our training data set. In such a case, the value of J(θ0,θ1) will be 0. The following example shows the ideal situation where we have a cost function of 0.

![](https://ws1.sinaimg.cn/large/006tNbRwly1fynsis7ygzj30ba06adgi.jpg)
![](https://ws3.sinaimg.cn/large/006tNbRwly1fynsix5f5nj308g081dge.jpg)

Thus as a goal, we should try to minimize the cost function. In this case, θ1 = 1 is our global minimum.

![](https://ws3.sinaimg.cn/large/006tNbRwly1fynsl1vn46j30ic09qgo3.jpg)

Taking any color and going along the 'circle', one would expect to get the same value of the cost function. For example, the three green points found on the green line above have the same value for J(θ0,θ1) and as a result, they are found along the same line.

![](https://ws3.sinaimg.cn/large/006tNbRwly1fynslczvx0j30hy08qgns.jpg)

The graph above minimizes the cost function as much as possible. Plotting those values on our graph to the right seems to put our point in the center of the inner most 'circle'.