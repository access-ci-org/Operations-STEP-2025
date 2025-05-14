# Git Workshop: Creating and Cloning a Repository

## Open a Unix Shell

Git setup instructions, if you haven't already:

> _An iOS or Android device won't work. They need to use a Windows, Mac, or Linux computer._
>
>  1. Follow these directions <https://github.com/git-guides/install-git> to install git. Students don't need to install "GitHub Desktop", just git.
> 2. Confirm that each student can open a command prompt (a.k.a. terminal or shell) and run `git version`.
> 3. Create an account on <https://github.com> if student doesn't have one already

If this doesn't work on your own computer, connect to the Jetstream2 instance.

## Exercise: Basic Shell Function

- Enter `pwd` to show the working directory
- Enter `mkdir step` to create a directory named step
- Enter `cd step` to change your working directory to `step`
- Text editor (e.g. `nano`)
  - Quit `nano` with `Ctrl + X` (then `y` or `n` if prompted)
- Copying and pasting text to/from your terminal
  - Mac:
    - `⌘ + C` to copy
    - `⌘ + V` to paste
  - Windows:
    - `Ctrl + C` to copy
    - `Ctrl + V` to paste
  - Linux:
    - `Ctrl + Shift + C` to copy
    - `Ctrl + Shift + V` to paste
  - Web Shell to Jetstream2 instance: depends on operating system and browser

<!--
Let's take a minute to review these if anyone is unsure about them.
-->

## Exercise: Ensure Git is Installed

Tip: do not type the `$`. (`$` is the prompt, type what comes after it.)

```shell
$ git help
```

<!--
The `$` is the prompt, some of my examples will show output

(`help` accepts subcommands, e.g. `git clone --help`, but shows LOTS of detail)
-->

---

## Exercise: Create a New Project From Scratch

```shell
$ mkdir your-project
$ cd your-project
$ git init
$ git status
```

---

## Exercise: Clone Someone's Existing Project

Perhaps you found something on GitHub, you want to use it or contribute to it.

```shell
$ cd
$ git clone https://github.com/access-ci-org/Operations_STEP_2025.git
$ cd Operations_STEP_2024
$ git status
```

**Vocabulary:** to _clone_ a Git repo means to download a copy from the internet.

---

## Exercise: Where is the Git Magic Stored?

Run this from the _root_ directory of a repo:

```shell
$ ls -a
```

`.git` directory contains all the metadata related to the history of the repo.

<!--
If you delete it, your directory ceases to be a Git repository!
-->