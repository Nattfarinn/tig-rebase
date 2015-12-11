# tig-rebase
Bash script to perform simple ```git rebase -i``` operations right in command line (ie. used as ```tig``` bindings)
# Usage
```
tig-rebase.sh fixup|ascend|descend|reword|abort HASH
```
# Example .tigrc
```
# Fixup with parent commit
bind main <Ctrl-f> !tig-rebase.sh fixup %(commit)
bind diff <Ctrl-f> !tig-rebase.sh fixup %(commit)

# Rebase to move commit up
bind main <Ctrl-k> !tig-rebase.sh ascend %(commit)
bind diff <Ctrl-k> !tig-rebase.sh ascend %(commit)

# Rebase to move commit down
bind main <Ctrl-j> !tig-rebase.sh descend %(commit)
bind diff <Ctrl-j> !tig-rebase.sh descend %(commit)

# Edit commit message
bind main <Ctrl-r> !tig-rebase.sh reword %(commit)
bind diff <Ctrl-r> !tig-rebase.sh reword %(commit)

# Abort current rebase
bind main <Ctrl-x> !tig-rebase.sh abort
bind diff <Ctrl-x> !tig-rebase.sh abort
```
