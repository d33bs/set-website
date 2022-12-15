---
title: "Tip of the Week: Linting Documentation as Code"
author: Dave Bunten
member: dave-bunten
tags:
  - tip-of-the-week
  - software
  - documentation
  - docsascode
  - linting
  - staticanalysis
---

# Tip of the Week: Linting Documentation as Code

> Each week we seek to provide a software tip of the week geared towards helping you achieve your software goals. If you have any software questions or suggestions for an upcoming tip of the week, please don’t hesitate to reach out to #software-engineering on Slack or email DBMISoftwareEngineering at olucdenver.onmicrosoft.com

[Software documentation](https://en.wikipedia.org/wiki/Software_documentation) is sometimes treated as a less important or secondary aspect of software development. Treating documentation as code allows developers to version control the shared understanding and knowledge surrounding a project. Leveraging this paradigm also enables the use of tools and patterns which have been used to strengthen code maintenance. This article covers one such pattern: [linting](https://en.wikipedia.org/wiki/Lint_(software)), or static analysis, for documentation treated like code.

__TLDR (too long, didn't read);__
There are many linting tools available which enable quick revision of your documentation. Try using [codespell](https://github.com/codespell-project/codespell) for spelling corrections, [mdformat](https://github.com/executablebooks/mdformat) for markdown file formatting corrections, and [vale](https://vale.sh/) for more complex editorial style or natural language assessment within your documentation.

## Spelling Checks

```markdown
<!--- readme.md --->
## Example Readme

Thsi project is a wokr in progess.

(CU Anschutz)[https://www.cuanschutz.edu/]
```

_Example readme.md with incorrectly spelled words_

```sh
% codespell readme.md
readme.md:4: Thsi ==> This
readme.md:4: wokr ==> work
readme.md:4: progess ==> progress


```

_Example showing codespell detection of mispelled words_

[Spelling checks](https://en.wikipedia.org/wiki/Spell_checker) may be used to automatically detect incorrect spellings of words within your documentation (and code!). [Codespell](https://github.com/codespell-project/codespell) is one library which can lint your word spelling. Codespell may be used through the command-line and also through a [pre-commit](https://pre-commit.com/index.html) hook.

- [codespell](https://github.com/codespell-project/codespell)

## Markdown Format Linting

```markdown
<!--- readme.md --->
## Example Readme

This project is a work in progress.

(CU Anschutz)[https://www.cuanschutz.edu/]
```

_Example readme.md with markdown issues_

```sh
% markdownlint readme.md
readme.md:2 MD041/first-line-heading/first-line-h1 First line in a file should be a top-level heading [Context: "## Example Readme"]
readme.md:6:5 MD011/no-reversed-links Reversed link syntax [(link)[https://www.cuanschutz.edu/]]



```

_Example showing markdownlint detection of issues_

- [markdownlint](https://github.com/markdownlint/markdownlint)

Additional and similar resources to explore in this area:

- [restructuredtext-lint](https://github.com/twolfson/restructuredtext-lint)
- [mdformat](https://github.com/executablebooks/mdformat)

## Editorial Style and Natural Language

- [vale](https://vale.sh/)

Additional and similar  resources to explore in this area:

- [textlint](https://textlint.github.io/)

## Additional Resources

Please see the following the additional resources on this topic.

-
