---
toc: true
comments: true
layout: post
title: Tool Procedure for my Mac
description: This guide is specific to MacOS
courses: { compsci: {week: 0} }
type: hacks
---

## Hacks
> Complete the procedure below accurately.  These are absolutely required and must be 100% accurate for your success.

### GitHub Account
- Follow instruction [https://docs.github.com/en/get-started/signing-up-for-github/signing-up-for-a-new-github-account](https://docs.github.com/en/get-started/signing-up-for-github/signing-up-for-a-new-github-account)  Use your own personal/permanent email... NOT SCHOOL!!! GitHub account belongs to you.

### MacOS 1st Time Developer
> VSCode install
- Install [VSCode](https://code.visualstudio.com/docs/setup/mac)

> Anaconda install
- Download for MacOS: [Anaconda](https://www.anaconda.com/products/distribution)
- Run Install: Answer yes to questions

> Homebrew install
- Copy and Paste to Install from Terminal [Homebrew](https://brew.sh)
    - Copy ```bash ... curl ...```  command using copy box on website
    - Launch ```terminal``` from search bar
    - Paste ```bash ... curl ...``` command into Terminal ... 
    - Make sure command starts, this should provide feedback/output in terminal and could take a long time, like 10-min, there could be a  prompt in the middle, at about 5-minutes.  Follow any on screen instructions provided in terminal output to finish.
- Homebrew installs a tool called "brew" which helps add and manage developer packages on MacOS.

> At this point, the next task is to prepare tools.  <mark>You must start a new Terminal</mark>.  Now the Terminal prompt should be <mark>prefixed with (base)</mark>.  If not, you need to go back to Anaconda install.
- Open new Terminal, your prompt should look like this...
```bash
(base) iMac:~ jmort1021$
```

> Key Packages needed on MacOS
- <mark>Close and Start a new terminal</mark>, run each command in Terminal
```bash
$ brew list # list packages
$ brew update # update package list
$ brew upgrade # upgrade packages
$ brew install git  # install latest git
$ brew install python # install python3 for development
$ python --version # version of python3 installed
```