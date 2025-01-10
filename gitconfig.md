
```bash

[user]
	name = Ahmed Midani
	email = ...

[alias]
  co = checkout
  cob = checkout -b
  ci = commit
  cm = commit -m
  st = status -sb
  br = branch
  brd = branch --format='%(HEAD) %(color:yellow)%(refname:short)%(color:reset) - %(contents:subject) %(color:green)(%(committerdate:relative)) [%(authorname)]' --sort=-committerdate
  mg = merge
  se = !git rev-list --all | xargs git grep -F
  slog = log --pretty=format:'%C(yellow)%h%Creset - %C(blue)%an%Creset \t %C(cyan)%ar:%Creset %s' -n 20
  last = log -1 HEAD --stat --pretty=format:'%C(yellow)%h%Creset - %C(blue)%an%Creset \t %C(cyan)%ar:%Creset %s'
  gl = config --global -l

  hist = log --pretty=format:'%h %ad | %s%d [%an]' --graph --date=short
  lg = log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %Cgreen(%cr) %C(bold blue)<%an>%Creset%s' --abbrev-commit --date=relative
  ll = log --oneline
  diff = difftool -t vimdiff -y

[filter "lfs"]
  clean = git-lfs clean -- %f
  smudge = git-lfs smudge -- %f
  process = git-lfs filter-process
  required = true

[core]
	autocrlf = false

```