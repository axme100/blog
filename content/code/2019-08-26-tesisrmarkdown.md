---
title: tesisRMarkdown
author: ''
date: '2019-08-26'
slug: tesisrmarkdown
categories: []
tags: []
description: ''
topics: []
---

Actually it's looking like the best way to go is use weave:

We want to use biber in order to have the apa style of biblatex: So I have to compile the document with the following command.

https://kevinstadler.github.io/blog/knitr-rmarkdown-flavours/

knitr::knit2pdf('testsweave.Rnw', bib_engine = "biber")


Resources:
https://bookdown.org/yihui/rmarkdown/pdf-document.html
It looks like this page talks about overall document structure

## 1. Compiler

**pdflatex** (maybe xelatex)

- It looks like the default for overleaf and for R studio is pdfLaTex but XeLaTex can also be used for both. Xelatex may be better for certain unicode fonts, but I'll probably want to stick with the default, and just change the language to Spanish.

## 2. Citation package manager

**Biblatex**

- Looks like it can be used for Spanish quite well, see the code in this answer
- for the code that would need to be in the latex preamble (remember YAML hearders can also contain certain options options)
https://tex.stackexchange.com/a/321975/151573

- Better than apacite for Spanish:

> Since this is for a thesis (and the apacite package is not being required by a particular journal) you might also consider using biblatex and the biblatex-apa package, which is a very up-to-date implementation of the APA 6th edition. There are plenty of examples of its use on the site. (https://tex.stackexchange.com/a/37046/151573)


3. Develop a document structure that uses child commands to bring in the three chapters.

# 
https://tysonbarrett.com/jekyll/update/2018/02/11/r_dissertation



## 1. https://bookdown.org/yihui/rmarkdown/pdf-document.html



/

PhD doesn't 







https://community.rstudio.com/t/what-are-your-recommendations-for-thesis-writing-with-rstudio-and-rmarkdown/13576/4?u=axme100

- Talks about kniting to latex code then editing that code

- Or embedding raw latex code into your rmarkdown document.