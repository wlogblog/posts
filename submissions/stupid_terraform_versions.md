---
title: "stupid terraform versions"
date: 2023-08-05T20:51:50+10:00
draft: false
ShowReadingTime: true
ShowShareButtons: false
ShowBreadCrumbs: true
tags:
  - terraform
  - infra
  - iac
editPost:
    URL: "https://github.com/wlogblog/posts/tree/main/submissions/" 
    Text: "suggest changes"
    appendFilePath: true
author: "@the.editor"  # put your own github handle for PRs, or put @anon if you want to remain anonymous
# author_external_url : "https://github.com/wlogblog/"
---

## You know when's the most annoying time to see a terraform version error?

When you are trying to `terraform import` a bunch of orphaned resources that didn't successfully delete during [CRUD](https://en.wikipedia.org/wiki/Create,_read,_update_and_delete) cause of a bug in a custom module.

```bash
Error: Error loading state:
    Remote workspace Terraform version "1.4.6" does not match local Terraform version...
```
...


SREs are probably laughing at us for not using `direnv`; but hey, why do I even need to worry about matching versions when I'm using `remote` workspace mode with Terraform Cloud? Don't have to match versions with `apply` and `plan`...

## anways, here's the quick fix.

- *If you want version `1.4.6`*
```bash
brew uninstall terraform # I assume you are civilised
brew install tfenv
tfenv install 1.4.6
tfenv use 1.4.6
terraform --version # trust but validate
```

- *If you want to switch to another verison*
```bash
tfenv install 1.5.4
tfenv use 1.5.4
terraform --version
```

- *If you are an over-achiever*
  - spend the time to set up [direnv](https://github.com/direnv/direnv) like the SREs told you
  - or try the [tips in this stackoverflow thread](https://stackoverflow.com/questions/56283424/upgrade-terraform-to-specific-version)
