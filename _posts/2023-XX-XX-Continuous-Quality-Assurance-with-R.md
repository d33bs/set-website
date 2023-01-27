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

Linting, or [static analysis](https://en.wikipedia.org/wiki/Static_program_analysis), is one way to ensure a minimum level of code quality without writing new tests. Linting checks how your code is structured without running it to make sure it abides common language paradigms and logical structures. Using linting tools allows a developer to gain quick insights about their code before it is viewed or used by others.

One way to lint your R code is by using the [`lintr`](https://github.com/r-lib/lintr) package. The `lintr` package is also complementary of the [`styler`](https://github.com/r-lib/styler) pacakge, which formats the syntax of R code in a consistent way. Both of these can be used independently or as part of continuous quality checks for R code repositories.

## Automated Linting Checks

`lintr` and `styler` can be incorporated into automated checks to help make sure linting (or other steps) are always used with new code. One tool which can help with this is [pre-commit](https://pre-commit.com/), which acts as both a local development tool in addition to providing observability within source control (more on this later).

Using pre-commit locally enables quick feedback loops using one or many checkers (such as `lintr`, `styler` or others). Pre-commit may be used through the use of [git hooks](https://pre-commit.com/#usage) or manually using [`pre-commit run ...`](https://pre-commit.com/#pre-commit-run) from a command-line. See [this example of pre-commit checks with R](https://github.com/lorenzwalthert/precommit) for an example of multiple pre-commit checks for R code.

## Continuous and Observable Checks

Pre-commit linting checks can also be incorporated into continuous checks performed on your repository. One way to do this is using [Github Actions](https://docs.github.com/en/actions). Github Actions provides a programmatic way to specify automatic steps taken as changes occur to a repository.

Pre-commit provides [an example Github Action](https://github.com/pre-commit/action) which will automatically check and alert repository maintainers when code challenges are detected. Using pre-commit in this way allows R developers to ensure `lintr` checks are performed on any new work checked into a repository. This can have benefits towards decreasing pull request (PR) review time and standardize how code collaboration takes place for R developers.

## Resources

Please see the following the resources on this topic.

-
