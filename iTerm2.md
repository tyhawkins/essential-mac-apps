# iTerm2 Configuration

1. Install the shell integration from the iTerm2 menu
2. Edit your .bashrc and add the following:

```
updateitermvars() {
  context=$(kubectl config current-context)
  iterm2_set_user_var kube_context "$context"
  iterm2_set_user_var pwd "$PWD"
}

PROMPT_COMMAND='history -a; updateitermvars'
```

3. Then edit your default profile and go to Session,
then enable the status bar and configure it.

4. Add an interpolated string like `\(user.kube_context)` or
`\(user.pwd)` (reference above) and your context will
show up on the status bar of iTerm2.  You can also add
battery, CPU, memory, network utilization monitors, as
well as a built-in component that will tell you what
git branch you're on.
