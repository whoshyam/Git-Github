## Connecting and syncing with upstream concept
- let there is a repo "originaldev" that has issue #123
  ex-change let to const  

so, as usual steps
fork orginal>git clone to own machine > 
- now we have
  `original repo` 
  `forked repo on GitHub`
  `local machine pe clone repo`

- open terminal
```
cd coding  
```
```
git clone link
```
```
cd reponame
``` 
```
code . 
```
`tells if we do push/pull then it is linked to which repo`
```
git remote -v 
```
`origin:(fetch)/pull`</br>
`origin:(push)`

//now local set up
```
yarn 
```
when repo is locally set then run it on localhost3000 and checks the issue that it is actually there or not
```
yarn dev 
```

// now make new branch 
```
git checkout -b feat/let-to-const 
```
after making changes in the branch ,now add changes to stage 
``` 
git add .
```
//now commit and push
```
git commit -m "changed let to const"
```
- note-after executing above command there will be automatically a command for push on upstream
```
git push --set-upstream origin feat/let-to-const
```
now if we go github and check branches then there is a branch now we can make a PR
- PR 
PR desc: fixes #123

now the maintainer of original repo merges the PR

---------------------------------------
- now if we select a new issue from original repo then 
```
git switch main
```

- now what should be done is make a new branch and then work on that issue but 
  what happens now is `forked repo's feat/..` branch is merged in original repo
`but but now still the github forked repo's main let is let it hasn't changed yet
while in original repo main let has been changed into const hogya`

what should we do now so upstream main and forked main will sync!!</br>
now we are letting the local machine that there is something called upstream
```
git remote add upstream url-of-original-repo
```
```
git remote -v
```
`origin/forked(fetch)`
`origin/forked(push)`
`upstream(fetch)`
`upstream(push)`

```
git pull upstream main
```
means ie sync original repo and local machine repo but the github forked repo is not yet synced so to make it happen we do the`push` command 
```
git push 
```
now everything is in sync 
`upstream main`
`forkedrepo main`
`clone/localmachinerepo`

//
git fetch</br>
git merge upstream/main</br>
git commit -m "Merged changes from upstream main branch"</br>
git push
//

----
## Code sync problem when multiple contributors working on different issues simultaneously

ie agar jb hme upstream se fork ar koi issue solve kiya L34 code daal dete ar PR karne se phle koi ar user contri krdeta h L42 upstream mae daal deta h </br>
ab hmara forked repo ,local machine piche h upstream se th 
then do 
ie if we fork a repo and work on some issue and maked changes on line34 and makes a PR but before the PR merge </br>
some other user works on another issue and makes changes on line42 and makes a PR and then the PR is merged in the main </br>
then now the local machine and github forked repo is behind the upstream main 
so to make it happen we do -->

```
git remote add upstream <url of original repo>
```
```
git upstream main
```
```
git push origin main
```
```
git checkout -b "abc"
```
```
git merge origin main 
```
