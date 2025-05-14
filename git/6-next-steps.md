# Git Workshop: Next Steps, Bonus, Q&A

## Next Learning Steps

- Work through Software Carpentry Git lesson
  - <https://swcarpentry.github.io/git-novice>
  - Consider attending a Carpentry workshop
- Learn how branches and merging work
- _Pro Git_ free online book (though it is technical)
  - <https://git-scm.com/book>
- Learn about Git's data model, then everything else will make more sense
  - <https://maryrosecook.com/blog/post/git-from-the-inside-out>
- Ask a LLM to help you understand and use Git
  - (but fact-check its answers before relying on them)

<!--
When you understand the data model, concepts like branches and tags and merges are a lot less mysterious.

LLMs are great study assistants, as long as you don't trust them. and Git is very well-represented in their training sets.
-->

---

## Students choose: Q&A or Bonus Material?

## "I found this push-button Git app, it's so easy! No commands to run!"

Okay, but:

- Every graphical interface for git is feature-incomplete
- In your career, you _will_ encounter tricky situations that require using the Git command line
    - Working in remote servers
    - Interactive rebase
    - Submodules
    - Rescuing lost commits from the reflog
    - Automated (scripted) use of Git

If you avoid the CLI until you're in a pinch, you face the steepest learning curve at the worst possible time. If you build the CLI skills and habits now, you'll become a total pro, and your skills will transfer to other tools. 😎

---

## Alternatives to GitHub

Call to action: let's not put all our eggs in Microsoft's basket!

- Codeberg
  - <https://codeberg.org>
  - Built on open-source, self-hostable Forgejo software
- GitLab (proprietary with open-source core, self-hostable)
- Phabricator (open-source)
- Bitbucket (proprietary, Atlassian)

---

## Job Interview Advice

Ask about their use of revision control!

For a software or infrastructure engineering job:

- Standard correct answer
  - "Everyone here who works with code uses Git"
- Maybe run away
  - "We don't use a revision control system"
    - This is like a hospital with no rules for how they keep medical records
  - "We're in the process of adopting git"
    - Expect chaos in this workplace
  - "We use CVS / Subversion / Source Safe"
    - This workplace is trapped in 2005
- Weird / interesting
  - "We use Mercurial / Perforce"
    - Expect other niche tech choices too

---

## About the Presenter

Chris Martin (a.k.a. cmart), Systems Engineer at Indiana University, cm10@iu.edu

- "Informatics" undergrad at SUNY Buffalo (2010)
- 4 years working in Windows IT shops
  - First tech job: bigcorp desktop support
  - Ended up at consultancy leading infrastructure projects for SMBs
- Quit working to hike for a few months
  - Decided to build open-source software, focus on Linux ecosystem
- 1 year "under-employed" learning new skills and building projects
- 8 years at universities, building cloud systems and UI for OpenStack
  - <https://exosphere.app>
  - <https://jetstream-cloud.org>
  - <https://gitlab.com/jetstream-cloud>