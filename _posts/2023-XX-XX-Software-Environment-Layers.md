---
title: "Tip of the Week: Software Environment Layers"
author: Dave Bunten
member: dave-bunten
tags:
  - tip-of-the-week
  - software

---

# Tip of the Week: Software Environment Layers

> Each week we seek to provide a software tip of the week geared towards helping you achieve your software goals. If you have any software questions or suggestions for an upcoming tip of the week, please don’t hesitate to reach out to #software-engineering on Slack or email DBMISoftwareEngineering at olucdenver.onmicrosoft.com

Code needs a consistent way to be used by computers. The "places" where code runs are generally called environments. Software environments have various layers and specific tools intended to ensure your code can run where it's needed. This article is the first in a series intended to cover the layers of where your code lives.

__TLDR (too long, didn't read);__

## Why this matters

```console
IT'S DANGEROUS TO GO ALONE!
USE ENVIRONMENT MANAGEMENT TOOLS!
🔥 🧑‍💻 🔥
   🛠️
```

{:.center}

Software environment management is crucial because [software decay](https://en.wikipedia.org/wiki/Software_rot#Environment_change) may occur due to environmental change. If software is unable to be used due to the environment, it risks becoming meaningless to the audience. One way to think of this is as software shelter; code is unprotected and may fall victim to the elements without a home.

## Local Development Environment

<pre class="mermaid">
flowchart BT
    local["Local Development\nEnvironment"]
    style local fill:#9FE2A6,stroke:#aaa
</pre>
<script type="module">
  import mermaid from 'https://unpkg.com/mermaid@9/dist/mermaid.esm.min.mjs';
  mermaid.initialize({ startOnLoad: true });
</script>
{:.center}

The first layer our code typically lives in is the local development environment. This is where code is initially written and tested by the developer using a specific language and set of dependencies.

## Operating System Environment

<pre class="mermaid">
flowchart BT
    subgraph os [Operating System]
      local["Local Development\nEnvironment"]
    end
    style local fill:#fff,stroke:#aaa
    style os fill:#9FE2DE,stroke:#aaa
</pre>
{:.center}

## Inter-Systems Environment

<pre class="mermaid">
flowchart LR
    subgraph is [Inter-system]
    direction LR
      subgraph os [Operating System X]
        local["Local Development\nEnvironment X"]
      end
      subgraph os2 [Operating System Y]
        local2["Local Development\nEnvironment Y"]
      end
    end
    os <-.-> os2
    style local fill:#fff,stroke:#aaa
    style local2 fill:#fff,stroke:#aaa
    style os fill:#fff,stroke:#aaa
    style os2 fill:#fff,stroke:#aaa
    style is fill:#87B8ED,stroke:#aaa
</pre>
{:.center}

## Additional Resources

-
