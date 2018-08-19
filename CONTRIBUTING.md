# Fortnite Battle Royale subreddit theme contribution

This file will give you guidelines on how to contribute if you want to, and will list known contributors to this repo.

If you're not into software development or design in any way, you can still help by pointing out [issues](https://github.com/fortnite-subreddit/BattleRoyaleTheme/issues) or sharing your ideas with us.

## Workflow

### Branches & issues

If you want to work on an issue, make sure you create a specific branch for this issue using the format `issue_number-solution_explanation`. Examples are:

If issue #64 is `The subscribe button is not easy enough to see`, the branch to fix it should be something like: `64-change-subscribe-button-color-to-green` or `64-improve-subscribe-button-visibility`. Note that it should always start with a verb conjugated in the infinitive form, and describe what the commits's effects will be on the codebase. One branch should only be for one change. If your branch fixes multiple things, you're doing it wrong.

**Always make sure you're not working on the same issue as someone else, by asking on the issue thread to be assigned to it.**

### Commit names

The name of the commits should always be `#[issue number] [effect of the issue]` (ex: `#343 Remove unused icons`).

When working on your local branch, you can do as many commits as you want, obviously. The most important is that you **squash** your commits before creating your pull request, or at least before it is merged.

In case you're not familiar with squashing, here is a simple way to do it :

+ `git fetch origin` will make sure that you have a local version of the origin repository that is up to date (will not overwrite anything on your branch, no worries)
+ Then run `git rebase -i origin/master`
+ This will open a file letting you decide what to do with the commits. You want to keep the first `pick` and write `s` instead of `pick` for all other commits below, s meaning squash.
+ If there are conflicts, you will fix them step by step by following what git tells you, it's pretty straight-forward.
+ If there are no conflicts or if they are resolved, git will let you edit the commit names. Don't forget to comment the commit names of the commits you squashed by adding a `#` character in front of the commit message, and make sure that the commit message you left follows the aforementioned guidelines.
+ Now run `git log`, you should see only one commit by the name you chose during the rebase.
+ You can now `git push -f` if you already pused your branch on origin or simply push without the `-f` if it's your first push on origin. The reason for the `-f` is that when you squash your commits, you create a new one that will conflict with the state of your branch on origin. If you pull, it will overwrite your local state, so don't do that except if you messed up your rebase.

### Pull Requests

When creating your pull request, make sure to write in its description what issue it fixes. GitHub will intepret it and automatically close the issue once your pull request is closed. Just write `Fixes #IssueNumber` in the description.

When your pull request is created, GitHub will first check for conflicts and then your code will be reviewed by the maintainers of this repository.

If GitHub reports conflicts with the develop branch, you should resolve them by yourself using your git command-line interface. The easiest and cleanest way is to use `git rebase -i origin/master` and follow git's instructions.
If we report issues with your code, you should resolve them and then ping the person that reported them to notify them that you did the requested changes.

Once everything is in order, we will merge your pull request.

### Coding guidelines

WIP

## Contributors

WIP