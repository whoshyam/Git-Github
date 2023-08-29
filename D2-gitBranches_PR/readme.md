## Branches 
- branch name convention</br>
  fix/wrong-youtubestats
- for best practises to resolve any issue create a branch and then solve it 
- after making change in branch, if satisfies with it ... so now we wanna merege it to the main/master/upstream </br>
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
</br> piyushh ko piyush krna h website se

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
git add.
```
```
git commit -m "commit message"
```
git commit -m "fixed typo"
```
git push --set-upstream origin fix/typo-in-homepage
```

now new branch is created
</br>
now make a PR</br>
- repo >>pull request>>new pull request</br>
now select kis branch ko kismae merge karna h </br>
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
- to run it on local host 3000 //uss localhost3000 pe fix ka SS lelo ar PR mae paste krdo 
</br>
so if the PR is good and the maintainer merge it </br>
and delete the fix/typo branch as best practise</br>
---
//now it if do something like </br>
//main>fix/typo »git checkout -b "somnethig"</br>
mtlab main se jo fix typo name ka branch bna tha usmae fir branch bnane ka command likhe h </br>
th fix/typo branch se something branch aaega </br> 
wo ki fix/typo wale change ko commit karega </br>

so del branch se branch nhi banana h </br>

so now in vs terminal 
```
git switch main
```
//ab local vscode ka repo 2 commit piche h th do 
```
git pull
```
ab github ar local repo sync ho jaega 
</br>
if main has issue #1,#2,#3</br>
ar agar fork ke repo mae changes kare jo fixes  issue1,2,3 </br>
ar PR daal de th invalid hoga </br>
as har ek issue ke liye ek alag branch bano ar usko PR mae dalo</br>

