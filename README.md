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

Use this command line ```tree .git/objects``` to see the directory

```
tree .git/objects     
.git/objects
├── 06
│   └── e15c9e8686fd4c1a8081f830b5735a66ae2858
├── 07
│   └── cde6e5c756e879a06856d2f4902d4230cc86f6
├── 08
│   └── fcff8873c78d1c276c49da4be8523f32324178
├── 1b
│   └── 89f0d88f945438d1a3f44cd9885c97318f4e31
├── 21
│   └── 682235cc91b901f3da8c2a60979b02c0bc3e80
├── 27
│   └── fa3df8636b4390c78cbe93ec0e388e46814cd4
├── 66
│   └── 869eec9f3c1d666d6aa414c293db3c22e954d1
├── 83
│   └── 9eae196afce3d3440989a2e68fadb86f184566
├── 89
│   └── 2ff268dd0d98234d99c61d87d4098dcea20586
├── 8f
│   └── 1e494dc8c738db7eef1d3e7e8ea2115b2a5fba
├── 98
│   └── 0a0d5f19a64b4b30a87d4206aade58726b60e3
├── a4
│   └── 8ca63b3e436594946722d2a1ccc6d622c5066d
├── aa
│   └── 28f9372a2de3de1de7c2ad458829b98fc091ac
├── ac
│   └── 0a169682966fdf7463347a95fc2d1758fd3f50
├── cb
│   └── b65c7331f475ca8cbae8b089f19bc4076fa8af
├── e7
│   └── 64b7cf5e02e3102bbbcf66ca40e575e8cf91bb
├── f9
│   └── c02c1063f4d5d8e492be14fa46c012e6fa785f
├── info
└── pack
    ├── pack-77332c502f4912bc6ffc4dd9084573edbb45b78c.idx
    └── pack-77332c502f4912bc6ffc4dd9084573edbb45b78c.pack

19 directories, 19 files
```

### Print The Type
```
➜  git cat-file -t 06e15 
tree
➜  git cat-file -t 07cde6
blob
➜  git cat-file -t 08fcff
commit
```
### Print The Contents
```
git cat-file -p 08fcff
tree 839eae196afce3d3440989a2e68fadb86f184566
parent 11a1d208dd3454f7afedd676998e92bba3191cbb
author mwsucahyo <m.r.sucahyo@gmail.com> 1642460965 +0700
committer mwsucahyo <m.r.sucahyo@gmail.com> 1642460965 +0700

Initial Commit
```


## Git Areas and Stashing
### Three areas where code lives
- Working area
  - The files in your working area that are also not in the staging area are not handled by git
  - Also called untracked filed 
- Staging area
  - What files are going to be part of the next commit
  - The staging area is how git knows what will change between the current commit and the next commit 
- Repository
  - The files git knows about!
  - Containt all of your commits

### Stashing 
Git Stash is very helpful when there is a condition where we are working on something but it hasn't been finished yet it turns out that there is a bug or other feature with a higher priority, because with git stash we can save our code temporarily so that we can reuse it at any time.

  - Save un-commited work (temporery code)
  - The stash is safe from destructive operations

#### Git stash basic use

Stash changes
```
$ git stash
```

List changes
```
$ git stash list
```

Show the contents
```
$ git stash show stash@{0}
```

Apply the last stash
```
$ git stash apply
```

Apply a specific stash
```
$ git stash apply stash@{0}
```

Stashing all files
```
$ git stash --all
```

Delete last stashing and applying change
```
$ git stash pop
```

Delete last stash
```
$ git stash drop
```

Delete specific stash
```
$ git stash drop stash@{n}
```

Delete all stash
```
$ git stash clear
```
