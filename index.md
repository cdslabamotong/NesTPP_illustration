---
layout: page
title: An illustration for NesTPP

--------

NesTPP: Modeling Information Diffusion in Online Discussion Forum
---
We study the online discussion forum that is generally tree-like in structure: a forum can contain several subforums. Within a subforum, each new discussion started is called a thread and can be replied by online users. A list of main threads and linked replies constitute the series of reply-trees. Each reply-tree is rooted in the main thread and joined by replies. In our intuition, the occurrence of a new main thread not only depends on the impact from all previous main threads but also from all the associated replies. Moreover, the generation of reply events relies on the influence of the linked main threads as well.

Our data is the complete set of topic-related threads and associated replies retrieved from Reddit. We crawled data from the most popular subforums - Sports subforum. For the sports data, we select all main threads with replies related to the famous NBA player - LeBron James during the NBA Playoffs (April 2019) that attracts most of the attention in a season.

We illustrate the improvments of our model by comparing with several state-of-the-art approaches in different prediction tasks, and the following figure is the Mean Absolute Error (MAE) in the simulated reply number of each main thread comparing with the real-world data in the sports dataset.

Specifically, we apply cross-validation to measure the effectiveness of our model. We select a total of $10$ groups of randomly-picked continuous main threads from sports datasets with window size $150$, we then simulate the future $20$ main threads and linked replies for measuring the MAE in the amount of replies for each group. The labels $G1$ - $G5$ in x-axis represent the average MAE for the first events, the first $5$ events, the first $10$ events, the first $15$ events, and the total $20$ events. As shown in the following figure, in the task of predicting the future reply number of each main therad, NesTPP outperforms other baselines and achieve lower error consistently.

<div style="text-align:center"><img src="https://s2.ax1x.com/2019/07/27/eKtmTg.png" alt="figure1" width="600"/></div>   

The code for reproducing the simulation result can be found [here](https://github.com/lingchen0331/NesTPP/blob/master/ntpp.py)
 

