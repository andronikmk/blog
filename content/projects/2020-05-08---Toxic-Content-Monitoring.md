---
title: Toxic Content Monitoring
date: "2020-05"
template: "project"
draft: false
slug: "toxic-content-monitoring"
category: "Natural Language Processing"
tags:
  - "Natural Language Processing"
  - "Project"
description: "In recent years, many articles have highlighted the toxic world of internet comments and intenet posts."
---
[![Alt text](/media/icons/GitHub-Mark-32px.png)](https://github.com/andronikmk/toxic-content-monitoring)


## Introduction

<p style="text-align: justify;"> 
In recent years, many articles have highlighted the toxic world of internet comments and intenet posts.
Reddit has announced its "anti-evil team" and YouTube has diasbled the comments section on videos featuring
children. The internet of today is a far cry from the early days when cyber-utopians heralded in a new era
of human collaboration and communication. While furfilling my role as a <i>Data Science Intern</i> at Big Armor, 
our team was tasked to come up with an application to be used by social workers to monitor and report potentially
harmful and toxic online behavior. Systems exist to detect toxicity, suicidality, and other concerning behavior, but
they are all either whole system programs or limited to a small number of topics.
The model that performs best is a Bi-directional LSTM + GRU neural network made with PyTorch.
</p>

## Models and Metrics

<p style="text-align: justify;"> 
Our model is used to determine if text contains the following characteristics:
</p>

+ toxic
+ severe toxic
+ obscene
+ threat
+ insult
+ identity hate

<p style="text-align: justify;">
The API returns clean text, labeled True or False, and the predicted probability of each. The current model is a Bi-directional LSTM + GRU neural network made with
PyTorch, assuming FastText vectorization. Considerable preprocessing is
performed on the text before vectorization. The metrics used for evaluation
are F1 and ROC-AUC scores.  

</p>

<img src="/media/toxic-content-monitoring/baselines-with-labels.png" alt="Baseline">

<p style="text-align: justify;"> 
F1 score is defined as the harmonic mean between precision and recall and is measured on a scale from 0 to 1. Recall demonstrates how effectively this model identifies all relevant instances of toxicity. Precision demonstrates how effectively the model returns only these relevant instances. The AUC score represents the measure of separability, in this case, distinguishing between toxic and non-toxic content. Also on a scale of 0 to 1, a high AUC score indicates the model successfully classifies toxic vs non-toxic. The ROC represents
the probability curve. The F1 score for this model is 0.753 and the ROC-AUC score is 0.987.
The figure above shows all the various models our team assembled with top performing model show on the top right hand side
of the chart.
</p>

## Presentation
<div style="position: relative; padding-bottom: 56.25%; height: 0;"><iframe src="https://www.loom.com/embed/845187a43cac49c09eda06f51443f8c7" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>