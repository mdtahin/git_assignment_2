## Initialize the Repository

### Create a new directory and initialize it as a Git repository

<em> $ mkdir git_assignment_2 </em>

<em> $ cd git_assignment_2 </em>

<em> $ git init </em>


### Add a README.md file, Stage and commit the README.md file

<em> $ touch README.md  </em>
<em> $ git add README.md </em>
<em> $ git commit -m “add README.md file to repository” </em>

### Add a remote repository with git URL and Push the initial commit to the remote repository

<em> $ git remote add origin git@github.com:mdtahin/git_assignment_2.git </em>
<em> $ git branch -M main </em>
<em> $ git push -u origin main </em>

## Create and Work on new branches  feature-1 and feature-2

<p> For feature 1 branch </p>

### Create and switch to a new branch named feature-1

<em> $ git checkout -b feature-1 </em>

### Add feature-1.txt with a single line and commit

<em> $ echo "This is 1st line as content on feature-1 branch" > feature-1.txt </em>
<em> $ git add feature-1.txt </em>
<em> $ git commit -m "Add feature-1.txt with initial content" </em>

<p> For feature 2 branch </p>

### Create and switch to a new branch named feature-2

<em> $ git checkout -b feature-2 </em>

### Add feature-2.txt with a single line and commit

<em> $ echo "This is 1st line as content on feature-2 branch" > feature-2.txt </em>
<em> $ git add feature-2.txt </em>
<em> $ git commit -m "Add feature-2.txt with initial content" </em>

### Push the feature-1 and feature-2 branch to the remote repository 

<em> $ git push -u origin feature-1 </em>
<em> $ git push -u origin feature-2 </em>

##Review and Update

### Rebase the branch onto the latest main branch

<em> $ git fetch origin </em>
<em> $ git checkout main </em>
<em> $ git pull origin main </em>
<em> $ git checkout feature-1 </em> 
<em> $ git rebase main </em>
-Resolve any conflicts if they arise. After resolving conflicts: 
<em> $ git add . </em>
<em> $ git rebase --continue  </em>

### Push the updated branch (use --force if anything rebased) 

<em> $ git push --force </em>

## Clean Up Merged Branches

<em> $ git checkout main </em>
-Switch back to the main branch

 ### Delete local feature branches

<em> $ git branch -d feature-1 </em>
<em> $ git branch -d feature-2 </em>

### Delete remote feature branches

<em> $ git push origin --delete feature-1 </em>
<em> $ git push origin --delete feature-2 </em>


