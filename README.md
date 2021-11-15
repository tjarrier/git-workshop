# Git working

## Installation
Use git to clone this repository  
`git clone https://gitlab.com/tjarrier/git-working.git`

## Documentation
Documentation Git : https://git-scm.com/book/fr/v2

## To Do

### Rebase
1. Create a first branch from **master** :  `git branch branch_1`  

2. Create a second branch from **master** : `git branch branch_2`

3. Go to **branch_1** and modify the file **README.md** (under "To Do" title) : `git checkout branch_1`  
Commit your modifications : `git commit -a -m "Commit branch_1 modifications"`

4. Go to **branch_2** and modify the file **README.me** (the same lines) : `git checkout branch_2`  
Commit your modifications : `git commit -a -m "Commit branch_2 modifications"`

5. Merge **branch_1** into master : `git checkout master && git merge branch_1`

6. Rebase **branch_2** on master : `git checkout branch_2 && git reabse master`

7. Resolve conflicts

8. Merge **branch_2** into master : `git checkout master && git merge branch_2`

9. Look git logs : `git log --pretty=oneline`

### Cherry-pick
