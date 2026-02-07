# Git CLI
> I Forget this stuff all the time


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
This unstages the file then it restores the conflict markers - mainly if you merged the WRONG resolution.

## Push resolved merges
<pre>git push origin main</pre>
'main' refers to your current branch (usually main in my case)
