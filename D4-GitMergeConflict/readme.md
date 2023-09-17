## conflicts occurance
- let cal.com repo has 2 issue </br>
  issue#1 </br>
  this issue req changes on line 32</br>
  ie change var a to b</br>

  issue#2</br>
  this issue also req changes on line 32</br>
  change value 1 to 37 

- now user1 work on issue#1 and user2 works on issue#2

- now user 1 makes  a branch and solves the issue  user1/fix... --> cal/main
 and makes a PR which is open

where as user2 is still working on issue2 which is till the original line </br>
and now user2 makes a PR </br>
user2/fix... --> cal/main</br>

now user1 PR is merged  

- now if we try to merge user2 PR then there will be a conflict as in user2 PR it does not have the changes of user2 so now github is confused which change is to accept as both the user changes on the same line 
` now user2 have to resolve the conflict user2 ki files changed mae kuch aisa dhkega` </br>

![Alt text](image-1.png)

</br>

` now user2 have to wisely deal with conflict 
as dev should see other code also so that conflict does not now ` 
</br>
ie --> 

![Alt text](image-2.png)
</br>

- after user1 PR merge 
  user2 wants to merge its PR also then after making changes 
  `git pull upstream main`

now it shows merge conflicts 
user2 have to handle conflicts wisely 
 
`git add .`

`git rebase --continue`

`commit message`

`git status`

`git push -f`











