# What is Git?
- Git it's a distributed version control system
- Git is software for tracking changes in any set of files for development

The git stores things as in git object and their basic one is called a blob & Generate the SHA1 of the contents with the metadata as it`s stored in git

ex:
```
➜  ~ echo 'Hello, World!' | git hash-object --stdin
8ab686eafeb1f44702738c8b0f24f2567c36da6d
```

## Git Commit
In Git, a commit is a snapshot of repo at a specific point in time. there's three types of object will create when we do git commit
- Tree
- Blob
- Commit

## Git Areas and Stashing
Three areas where code lives
- Working area
  - The files in your working area that are also not in the staging area are not handled by git
  - Also called untracked filed 
- Staging area
  - What files are going to be part of the next commit
  - The staging area is how git knows what will change between the current commit and the next commit 
- Repository
  - The files git knows about!
  - Containt all of your commits

Stashing 
  - Save un-commited work (temporery code)
  - The stash is safe from destructive operations




