---
theme: academic
favicon: https://static-alex-eble.mo.cloudinary.net/logo.png
fonts:
  sans: 'Roboto'
  weights: '200,300,400,500,600,700'
highlighter: prism
info: |
  <h2>Git's Most Wanted</h2>
  <h5 class="font-light">Alexander Eble</h5>

  <a href="https://www.alex-eble.de" target="_blank" rel="noreferrer"><img alt="Alexander Eble Logo" class="w-48px" src="https://static-alex-eble.mo.cloudinary.net/logo.png" /><a/>

  <a href="https://www.alex-eble.de" target="_blank" noreferrer>https://www.alex-eble.de</a>

  The presentation is licensed under <a href="https://creativecommons.org/licenses/by-nc-sa/4.0/" target="_blank" noreferrer>CC BY-NC-SA</a>.
title: Alexander Eble • Git's Most Wanted
author: Alexander Eble
authorUrl: https://www.alex-eble.de
backgroundUrl: https://images.unsplash.com/photo-1556075798-4825dfaaf498?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1176&q=80
class: text-white
backgroundSource: unsplash
backgroundSourceUrl: https://images.unsplash.com/photo-1556075798-4825dfaaf498?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1176&q=80
date: 03/11/2022
hideInToc: true
---

# Git's Most Wanted <mdi-git />

## Git Commands Needed in the Everyday Workflow

---
hideInToc: true
---

# Target Group

Developers who..

- just started with Git and need a curated source of what is most important.
- who are already familiar with Git but need a refresher.
- who are already familiar with Git GUIs but intend to switch to the CLI.

---
class: "text-center"
layout: center
hideInToc: true
preload: false
---

# Prerequisites

<ul class="flex !list-none">
  <li>
    <a class="font-light" href="https://git-scm.com/book/en/v2/Getting-Started-Installing-Git" rel="noreferrer" target="_blank">Git <mdi-git /></a>
  </li>
  <li>
    <a class="font-light" href="https://en.wikipedia.org/wiki/Command-line_interface#Operating_system_command-line_interfaces" rel="noreferrer" target="_blank">OS CLI <mdi-bash />
    </a>
  </li>
</ul>

<div class="absolute top-18 right-10 w-260px" v-click>
  <img alt="Linus Tovalds" class="mb-4 rounded-sm" src="https://grupobcc.com/wp/wp-content/uploads/2015/05/Linus-Torvald-speaker-keynote-linus-conferencias.jpg" />
  <span class="font-light">..and Linus Tovald's blessing<sup>1</sup></span>
</div>

<Footnotes v-after separator>
  <Footnote :number=1><a href="https://grupobcc.com/wp/wp-content/uploads/2015/05/Linus-Torvald-speaker-keynote-linus-conferencias.jpg" target="_blank" rel="noreferrer">BBC International</a></Footnote>
</Footnotes>

---
hideInToc: true
layout: table-of-contents
class: text-xs
---

---

# `git init`

Create an empty Git repository or reinitialize an existing one<sup>1</sup>

```bash
git init
```

<Footnotes separator>
  <Footnote :number=1><a href="https://git-scm.com/docs/git-init" target="_blank" rel="noreferrer">Git. git-init</a></Footnote>
</Footnotes>

---

# `git status`

Show the working tree status<sup>1</sup>

```bash
git status

git status --ignored
```

<Footnotes separator>
  <Footnote :number=1><a href="https://git-scm.com/docs/git-status" target="_blank" rel="noreferrer">Git. git-status</a></Footnote>
</Footnotes>

---

# `git add`

Add file contents to the index<sup>1</sup>

```bash {all|1-3|5}
git add [<pathspec>...]

git add -A

git add -p [<pathspec>...]
```

<Footnotes separator>
  <Footnote :number=1><a href="https://git-scm.com/docs/git-add" target="_blank" rel="noreferrer">Git. git-add</a></Footnote>
</Footnotes>

---

# `git diff`

Show changes between commits, commit and working tree, etc<sup>1</sup>

```bash {all|1-3|5}
git diff [<pathspec>...]

git diff --staged [<pathspec>...]

git diff [<remote>]/<branch>
```

<Footnotes separator>
  <Footnote :number=1><a href="https://git-scm.com/docs/git-diff" target="_blank" rel="noreferrer">Git. git-diff</a></Footnote>
</Footnotes>

---

# `git restore`

Restore working tree files<sup>1</sup>

```bash
git restore [<pathspec>...]

git restore --staged [<pathspec>...]
```

<Footnotes separator>
  <Footnote :number=1><a href="https://git-scm.com/docs/git-restore" target="_blank" rel="noreferrer">Git. git-restore</a></Footnote>
</Footnotes>

---

# `git commit`

Record changes to the repository<sup>1</sup>

```bash {all|1-5|7|9}
git commit [<pathspec>...]

git commit -a [<pathspec>...]

git commit -m <msg> [<pathspec>...]

git commit --amend -m <newmsg> [<pathspec>...]

git commit --no-edit [<pathspec>...]
```

<Footnotes separator>
  <Footnote :number=1><a href="https://git-scm.com/docs/git-commit" target="_blank" rel="noreferrer">Git. git-commit</a></Footnote>
</Footnotes>

---

# `git config`

Get and set repository or global options<sup>1</sup>

```bash {all|1-3|5}
git config <name> <value>

git config --global <name> <value>

git config --list
```

<Footnotes separator>
  <Footnote :number=1><a href="https://git-scm.com/docs/git-config" target="_blank" rel="noreferrer">Git. git-config</a></Footnote>
</Footnotes>

---

# `git log`

Get and set repository or global options<sup>1</sup>

```bash {all|1-3|5}
git log

git log --oneline

git log -x
```

<Footnotes separator>
  <Footnote :number=1><a href="https://git-scm.com/docs/git-log" target="_blank" rel="noreferrer">Git. git-log</a></Footnote>
</Footnotes>

---

# `git show`

Show various types of objects<sup>1</sup>

```bash
git show [<object>…​]
```

<Footnotes separator>
  <Footnote :number=1><a href="https://git-scm.com/docs/git-show" target="_blank" rel="noreferrer">Git. git-show</a></Footnote>
</Footnotes>

---

# `git reset`

Reset current HEAD to the specified state<sup>1</sup>

```bash {all|1|3}
git reset HEAD~x

git reset --hard <remote>/<branch>
```

<Footnotes separator>
  <Footnote :number=1><a href="https://git-scm.com/docs/git-reset" target="_blank" rel="noreferrer">Git. git-reset</a></Footnote>
</Footnotes>

---

# `git remote`

Manage set of tracked repositories<sup>1</sup>

```bash {all|1|3|5}
git remote add <name> <URL>

git remote set-url <name> <newurl>

git remote -v
```

<Footnotes separator>
  <Footnote :number=1><a href="https://git-scm.com/docs/git-remote" target="_blank" rel="noreferrer">Git. git-remote</a></Footnote>
</Footnotes>

---

# `git push`

Update remote refs along with associated objects<sup>1</sup>

```bash {all|1|3|5}
git push

git push -u <remote> <branch>

git push -d <remote> <branch>
```

<Footnotes separator>
  <Footnote :number=1><a href="https://git-scm.com/docs/git-push" target="_blank" rel="noreferrer">Git. git-push</a></Footnote>
</Footnotes>

---

# `git fetch`

Download objects and refs from another repository<sup>1</sup>

```bash
git fetch

git fetch --all
```

<Footnotes separator>
  <Footnote :number=1><a href="https://git-scm.com/docs/git-fetch" target="_blank" rel="noreferrer">Git. git-fetch</a></Footnote>
</Footnotes>

---

# `git pull`

Fetch from and integrate with another repository or a local branch<sup>1</sup>

```bash {all|1|3-5}
git pull

git config pull.rebase <true | false>

git config pull.ff <false | only>
```

<Footnotes separator>
  <Footnote :number=1><a href="https://git-scm.com/docs/git-pull" target="_blank" rel="noreferrer">Git. git-pull</a></Footnote>
</Footnotes>

---

# `git branch`

List, create, or delete branches<sup>1</sup>

```bash {all|1|3|5-7|9}
git branch

git branch <name>

git branch -v

git branch -a

git branch -D <name>
```

<Footnotes separator>
  <Footnote :number=1><a href="https://git-scm.com/docs/git-branch" target="_blank" rel="noreferrer">Git. git-branch</a></Footnote>
</Footnotes>

---

# `git checkout`

Switch branches or restore working tree files<sup>1</sup>

```bash
git checkout <branch>

git checkout -b <branch>
```

<Footnotes separator>
  <Footnote :number=1><a href="https://git-scm.com/docs/git-checkout" target="_blank" rel="noreferrer">Git. git-checkout</a></Footnote>
</Footnotes>

---

# `git stash`

Stash the changes in a dirty working directory away<sup>1</sup>

```bash {all|1-3|5-7|9|11}
git stash

git stash push <pathspec>

git stash show

git stash show -v

git stash pop

git stash drop
```

<Footnotes separator>
  <Footnote :number=1><a href="https://git-scm.com/docs/git-stash" target="_blank" rel="noreferrer">Git. git-stash</a></Footnote>
</Footnotes>

---

# `git clean`

Remove untracked files from the working tree<sup>1</sup>

```bash
git clean -f

git clean -d
```

<Footnotes separator>
  <Footnote :number=1><a href="https://git-scm.com/docs/git-clean" target="_blank" rel="noreferrer">Git. git-clean</a></Footnote>
</Footnotes>
