---
title: "stop using chatGPT for coding"
date: 2023-08-07T21:24:30+10:00
draft: false
keywords:
  - generative AI
  - chatGPT
  - data engineering
  - stack overflow
  - GitHub CoPilot
tags:
  - AI
  - chatGPT
  - Stack Overflow
author: "@the.editor"
# author_external_url : "https://github.com/wlogblog/"
robots: index,follow
---

Do you ever ask chatGPT for help when debugging code or maybe even for designing functionality from scratch?

If you answered yes, you should go back to asking Google or StackOverflow.

A [new research paper published on 4.Aug.2023](https://arxiv.org/pdf/2308.02312.pdf) compared StackOverflow answers with ChatGPT answers for **software engineering questions** and found that:
> *52% of ChatGPT answers are incorrect and 77% are verbose*


## tl;dr of the paper's findings  :open_book:

The researchers attributed the incorrect ChatGPT errors with 3 overlapping themes:  

- `Conceptual`, it didn't understand the question, (54%)
- `Factual`, it made shit up, (36%)
- `Code` + `Terminology`, wrong syntax (40%)

The funny (and dangerous) thing is that although the answers are wrong, they are so well written that it's sometimes hard to tell they are wrong.

> *Users get tricked by appearance. Our user study results show that users prefer ChatGPT answers 34.82% of the time. However, 77.27% of these preferences are incorrect answers.*
> 
> ... *polite language, articulated and text-book style answers, comprehensiveness, and affiliation in answers make completely wrong answers seem correct.*

## maybe time to try [GitHub copilot](https://github.com/features/copilot)? :joy:
