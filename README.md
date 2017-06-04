
# git-fixup

When you have a single line change in git that you want to apply as a 'fixup' to a previous commit,
this command tries to make it as easy as possible.

All the information is available to do the work automatically so the user should not have to
retrieve the reference for the commit in order to use the `git commit --fixup <ref>` command. For a
single line change, `git blame` can identify the commit in question.

## Status

This is a hacky experiment that doesn't do any checking and problem makes too many assumptions but
works on simple cases.

## Further work

It currently works with `git diff` but it should probably prefer `git diff --cached` so that you can
add the change you want first in order to help guide the process. 

If there are multiple changes then it should be possible to provide a `git add -p` style interaction
prompt for repeating the command on different chunks. Maybe.

