# Connecting and syncing with upstream concept

- let ek repo h originaldev naam ka ,uska ek issue #123 h jo hme solve krna h
ex-let ko const karna h ek line pe  

so, as usual steps
fork orginal>git clone to own machine > 
- now we have original repo
  forked repo on github
  local machine pe clone repo

- open terminal
//folder for repo
```
cd coding  
```
```
git clone link
```
```
cd reponame
``` 
// isse vscode khul jaega main branch ka
```
code . 
```
 
```
git remote -v 
```
//tells ki push/pull karenge th kis repo se link hoga
origin:(fetch)/pull
origin:(push)

//now local set up
```
yarn 
```
jb set up hogya tb, to run at local host3000,checks the issue 
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
- note-ye command dalne ke baad apne aap ek git push ka command aajaega just copy it
```
git push --set-upstream origin feat/let-to-const
```
// now if we go github and check branches th ek new branch ban gya h ar PR karenge tb
- PR 
PR desc: fixes #123

now the maintainer of original repo merge the PR

- now if we select a new issue from original repo then 
```
git switch main
```

//krna chahiye ki ab ek  branch bna ke uss issue pe kaam kare but but 
what happens now is forked repo ke feat/.. branch mae changes hue h ar feat/.. branch ko merge kiye h original repo mae 
abhi bhi forked repo ke main mae let --let hi h const nhi h main mae 
while original repo ke main mae let const hogya h 

//what should we do now ki upstream ka main ar forked ka main ek ho jae ar sync ho jae !!
**git remote add upstream url-of-original-repo
//hm local machine ko bta rhe h ki upstream bhi kuch hota h 
now
**git remote -v
origin/forked(fetch)
origin/forked(push)
upstream(fetch)
upstream(push)

**git pull upstream main
means ki jo upstream ka main h wo local machine/vscode bolo pe aa gyi h but wo abhi bhi github ke forkedrepo pe nhi h so to do it 
**git push 

now everything is in sync 
upstream main
forkedrepo main
clone/localmachinerepo

//**git merge upstream/main //means ki upstream ka mainn apne forked repo jo github pe h usmae daal do



------------------------------
Code sync problem when multiple contributors working on different issues simultaneously

ie agar jb hme upstream se fork ar koi issue solve kiya L34 code daal dete ar PR karne se phle koi ar user contri krdeta h L42 upstream mae daal deta h 
ab hmara forked repo ,local machine piche h upstream se th then do 
**git remote add upstream <url of original repo>
**git upstream main
**git push origin main

**git checkout -b "abc"
**git merge origin main 

 














