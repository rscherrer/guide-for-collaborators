# guide-for-collaborators

This is the workflow I use when working with collaborators on repos hosted under my username. Inspired by [Richel Bilderbeek](https://github.com/richelbilderbeek).

## Branches

My repos are usually structured in the following way: in addition to the **main** branch, there usually is a **develop** branch where changes can be implemented. When collaborating with multiple people, I like to create one branch for each contributor (e.g. **bob**), which they can work on. The idea is that changes added to the branch of a certain user are then merged into _develop_, and if that does not cause any bug or weird issue, to then merge _develop_ into _main_.

So:

**bob** --> **develop** --> **main**

## For collaborators

Please make sure that you are working on your own branch! From within the repo, use (in the terminal):

```{shell}
git checkout bob
```

Or use the equivalent provided your GitHub Desktop client if you use one (e.g. GitHub Desktop for Windows).

Once your changes have been implemented, committed and pushed to GitHub, you can open a pull request online to merge your branch into _develop_.

There may be changes that others have merged into _develop_ but that are not yet present on your own personal branch. You can make sure to be working on the latest version by regularly pulling from _develop_ or _main_ into your branch:

**main** / **develop** --> **bob**

And remember, this won't erase work you've been doing on _bob_, as merging of branches in git is a non-destructive process. 

## Merge conflicts

It may happen that branches cannot be automatically merged, because incompatible changes have occurred on both sides. This leads to _merge conflicts_, and those must typically be solved manually (i.e. you must choose which of the two conflicting versions you want to keep for the incompatible piece of code or content). If in doubt, don't hesitate to contact me.

Looking forward to collaborating with you!
