Config
======

### List current config enties

    git config -l

### Common config entries

    git config --global user.name 'user_name'
    git config --global user.email 'user@host.com'
    
See `~/.gitconfig`file for current user configuration.    


### Git add and commit in one single command

Create an alias with

    git config --global alias.ac '!git add -A && git commit'
    
And use it with

    git ac -m 'My commit message'


Working with repositories
=========================

### Initialise a repo without working dir (server)

    > mkdir project.git
    > cd project.git
    > git init --bare


### Deploy in a directory after received a push

From a bare repository, Create an executable file `.git/hook/post-receive` with the folliwing
    
    #!/bin/sh
    GIT_WORK_TREE=/path/to/my/site/checkout git checkout -f




