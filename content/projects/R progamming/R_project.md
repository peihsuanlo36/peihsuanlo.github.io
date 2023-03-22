---
title: "World Happiness Report 分析"
date: 2022-11-18
description: Introduction to Sample Post
menu:
  sidebar:
    name: World Happiness Report 分析
    identifier: projects-r-project
    parent: projects
    weight: 20
tags: ["Basic", "Multi-lingual"]
categories: ["Basic"]
---

> 本分析為 <商業分析-R> 期末個人專案 

## 1. Introduction

本篇為介紹使用 R 作為工具分析 World happiness report。  
<br>
以下為本次分析所使用的 method:
- EDA
- decision tree

預計透過本資料,去分析會影響各大洲幸福指數的因素,以及將國家分成是高收入國家以及低收入國家的幸福分數分析,最後透過決策樹分析,透過現有
因素(扣除人均 GDP 的因素),去預測高收入國家抑或是低收入國家,並觀察其中的決策因素,去了解到通常高收入國家會具有的特色。

## 2. Research motivation
在本學期 (109-2) 在總體經濟學課堂中老師有提及幸福指數的相關新聞,在搜尋資料時發現 Kaggle 上有整理和 World Happiness Report 相關的資料,因此決定進行相關的分析。本資料在評估幸福分數時,在 2019 年的數據中預計要討論以下六項變數,以下會針對各指數代表意義進行進一步說明。

## 3. Variables
1. 人均 GDP(GDP per capita):  
<br>
可以視為觀察各國經濟狀況、消費能力的指標

2. 健康平均餘命(Health life expectancy):  
<br>
代表的則是代表一個人處於完 全健康、無失能或疾病的期望歲數,可以為是一個國家的人民健康情形。

3. 社會支持 (Social support):  
<br>
詢問的問題為“If you were in trouble, do you have relatives or friends you can count
on to help you whenever you need them, or not ? ” 可視為是社會中關係互動上對幸福指數的影響指標

4. 生活中做選擇的自由程度(Freedom to make life choices) :  
<br>
詢問的問題為“Are you satisfied or dissatisfied with your freedom to choose what
you do with your life?” 可視為是人民對於在自己國家行為自由程度的認知

5. 慷慨程度 (Generosity) :  
<br>
詢問的問題為“Have you donated money to a charity in the past month?” on GDP per capita. 可視為是人民願意捐款的比例。

6. 貪腐程度(Perceptions of corruption) :  
<br>
詢問的問題為 “Is corruption widespread throughout the government or not?” 以及 “Is corruption widespread within businesses or not?”,可視為是人民對自己國家貪腐程度的認知。

## 4. Analysis
 #### 4.1 EDA
  首先要先透過 EDA 了解整筆資料的特性。
  - Heat map: 瞭解變數間的相關性
  ```
  Num.cols <- sapply(Happiness, is.numeric)
  Cor.data <- cor(Happiness[, Num.cols]
  corrplot(Cor.data, method = 'color') 
  ```
  // 補圖片

 #### 4.2 Decision tree




## 5. Conclusion
在依照各大洲分類下去觀察各項因素相關性時,可以發現各大洲間和幸福程度正相關性較強的因素不完全一致,雖然我們能根據能夠數據化討論的因素,如:
人均 GDP、健康平均餘命再佐以其他面向單單詢問一題的 binary response 平均分數進行評價,去獲得全球整體的情形;然而若是要更針對各區域進行分析時,可能需要針對當地的文化、習慣、民情等進行更深一步的分析,才能了解該區域的人能讓感到幸福的因素。在這項分析下,我們也了解到,金錢收入並非唯一能帶來快樂的因素,故未來政府在推行政策時,如果目標是為了使人民獲得最大福祉、感到幸福,就應該要考量更多面向的政策,而不是一昧地拚經濟發大財。

## References:
- Kaggle data source: https://www.kaggle.com/datasets/unsdsn/world-happiness 



