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

ex:
```
➜  git-in-depth git:(main) echo 'Hello World!' > hello.txt
➜  git-in-depth git:(main) ✗ git add hello.txt
➜  git-in-depth git:(main) ✗ git commit -m "Initial Commit" 
[main 08fcff8] Initial Commit
 1 file changed, 1 insertion(+)
 create mode 100644 hello.txt
➜  git-in-depth git:(main) 
```

## Git Areas and Stashing
...
