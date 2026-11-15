# 2. Where are Git Hooks stored?
Whenever you initialize a Git repository:

```GitHub 
git init
```
Git creates an internal directory:

```Plain Text 
.git/
   hooks/
       applypatch-msg.sample
       commit-msg.sample
       pre-commit.sample
       pre-push.sample
       post-commit.sample
       post-merge.sample
```

These are sample hook scripts.

To activate a hook, create a file with the correct name, without .sample.

For example:

```Plain Text
.git/hooks/pre-commit
.git/hooks/pre-push
```

Git automatically recognizes these names.

> [!IMPORTANT]
> .git/hooks is local to each developer's repository. It is not normally included in Git commits or pushed to GitHub.

For team sharing, we will use a version-controlled .githooks directory.



