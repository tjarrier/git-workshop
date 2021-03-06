# Git workshop

## Installation
Use git to clone this repository  
`git clone https://github.com/tjarrier/git-workshop.git`

## Documentation
Git documentation : https://git-scm.com/book/fr/v2

## To Do

### Rebase
Git rebase documentation : https://git-scm.com/book/fr/v2/Les-branches-avec-Git-Rebaser-Rebasing

1. Create a first branch from **master** :  `git branch branch_1`  

2. Create a second branch from **master** : `git branch branch_2`

3. Go to **branch_1** and edit the file **README.md** (under "To Do" title) : `git checkout branch_1`  
Commit your modifications : `git commit -a -m "Commit branch_1 modifications"`

4. Go to **branch_2** and edit the file **README.me** (the same lines) : `git checkout branch_2`  
Commit your modifications : `git commit -a -m "Commit branch_2 modifications"`

5. Merge **branch_1** into master : `git checkout master && git merge branch_1`

6. Rebase **branch_2** on master : `git checkout branch_2 && git reabse master`

7. Resolve conflicts (keep all modifications)

8. Merge **branch_2** into master : `git checkout master && git merge branch_2`

9. Look git logs : `git log --pretty=oneline`

### Cherry-pick
Git cherry-pick documentation : https://git-scm.com/docs/git-cherry-pick/fr

1. Create a first branch from **master** :  `git branch branch_3`

2. Go to **branch_3** : `git checkout branch_3` 

3. Create new file **documentation.md** and commit :  
```
touch documentation.md
git add documentation.md
git commit -m "Commit documentation.md in branch_3"
```

4. Edit the file **README.md** (under "To Do" title)
Commit your modifications : `git commit -a -m "Update README.me in branch_3"`

5. Edit **documentation.md** (add anything)
Commit your modifications : `git commit -a -m "Update documentation"`

6. Now, to retrieve specific commits and apply them on the branch **master** :  
Look at the git logs to find the hash of your commits : `git log --pretty=oneline` 
```
git checkout master
git cherry-pick <commit>
git log --pretty=oneline
```
