---
title: "Med Cabinet"
date: "2020-02-28"
template: "project"
draft: false
slug: "med-cabinet"
category: "Natural Language Processing"
tags:
  - "natural language processing" 
  - "flask"
  - "heroku"
description: "App for new cannabis consumers (especially those trying to get off of pharmaceuticals) who want to use cannabis as a means to battle medical conditions and ailments."
socialImage: "/media/image-0.jpg"
---
[![Alt text](/media/icons/GitHub-Mark-32px.png)](https://github.com/andronikmk/med-cabinet-data-science)


## Introduction

<p style="text-align: justify;"> 
Med Cabinet is an application for new cannabis consumers who want to use cannabis as a means to battle medical conditions
and ailments. In addition, Med Cabinet helps patients find the right strain, dosing, intake methods and scheduale.
This application is built using Flask, along with a PostgreSQL database hosted database. The API is deployed to Heroku at which
point a front-end team is tasked to build a user interface. This is a cross functional project during which my team was tasked
to build a Flask app and PostgreSQL database. An additional data science team was responisble to the model used for this app as
well as choosing the metrics to measure our models success.  
</p>

## Model and Metric

<p style="text-align: justify;"> 
Our model leverages k-Nearest Neibors assuming TF-IDF vectorization and achieves a 
validation accuracy of 73.2%. In addition, on this project my team was tasked
to intergrate the model into our Flask app, host the data using PostgreSQL and
deploy the API to Heroku, at which point the Front End team would connect to
the endpoint. Finally, model output is in the form of a Json object using the following
categories:
</p>

+ id
+ name
+ strain
+ flavors
+ negative
+ positve
+ medical
+ rating
+ description

## Presentation

+ [Med Cabinet App Demo](https://med-cab-app.herokuapp.com/)

<img src="/media/med-cabinet/img1.png" alt="Front-end 1">
<img src="/media/med-cabinet/img2.png" alt="Front-end 2">
<img src="/media/med-cabinet/img3.png" alt="Output">