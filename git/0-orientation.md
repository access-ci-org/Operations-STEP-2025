# Git Workshop: Orientation

![XKCD comic about git](media/xkcd-1597.png)

([XKCD #1597](https://xkcd.com/1597/))

---

## Agenda

### Morning Session

| Duration | Module                               |
|----------|--------------------------------------|
| 20m      | context and orientation              |
| 30m      | creating and cloning a git repo      |
| 10m      | recording changes                    |

### Afternoon Session

| Duration | Module                               |
|----------|--------------------------------------|
| 20m      | recording changes (continued)        |
| 20m      | studying history                     |
| 50m      | working with servers                 |
| 30m      | break                                |
| 20m      | contributing to a software project   |
| 20m      | next steps, bonus material, Q&A      |


<!--
Times are squishy, we can adjust as it suits the group.

Anyone can browse to this repo to see the presentation materials. If you look at the Markdown source (raw code view), you can see my speaker notes.

Who here has ever worked on a programming project? On your own or for school?
Who here knows what Git does? Not GitHub, just Git.

Who here has used Git? If you have, keep your hand up. If your hand is up, look around the room. Are there any tables with no hands raised?

If so, move closer to that table, so that the folks who have never used Git are near someone who has.
-->

---

## Why We Need Version Control

**version control : software :: medical records : healthcare**

It's irresponsible to practice medicine with no record-keeping.

- This patient is taking 'dangerous medication', when was their last dose? 
- This bug surfaced in production last Thursday, what code changes happened then?

<!--
A patient chart answers the first question, a Git repository answers the second.

The terms "version control" and "revision control" mean approximately the same thing, I'll use them interchangeably.
-->

---

Imagine the world's simplest software project, in a directory (folder) on your computer. There are just two files: a Python script and a readme file.

```
cmart@thinkpad:~$ tree my-project
my-project
├── code.py
└── readme.md
```

<!--
The `tree` command draws the contents of a folder as a visual tree structure. We'll use it a lot today.
-->

---

Imagine that you work on your project with a friend for a week. Your two files have turned into this:

```
cmart@thinkpad:~$ tree my-project
my-project
├── code-2023-May-09.py
├── code-2023-May-09-backup-v2.py
├── code-nathan-changes.py
├── code.py
├── code-v2-final.py
├── code-v2-FINAL.py
├── code-v2-final-actually-working.py
├── code-v3.py
├── code.😵‍💫
├── readme-first.md
└── readme.md
```

<!--
Has anyone ever worked on a project like this? Especially a group project with multiple authors?

If you're seeing this project for the first time, how do you know which file to open?
-->

---

Now imagine your little project growing over a few years:

- 177 source code files
- 37,000 lines of code
- 25+ community contributors
- Thousands of hours of work
- Production system with 2000 users

<!--
this actually happened to me
-->

There will be chaos! Git helps you manage the chaos.

---

Very common tasks on a software team:

1. **Exploring changes** on your own, then **submitting them** to the main project
2. **Reviewing other people's work**
- "What exact change is this internet stranger proposing?"
- "Do I want to accept it?"
3. **Troubleshooting**
- "Which code change introduced this problem?"
- "Why did we do this like that?"
4. **Conflict resolution**
- I changed function `increment_record()` to `increment_inner_record()`, but around the same time, you added a new argument to that function.
- How can we combine both of our changes in a way that works and makes sense?

Git helps us do all of these.

---

## What Does Git Do?

Git provides a way to _track changes to a directory of files_.

- Over time and space
- With multiple authors changing the same files
- With meaningful annotations of change sets
- With different branches of history that can diverge and converge
- Helps you avoid, notice, and resolve conflicting changes
- Guarantees you will notice corruption of (or tampering with) history

---

## Concretely, What _is_ Git?

Git is command-line software. Using it looks like this.

```shell
$ git init
Initialized empty Git repository in /home/cmart/my-project/.git/
$ touch code.py
$ git add code.py
$ git commit -m "first commit!"
[master (root-commit) e62062f] first commit!
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 code.py
```

**Vocabulary:** a *repository* (or *repo*, for short) is a project tracked by Git. A repo includes the complete history of changes to each file.

<!--
Here I'm initializing a new repo, adding a file to my staging area, and making a commit.
-->

---

## I'm new to Git, but is there something similar I might have used?

Probably not, but:

- "Track changes" in word processor
- History and versioning in (e.g.) Google Docs
- Filesystem-level tools
    - Time Machine (Mac OS)
    - Shadow copies (Windows)

These record changes in the background. Using Git requires explicitly scoping and annotating changes.

<!--
These record changes in the background while you build content. You don't have to think about them until you need to look at what has changed.

Git is kind of like storytelling.
-->


---

## Climbing the Skills Ladder

- On the ground: "What is Git?"
- Rung 1: Knowing a few Git commands
    - You after this workshop
- Rung 2: Having little projects on GitHub
    - Good commit scope and messages
- Rung 3: Working on a development team
    - Multiple remotes, interactive rebase, resolving merge conflicts
    - Understanding Git's _directed acyclic graph_ data model
- Rung 4: Maintaining a software project with many contributors
    - Building ecosystem of git-based workflows, tutoring others
- ...
- Top of ladder: Linus Torvalds
    - You created Git to manage the world's largest software project
    
<https://exosphere.app/docs/contributor-skills/#on-git-skills>

<!--
There is real computer science behind Git's data model!

This workshop is the briefest introduction. You will leave knowing barely enough to be dangerous. You will git stuck, this is normal.
-->

---

## Git for Text and Docs

Git not only works for source code, but also:

- Documentation
  - Markdown
  - LaTeX manuscripts
  - mkdocs, Read The Docs
- Configuration files
- Data science (i.e. Jupyter) notebooks
- Anything that looks like plain text!

<!--
This workshop is written entirely in Markdown and tracked in Git. (show source)

Learn to love plaintext and Markdown. You may die inside a little when someone wants to collaborate using a Google Doc.
-->

---

## Ecosystem of Git-based Workflows

- Pull/merge requests
- Continuous integration (CI) and deployment (CD)
- DevOps
- Website and documentation publishing

---

## Git != GitHub

Git is not GitHub.

GitHub is Git plus many other services.

- Git is a free and open-source revision control system.
- GitHub(.com) is a proprietary service built around Git.
  - Repository hosting
  - Access control
  - Collaboration features (issues, wiki)
  - Code review (pull requests)
  - Etc.

<!--
We can hold hands and say it together.

Git is open-source (GPL) software, trademark owned by the Software Freedom Conservancy, developed by Linux Kernel developers.

GitHub is owned by Microsoft. There are also several alternatives to GitHub.

This workshop focuses mostly on Git, we use GitHub a little bit near the end.
-->