---
title: "Tip of the Week: Continuous Quality Assurance with R"
author: Dave Bunten
member: dave-bunten
tags:
  - tip-of-the-week
  - software
---

# Tip of the Week: Continuous Quality Assurance with R

> Each week we seek to provide a software tip of the week geared towards helping you achieve your software goals. If you have any software questions or suggestions for an upcoming tip of the week, please don’t hesitate to reach out to #software-engineering on Slack or email DBMISoftwareEngineering at olucdenver.onmicrosoft.com

__TLDR (too long, didn't read);__

## Linting with R

Linting, or [static analysis](https://en.wikipedia.org/wiki/Static_program_analysis), is one way to ensure a minimum level of code quality without writing new tests. Linting checks how your code is structured without running it to make sure it abides common language paradigms and logical structures. One way to lint your R code is by using the [lintr](https://github.com/r-lib/lintr) package.

## Automated Checks

Lintr can be incorporated into automated checks to help make sure linting (or other steps) are always used with new code. One tool which can help with this is [pre-commit](https://pre-commit.com/), which acts as both a local development tool in addition to providing observability within source control (more on this later). Using pre-commit locally

## Continuous and Observable Testing

## Resources

Please see the following the resources on this topic.

-
