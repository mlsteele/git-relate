# git-relate

Describe how two git commits are related in history.

```
Usage:
git-relate <commit> [<commit>]
```

```
# Relate the current HEAD to master
$ git relate master
master (0be5ac6) -> 6 commits -> HEAD (65c19ec)

# Relate two commits by hash
$ git relate 1acd66a34 7b69d8a5a
The common ancestor is miles/keep-paper-key~2 (d17bd9b)

# Relate two branches
$ git relate miles/proxy miles/tiny
The common ancestor is tags/v1.0.27~576 (5848b25)
```

## Setup
Add the script to your path
```
git clone git@github.com:mlsteele/git-relate.git
cp git-relate/git-relate ~/bin/git-relate
# OR
ln -s ~/code/git-relate ~/bin/git-relate
```

AND/OR add the git alias to `~/.gitconfig`
```
...
[alias]
...
	# Examine how two commits are related in history.
	relate = !~/bin/git-relate
...
```
