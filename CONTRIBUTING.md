# How to contribute to this repository

All current work on the YiiBooster happens in the branches which are named like `N.N.N-wip`, where `N`s are numbers. So, you should not normally contribute to master branch, but only to current `*-wip` branch instead.

Common work process is as follows:

1.    **Fork YiiBooster** to your Github account.
      Use button "Fork" in the Github webpage, and follow instructions afterwards.

2.    **Add Clevertech's repo as an additional remote** to your fork.
      `git remote add ct git://github.com/clevertech/YiiBooster.git`
      Note that I named new remote as `ct` in this example. Remember it.

3.    **Pull latest `\*-wip` branch from Clevertech's repo**.
      `git pull ct`
      When you run just `git pull` you pull from the `origin` remote.
      This way you explicitly requires Git to pull from Clevertech's repository.

4.    **Make a new branch** named after the feature you're fixing/adding.
      `git checkout -b myfeature`
      Step 3 ensures you that you're branching from most latest `*-wip`, this will save you a lot of pain when you'll be pull-requesting.

5.    **Commit everything to this branch** and not to master.
      Easiest way is to run `git branch` before commit and look if the asterisk is before the name of your desired branch.

6.    After you've done with the feature under question, **open the `CHANGELOG.md` and append the line to it in the following format:**
      `Bug #999: a description of the bug fix (Your Name)`
      or
      `Enh #999: a description of the enhancement (Your Name)`

      Commit this change to `CHANGELOG.md` normally. It'll be included in your PR on next step and it's good.
      This step is proposed first in [#167](https://github.com/clevertech/YiiBooster/issues/167) and it's definitive. Please, do it.

7.   **Push this branch to your Github fork.**
     `git push origin myfeature`
     Note that you use the remote named `origin` here. It points to _your_ _fork_ of the YiiBooster.

8.   After this, go to [clevertech/YiiBooster](https://github.com/clevertech/YiiBooster), hit **"Pull Request"** and choose your branch at your fork as a source and desired `*-wip` branch as a receiver of pull request.

Please, do not forget to reference the original issue as '#'+issue-number in the description of your pull request. It's _very_ important, it'll help admins to quickly find what issues can be closed with this pull request.

Please, I know, too, that it all is an ass-crunching hassle, however, Git along with Github _forces_ us to work in such a way, thank you.