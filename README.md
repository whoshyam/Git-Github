https://www.javatpoint.com/git

- [**Git-docs**](https://git-scm.com/docs)
- [**Markdown-guide**](https://www.markdownguide.org/basic-syntax/)
# First Contributions
#### If you don't have git on your machine, [install it](https://docs.github.com/en/get-started/quickstart/set-up-git).

## Fork repository

Fork this repository by clicking on the fork button on the top of this page.
This will create a copy of this repository in your account.

## Clone the repository

<img align="right" width="300" src="https://firstcontributions.github.io/assets/Readme/clone.png" alt="clone this repository" />

Now clone the forked repository to your machine. Go to your GitHub account, open the forked repository, click on the code button and then click the _copy to clipboard_ icon.

Open a terminal and run the following git command:

```
git clone "url you just copied"
```

where "url you just copied" (without the quotation marks) is the url to this repository (your fork of this project). See the previous steps to obtain the url.

## Create a branch

Change to the repository directory on your computer (if you are not already there):

```
cd repo name
```

Now create a branch and switch to the branch 

```
git switch -c your-new-branch-name
```
`for switching between branches use command:` 
```
git switch
``` 

## Make necessary changes and commit those changes

If you go to the project directory and execute the command `git status`, you'll see there are changes.

Add those changes to the branch you just created using the `git add filename` or 'git add .' command:

```
git add .
```

Now commit those changes using the `git commit` command:

```
git commit -m "message"
```
## Push changes to GitHub

Push your changes using the command `git push`:

```
git push -u origin your-branch-name
```
## Submit your changes for review

If you go to your repository on GitHub, you'll see a `Compare & pull request` button. Click on that button.

Now submit the pull request.

good,if merged by maintainer 
