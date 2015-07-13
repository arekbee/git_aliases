# GIT Config 

To use git aliases you need to add these lines into .gitconfig file
To configure .gitconfig file you need to run this command:
```bash
    git config --global --edit
```
Into this file write this text:

```bash
[include]
    path = /PathToRepos/git_config/gitalias
    
```

After saving .gitconfig, type this command to see the definition of aliases:

```bash
  git aliasesd
```
