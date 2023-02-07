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
  subgraph Student
    direction LR
    work["completed\nassignment"]
  end
  subgraph Instructor
    direction LR
    open["open\nassignment"]
    turn_in["review\nassignment"]
  end
  open --> |works towards| work
  work --> |seeks review| turn_in
  open -.-> turn_in
```

_An example instructor and student assignment workflow._

[Git branching](https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging) practices may be simpler to understand in context with similar workflows from real life. Consider a scenario within an educational course where an assignment is administered. The steps might look like the following:

```markdown
# Course Assignment Workflow
1. An instructor opens an assignment for students to complete
2. A student completes the assignment
3. The student turns in their completed assignment for review or grading.
```

This workflow can help provide context with how branching may work within git. The diagram below shows a "student" branch based off of the "main" branch's "opened" commit. After the "completed" commit takes place on the student branch, a merge is performed to pull the changes into the "main" branch.

```mermaid
    gitGraph
       commit id: "..."
       commit id: "opened"
       branch student
       checkout student
       commit id: "completed"
       checkout main
       merge student id: "reviewed" tag: "Seeks review"
       commit id: ".." 
```

_An example git diagram showing student branch being merged with main after review._

## Branching

## Reviewing

## Merging

## Resources

Please see the following the resources on this topic.

- [Atlassian: Git Branch](https://www.atlassian.com/git/tutorials/using-branches)
