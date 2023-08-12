---
title: "machine learning model code testing framework"
date: 2023-08-11T00:00:00+10:00
draft: true
keywords:
  - mlops
  - machine learning models
  - unit tests
  - integration tests
  - post-deployment tests
tags:
  - mlops
author: "@the.engineer"
# author_external_url : "https://github.com/wlogblog/"
robots: index,follow
---

One of the most important components to a successful ML project is to have a solid automated testing framework in the CI/CD pipeline. As the code base gets larger, more complex and with more contributors, it will become a crucial part of your code development process. Although it may take some time initially setting it up, it will allow you to spend less time fixing code bugs in the long run.

The key word here is 'code testing' which is aimed to test the code functionality. It's not model performance testing - this is a completely separate thing.

Three basic tests to have in a somewhat mature ML project are unit tests, integration tests and post-deployment tests.

## 1. Unit tests
Unit tests are designed to test individual components or functions/classes of the code base. It will test that the function accepts the same specified input and output and will run without breaking. Unit tests allows you to easily identify which component of the code will break if some code changes and if the change was intentional, it's just a matter of updating the unit test.

## 2. Integration tests
If unit tests are testing individual components of the code base, integration tests will test the components together. The idea is to set up logical components of the code to test together. For example, in a ML project, there may be data preparation, model training and model prediction tests.

Both unit tests and integration tests should be fast and done every code commit.

## 3. Post-deployment tests
Post-deployment tests will test the code base end-to-end and usually using the resources used in production. For example, if you model is run on the cloud, then using the cloud resources. This may be a bit too much to do every code commit and so you may choose to run this before a pull request to the main branch.


## Some challenges

With multiple contributors adding to the code base, it's important to have the correct environment setup. The reason for this is, the tests may run fine on your local development environment. You can commit the code to the repository and realise the tests fail in your CI/CD pipeline.

A great way to do this is to wrap everything in docker!






