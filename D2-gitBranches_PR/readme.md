## Branches 
- branch name convention</br>
  fix/wrong-youtubestats
- for best practises to resolve any issue create a branch and then solve it 
- after making change in branch, if satisfied with it ... so now we wanna merege it to the main/master/upstream </br>
so we create a PR

## PR request 
EX-</br>
fix/typo-heading of the home page </br></br>
title: fix: typo in heading </br>
des: fixes #1
</br>
maintainer can merge & close
</br>
//if merged then maintainer close/delete the branch  

----------
## solving a issue
- select a issue
</br> change piyushh to piyush on server website

- Now make a branch </br>
to make a branch write the below command in vs code terminal
```
git checkout -b "new branch name"
```
git checkout -b "fix/typo-in-homepage"
 //now fix the issue in the local machine
and then test it 
</br>
in vscode terminal 
```
git add .
```
```
git commit -m "commit message"
```
```
git push --set-upstream origin fix/typo-in-homepage
```

now new branch is created
</br>
now make a PR</br>
- github repo >>pull request>>new pull request</br>
now select which branch is to merge in which</br>
base:main<- compare: fix/ typo-in-homepage</br>

- now create a pull request
Title: fixed typo</br>
PR description :</br>
fixes #123</br>
------
in terminal vs code
```
yarn dev
```
- to run it on the local host 3000 //on localhost3000 check the solution, take screenshot and paste it in PR desc. 
</br>
so if the PR is good then the maintainer will merge it </br>
and delete the fix/typo branch as best practice </br>
---
//now if we do something like </br>
//main>fix/typo »git checkout -b "something"</br>
  ie we are creating a branch from main-->fix/typo--->something</br
now if we we make PR from something branch then it will also commit the changes of fix/typo branch </br>

`So do not create a branch from deleted branch `</br>

```
git switch main
```
//now on local machine vscode repo is behind 2 commit from the forked github repo  
```
git pull
```
now github forked repo and local repo are in syn
</br>
` always create separate branch for separate issue for best practices`
