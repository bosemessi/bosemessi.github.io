---
title: "Where have the triangles gone ?"
layout: post
---

Statsbomb started releasing open data a few years back for hobbyists (like me) to play around with and learn a few things (hopefully ?! ). A big chunk of that open data is dedicated to charting Lionel Messi's journey with Barcelona's first team for about 17 years. That journey finally came to an end come summer of '21....Messi cried, I cried, some people laughed....then we all shrugged and moved on with life. Statsbomb's recent most release completed that data set, providing the data for the final season of Messi at Barcelona. 

One of my goals (that I've been deferring for lack of time for a better part of a year) was to use this data and investigate - to some extent,whatever extent event data permits - some stylistic features of Barcelona's gameplay that everyone (read : Pep and Xavi) keeps talking about. You know what I mean - triangles, triangles and triangles....Now, this is a project that has already been tackled (for a particular season) by a fantastic group of people. This [paper](https://www.nature.com/articles/s41598-019-49969-2) by Prof. Dr. Javier M. Buldú et. al. deals exactly with this, and more. Along with another [paper](https://www.sciencedirect.com/science/article/abs/pii/S0960077920303337) by Prof. Dr. Buldu et.al. , this serves as my starting point. In this post, I will briefly describe the recreation of some of the metrics presented in those two papers using the pass networks of Barcelona and their opposition. 

First things first, you obviously need to download the Statsbomb open data. I pre-process it such that for each game, I have the pass network for Barcelona for the largest chunk of uninterrupted time. This could be from minute 0 till the first substitution, or the first red card (why, hello Lenglet !!). Or this could be from a very early first substitution till the second substitution. 

![Image](https://bosemessi.github.io/images/triangles_directed_.png)
![Image](https://bosemessi.github.io/images/shortest_path_.png)
![Image](https://bosemessi.github.io/images/lambda1_.png)
![Image](https://bosemessi.github.io/images/lambda2_.png)


