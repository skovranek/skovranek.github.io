## [Portfolio](https://skovranek.github.io/) | [Education](https://skovranek.github.io/me/education.html) | [Experience](https://skovranek.github.io/me/experience) | [Blog](https://skovranek.github.io/blog)

### By: Matt Skovranek 06-08-2026

# Git's Insane Defaults

This is disgusting:

```
fatal: The upstream branch of your current branch does not match
the name of your current branch.  To push to the upstream branch
on the remote, use

    git push origin HEAD:main

To push to the branch of the same name on the remote, use

    git push origin HEAD

To choose either option permanently, see push.default in 'git help config'.

To avoid automatically configuring an upstream branch when its name
won't match the local branch, see option 'simple' of branch.autoSetupMerge
in 'git help config'.
```

Maybe you've seen this? It's git's ugly warning message because they would rather annoy you than let you push to master by mistake. That's probably a good thing, but I'd rather not be given a footgun in the first place.

Let's fix it! Here's my workflow 99% of the time (and how one would assume git works out-of-the-box):

1. When I start a new branch, I don't want to push to the starting branch, ie: `main`.
2. I want to push to a remote branch that's the same name as the new branch so it's obvious they are linked (and because I namespace my branches for safety).
3. If the remote branch doesn't exist, I want git to just create it automatically.
4. Also, when I pull from a remote branch, I want to rebase instead of merge for a clean git history.

How to configure that:

```bash
git config --global branch.autoSetupMerge simple
git config --global push.default current
git config --global push.autoSetupRemote true
git config --global pull.rebase true
```

Now you won't see this anymore when you create a new branch.

```
branch 'new_branch_name' set up to track 'origin/main'.
```
