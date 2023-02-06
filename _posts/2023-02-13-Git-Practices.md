---
title: "Tip of the Week: Git Practices"
author: Dave Bunten
member: dave-bunten
tags:
  - tip-of-the-week
  - software

---

# Tip of the Week: Git Practices

> Each week we seek to provide a software tip of the week geared towards helping you achieve your software goals. Views expressed in the content belong to the content creators and not the organization, its affiliates, or employees. If you have any software questions or suggestions for an upcoming tip of the week, please don’t hesitate to reach out to #software-engineering on Slack or email DBMISoftwareEngineering at olucdenver.onmicrosoft.com

__TLDR (too long, didn't read);__

## Setting the Scene

```mermaid
flowchart LR
  subgraph student
    direction LR
    work["completed\nassignment"]
  end
  subgraph instructor
    direction LR
    open["open\nassignment"]
    turn_in["review\nassignment"]
  end
  open --> |works towards| work
  work --> |seeks review| turn_in
  open -.-> turn_in
```

_An example instructor and student assignment workflow._

```mermaid
    gitGraph
       commit id: "created"
       commit id: "opened"
       branch student
       checkout student
       commit id: "completed"
       checkout main
       merge student id: "reviewed" tag: "Seeks review"
       commit id: "..." 
```

_An example git diagram showing student branch being merged with main after review._

## Branching

## Reviewing

## Merging

## Resources

Please see the following the resources on this topic.
