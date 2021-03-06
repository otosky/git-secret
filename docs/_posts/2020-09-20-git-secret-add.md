---
layout: post
title:  'git-secret-add'
date:   2020-09-20 15:12:56 -0400
permalink: git-secret-add
categories: command
---
git-secret-add - starts to track added files.
=============================================

## SYNOPSIS

    git secret add [-i] <pathspec>...


## DESCRIPTION
`git-secret-add` adds a filepath(s) into `.gitsecret/paths/mapping.cfg`
and ensures the filepath is mentioned .gitignore.

When adding files to encrypt, `git-secret-add` (as of 0.2.6) will ensure that they are ignored by `git` by mentioning
them in .gitignore, since they must be secure and not be committed into the remote repository unencrypted.

If there's no users in the `git-secret`'s keyring, when adding a file, an exception will be raised.

Use the `git secret add` command to add filenames to this file.
It is not recommended to add filenames directly into `.gitsecret/paths/mapping.cfg`.

(See [git-secret(7)](http://git-secret.io/git-secret) for information about renaming the .gitsecret
folder using the SECRETS_DIR environment variable.

## OPTIONS

    -i  - does nothing, adding paths to .gitignore is now the default behavior.
    -h  - shows this help.


## MANUAL

Run `man git-secret-add` to see this note.


## SEE ALSO

[git-secret-init(1)](http://git-secret.io/git-secret-init), [git-secret-tell(1)](http://git-secret.io/git-secret-tell), 
[git-secret-hide(1)](http://git-secret.io/git-secret-hide), [git-secret-reveal(1)](http://git-secret.io/git-secret-reveal)
