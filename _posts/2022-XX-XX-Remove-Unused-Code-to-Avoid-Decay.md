---
title: "Tip of the Week: Remove Unused Code to Avoid Software Decay"
author: Dave Bunten
member: dave-bunten
tags:
  - tip-of-the-week
  - software
  - code-quality
  - software-decay
  - code-decay
  - dead-code
  - vulture
---

# Tip of the Week: Remove Unused Code to Avoid Software Decay

> Each week we seek to provide a software tip of the week geared towards helping you achieve your software goals. If you have any software questions or suggestions for an upcoming tip of the week, please don’t hesitate to reach out to #software-engineering on Slack or email DBMISoftwareEngineering at olucdenver.onmicrosoft.com

The act of creating software often involves many iterations of writing, personal collaborations, and testing. During this process it's common to lose awareness of code which is no longer used (and may not be tested or otherwise linted). Unused code may contribute to ["software decay"](https://en.wikipedia.org/wiki/Software_rot) (the gradual diminishment of functionality). This post will cover software decay and strategies for addressing unused code to help keep your code quality high.

__TLDR (too long, didn't read);__

## Additional Resources

- [Software Rot](https://en.wikipedia.org/wiki/Software_rot)
- [Vulture](https://github.com/jendrikseipp/vulture)
