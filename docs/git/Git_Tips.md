---
title: GIT CLI Tips
---

# Git CLI Tips
> It's not the whole docs to git and certainly not how they'd write it - which is over-complicated and generally painful to read (in my opinion).

## Create a repo
<pre>git init .</pre>
This makes a git repo in the current directory of your CMD/Terminal

## Add files
<pre>git add &gt;filename&lt;</pre>
This adds one file or directory

<pre>git add .</pre>
<!-- @IGNORE:COMMA_PARENTHESIS_WHITESPACE@--><!-- @IGNORE:MORFOLOGIK_RULE_EN_GB@-->
This adds everything in the current directory, obviously listening to .gitignore

## Commit
<pre>git commit -m "Some message here!!"</pre>
This commits to the local repository, essentially stages changes to be pushed.

## Push
<pre>git push</pre>
This pushes changes to a remote repository, if you have one set.
If you don't have a remote repository set, it will just whinge at you.

<!-- @IGNORE:MORFOLOGIK_RULE_EN_GB@-->
## Unstage (remove) all current files from the current commit
<pre>git reset --soft HEAD~1</pre>

## Pull latest changes
<pre>git fetch origin</pre>
<pre>git pull origin main</pre>
'main' refers to your current branch (usually main in my case)

## See file(s) status(es)
<pre>git status</pre>
Files which are conflicted would show beneath 'both modified'

## See diffs
<pre>git diff --name-only --diff-filter=U</pre>

## Mark file resolved
<pre>git add &lt;file&gt;</pre>

## Abort the merge
<pre>git merge --abort</pre>
Returns the state of all files to pre-merge

## Re-merge a file
<pre>git reset HEAD &lt;file&gt;</pre>
<pre>git checkout --merge &lt;file&gt;</pre>
<!-- @IGNORE:MORFOLOGIK_RULE_EN_GB@-->
This unstages the file then it restores the conflict markers - mainly if you merged the WRONG resolution.

## Push resolved merges
<pre>git push origin main</pre>
'main' refers to your current branch (usually main in my case)