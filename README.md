# GIT Config 


# How Can I get it?
## Linux  and Mac OS

First you need to download raw file with all aliases:

```bash
curl -o  gitalias https://raw.githubusercontent.com/bnbsystems/git_config/master/gitalias/gitalias
```

than type in console this command:

```bash
git config --global include.path /PathToFile/gitalias
```

## Manually by cloning whole repo.
To configure .gitconfig file you need to run this command:
```bash
    git config --global --edit
```
and then write this text inside console editor:

```bash
[include]
    path = /PathToRepos/git_config/gitalias
```


# What kind of aliases there are?
Below are cases where you could apply aliases.


### Are you tired of writing most common command git status? Now, you can type only:
```bash
git s
```

### How can I get list of aliases
```bash
git aliases
```
![git aliases](/README_files/alias.png)


### How can I get definition of aliases?
To command git aliases add letter 'd' (like definition) to see the definition of aliases:
```bash
  git aliasesd
```
![git aliasesd](/README_files/git_aliasesd.png)


### Are you tired of writing git add, git commit message, git push origin and than you need to check logs? You can run it with one command ACP:

ACP stand for Add, Commit Push 

```bash
  git acp "message"
```


### Would you like to download repo. without .git folder
```bash
  git download https://github.com/bnbsystems/git_config.git
```

> Below examples are run agains https://github.com/fsharp/fsharp repository


### How can I get authors for given repo. with information about number of commits?
```bash
git authors | head -10
```
![git authors](/README_files/authors.png)


### When I need to go deep into code, I do not know what file is importen. Maybe if I could get information about most often changed files?

Yes, you can do it, by running churn commaned

```bash
git churn
```
![git churn](/README_files/churn.png)



### I would like to remove all non-versioned or not commited files. Is there a one command to do this?
Yes. Clean-all
```bash
git git clean-all
```

### I am trying to find file, where file name constains special string (like '.exe').

```bash
git find-file ".exe"
```
![git find-file](/README_files/find-file.png)

### I would like to see the history of whole repo. in nice way?
Just write git history

```bash
git hist
```
![git hist](/README_files/hist.png)

If you write 'histd' than you will get history with commit messages.

### I have navigate so deep into folders, that I do not know that is the root location of repo?
Magic word is root

```bash
git root
```

### I would like to see files which will not be added into repo. (because .gitignore applies)

Like ls but with ignore sufix:
```bash
git ls-ignore
```


### I need to quick add required submodules:
```bash
git siur
```

### I do not know which branches are still waiting to be merged.

```bash
git unmerged-branches 
```
![git unmerged-branches](/README_files/unmerged-branches.png)



### Can I see graph of commits.
Yes, you can, but this is still work in progress and you need to have graphviz application

```bash
git graphviz  -n10 > graph.dot
graphviz\dot.exe -Tpng graph.dot -o graph.png​
```
![git graphviz](/README_files/graph.png)


