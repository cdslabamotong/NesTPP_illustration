---
layout: page
title: An illustration for NesTPP

--------

---

<h2>DeepNest Preliminary Study</h2> 

This is a preliminary study of single topic DeepNest.

Our data is the complete set of topic-related threads and associated replies retrieved from Reddit. We crawled data from the most popular subforums - Sports subforum. For the sports data, we select all main threads with replies related to the famous NBA player - LeBron James during the NBA Playoffs (April 2019) that attracts most of the attention in a season.

We illustrate the improvments of our model by comparing with several state-of-the-art approaches in different prediction tasks, and the following figure is the Mean Absolute Error (MAE) in the simulated reply number of each main thread comparing with the real-world data in the sports dataset.

Specifically, we apply cross-validation to measure the effectiveness of our model. We select a total of $10$ groups of randomly-picked continuous main threads from sports datasets with window size 150, we then simulate the future 20 main threads and linked replies for measuring the MAE in the amount of replies for each group. The labels G1 - G5 in x-axis represent the average MAE for the first events, the first 5 events, the first 10 events, the first 15 events, and the total 20 events. As shown in the following figure, in the task of predicting the future reply number of each main therad, NesTPP outperforms other baselines and achieve lower error consistently.

<div style="text-align:center"><img src="https://s2.ax1x.com/2019/07/27/eKtmTg.png" alt="figure1" width="600"/></div>   

The code for reproducing the simulation result can be found [here](https://github.com/lingchen0331/NesTPP/blob/master/ntpp.py).
 

