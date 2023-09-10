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
  what happens now is `forked repo ke feat/..` branch mae changes hue h ar `feat/.. branch`ko merge kiye h original repo mae 
`abhi bhi forked repo ke main mae let --let hi h const nhi h main mae 
while in original repo main let has been changed into const hogya`

what should we do now ki upstream ka main ar forked ka main ek ho jae ar sync ho jae !!

hm local machine ko bta rhe h ki upstream bhi kuch hota h 
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
means ki jo upstream ka main h wo local machine/vscode pe aajae h but wo abhi bhi github ke `forkedrepo` pe nhi h so to do it 

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
