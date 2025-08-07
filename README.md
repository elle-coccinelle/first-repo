
USER@DESKTOP-7TKVOOD MINGW64 ~/Desktop/elle_coccinelle (master)
$ mkdir learn_git

USER@DESKTOP-7TKVOOD MINGW64 ~/Desktop/elle_coccinelle (master)
$ cd learn_git

USER@DESKTOP-7TKVOOD MINGW64 ~/Desktop/elle_coccinelle/learn_git (master)
$ touch third.txt.

USER@DESKTOP-7TKVOOD MINGW64 ~/Desktop/elle_coccinelle/learn_git (master)
$ git init
Initialized empty Git repository in C:/Users/USER/Desktop/elle_coccinelle/learn_git/.git/

USER@DESKTOP-7TKVOOD MINGW64 ~/Desktop/elle_coccinelle/learn_git (master)
$ git add third.txt
fatal: pathspec 'third.txt' did not match any files

USER@DESKTOP-7TKVOOD MINGW64 ~/Desktop/elle_coccinelle/learn_git (master)
$ git add third.txt.
error: open("third.txt."): No such file or directory
error: unable to index file 'third.txt.'
fatal: adding files failed

USER@DESKTOP-7TKVOOD MINGW64 ~/Desktop/elle_coccinelle/learn_git (master)
$ touch third.txt

USER@DESKTOP-7TKVOOD MINGW64 ~/Desktop/elle_coccinelle/learn_git (master)
$ git add third.txt

USER@DESKTOP-7TKVOOD MINGW64 ~/Desktop/elle_coccinelle/learn_git (master)
$ git commit -m "adding third.txt"
[master (root-commit) 1e183c2] adding third.txt
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 third.txt

USER@DESKTOP-7TKVOOD MINGW64 ~/Desktop/elle_coccinelle/learn_git (master)
$ git log
commit 1e183c24ef85e5762dfff0e1b5617bf8ac0438aa (HEAD -> master)
Author: elle_coccinelle <emnaennaceur@gmail.com>
Date:   Fri Aug 8 01:15:08 2025 +0200

    adding third.txt

USER@DESKTOP-7TKVOOD MINGW64 ~/Desktop/elle_coccinelle/learn_git (master)
$ touch fourth.txt

USER@DESKTOP-7TKVOOD MINGW64 ~/Desktop/elle_coccinelle/learn_git (master)
$ git add fourth.txt

USER@DESKTOP-7TKVOOD MINGW64 ~/Desktop/elle_coccinelle/learn_git (master)
$ git commit -m "adding fourth.txt"
[master 0d67e84] adding fourth.txt
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 fourth.txt

USER@DESKTOP-7TKVOOD MINGW64 ~/Desktop/elle_coccinelle/learn_git (master)
$ git rm third.txt
rm 'third.txt'

USER@DESKTOP-7TKVOOD MINGW64 ~/Desktop/elle_coccinelle/learn_git (master)
$ git add .
error: open("third.txt."): No such file or directory
error: unable to index file 'third.txt.'
fatal: adding files failed

USER@DESKTOP-7TKVOOD MINGW64 ~/Desktop/elle_coccinelle/learn_git (master)
$ git commit -m "removing third.txt"
[master b767bd4] removing third.txt
 1 file changed, 0 insertions(+), 0 deletions(-)
 delete mode 100644 third.txt

USER@DESKTOP-7TKVOOD MINGW64 ~/Desktop/elle_coccinelle/learn_git (master)
$ git log.
git: 'log.' is not a git command. See 'git --help'.

The most similar command is
        log

USER@DESKTOP-7TKVOOD MINGW64 ~/Desktop/elle_coccinelle/learn_git (master)
$ git log .
commit b767bd4d6af21ab8a3e91b6f9774ebc3314198c1 (HEAD -> master)
Author: elle_coccinelle <emnaennaceur@gmail.com>
Date:   Fri Aug 8 01:19:21 2025 +0200

    removing third.txt

commit 0d67e8469e838c7c7a0e638fdc6ae90d2d86089c
Author: elle_coccinelle <emnaennaceur@gmail.com>
Date:   Fri Aug 8 01:17:30 2025 +0200

    adding fourth.txt

commit 1e183c24ef85e5762dfff0e1b5617bf8ac0438aa
Author: elle_coccinelle <emnaennaceur@gmail.com>
Date:   Fri Aug 8 01:15:08 2025 +0200

    adding third.txt

USER@DESKTOP-7TKVOOD MINGW64 ~/Desktop/elle_coccinelle/learn_git (master)
$ git config --global core.pager "cut"

USER@DESKTOP-7TKVOOD MINGW64 ~/Desktop/elle_coccinelle/learn_git (master)
$ git config --global --list
cut: you must specify a list of bytes, characters, or fields
Try 'cut --help' for more information.

USER@DESKTOP-7TKVOOD MINGW64 ~/Desktop/elle_coccinelle/learn_git (master)
$ cut -help
cut: unknown option -- h
Try 'cut --help' for more information.

USER@DESKTOP-7TKVOOD MINGW64 ~/Desktop/elle_coccinelle/learn_git (master)
$ cut -help
cut: unknown option -- h
Try 'cut --help' for more information.

USER@DESKTOP-7TKVOOD MINGW64 ~/Desktop/elle_coccinelle/learn_git (master)
$ cut --help
Usage: cut OPTION... [FILE]...
Print selected parts of lines from each FILE to standard output.

With no FILE, or when FILE is -, read standard input.

Mandatory arguments to long options are mandatory for short options too.
  -b, --bytes=LIST        select only these bytes
  -c, --characters=LIST   select only these characters
  -d, --delimiter=DELIM   use DELIM instead of TAB for field delimiter
  -f, --fields=LIST       select only these fields;  also print any line
                            that contains no delimiter character, unless
                            the -s option is specified
  -n                      (ignored)
      --complement        complement the set of selected bytes, characters
                            or fields
  -s, --only-delimited    do not print lines not containing delimiters
      --output-delimiter=STRING  use STRING as the output delimiter
                            the default is to use the input delimiter
  -z, --zero-terminated    line delimiter is NUL, not newline
      --help     display this help and exit
      --version  output version information and exit

Use one, and only one of -b, -c or -f.  Each LIST is made up of one
range, or many ranges separated by commas.  Selected input is written
in the same order that it is read, and is written exactly once.
Each range is one of:

  N     N'th byte, character or field, counted from 1
  N-    from N'th byte, character or field, to end of line
  N-M   from N'th to M'th (included) byte, character or field
  -M    from first to M'th (included) byte, character or field

GNU coreutils online help: <https://www.gnu.org/software/coreutils/>
Report any translation bugs to <https://translationproject.org/team/>
Full documentation <https://www.gnu.org/software/coreutils/cut>
or available locally via: info '(coreutils) cut invocation'

USER@DESKTOP-7TKVOOD MINGW64 ~/Desktop/elle_coccinelle/learn_git (master)
$ git config --global --list
cut: you must specify a list of bytes, characters, or fields
Try 'cut --help' for more information.

USER@DESKTOP-7TKVOOD MINGW64 ~/Desktop/elle_coccinelle/learn_git (master)
$ git config --global core.pager cut

USER@DESKTOP-7TKVOOD MINGW64 ~/Desktop/elle_coccinelle/learn_git (master)
$ git config --global --list
cut: you must specify a list of bytes, characters, or fields
Try 'cut --help' for more information.

USER@DESKTOP-7TKVOOD MINGW64 ~/Desktop/elle_coccinelle/learn_git (master)
$ ~ / .gitconfig
bash: /c/Users/USER: Is a directory

USER@DESKTOP-7TKVOOD MINGW64 ~/Desktop/elle_coccinelle/learn_git (master)
$ git push
fatal: No configured push destination.
Either specify the URL from the command-line or configure a remote repository using

    git remote add <name> <url>

and then push using the remote name

    git push <name>


USER@DESKTOP-7TKVOOD MINGW64 ~/Desktop/elle_coccinelle/learn_git (master)
$ git remote add first-repo https://github.com/elle_coccinelle/first repo.git
usage: git remote add [<options>] <name> <url>

    -f, --[no-]fetch      fetch the remote branches
    --[no-]tags           import all tags and associated objects when fetching
                          or do not fetch any tag at all (--no-tags)
    -t, --[no-]track <branch>
                          branch(es) to track
    -m, --[no-]master <branch>
                          master branch
    --[no-]mirror[=(push|fetch)]
                          set up remote as a mirror to push to or fetch from


USER@DESKTOP-7TKVOOD MINGW64 ~/Desktop/elle_coccinelle/learn_git (master)
$ git remote add first-repo https://github.com/elle_coccinelle/first-repo.git

USER@DESKTOP-7TKVOOD MINGW64 ~/Desktop/elle_coccinelle/learn_git (master)
$ git push origin main
error: src refspec main does not match any
error: failed to push some refs to 'origin'

USER@DESKTOP-7TKVOOD MINGW64 ~/Desktop/elle_coccinelle/learn_git (master)
$ git add .
error: open("third.txt."): No such file or directory
error: unable to index file 'third.txt.'
fatal: adding files failed

USER@DESKTOP-7TKVOOD MINGW64 ~/Desktop/elle_coccinelle/learn_git (master)
$ git commit -m "wanna push"
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        third.txt.

nothing added to commit but untracked files present (use "git add" to track)

USER@DESKTOP-7TKVOOD MINGW64 ~/Desktop/elle_coccinelle/learn_git (master)
$ git add
Nothing specified, nothing added.
hint: Maybe you wanted to say 'git add .'?
hint: Disable this message with "git config set advice.addEmptyPathspec false"

USER@DESKTOP-7TKVOOD MINGW64 ~/Desktop/elle_coccinelle/learn_git (master)
$ git add .
error: open("third.txt."): No such file or directory
error: unable to index file 'third.txt.'
fatal: adding files failed

USER@DESKTOP-7TKVOOD MINGW64 ~/Desktop/elle_coccinelle/learn_git (master)
$ git push -u first-repo main
error: src refspec main does not match any
error: failed to push some refs to 'https://github.com/elle_coccinelle/first-repo.git'

USER@DESKTOP-7TKVOOD MINGW64 ~/Desktop/elle_coccinelle/learn_git (master)
$ git remote add first-repo https://github.com/elle-coccinelle/first repo.git
usage: git remote add [<options>] <name> <url>

    -f, --[no-]fetch      fetch the remote branches
    --[no-]tags           import all tags and associated objects when fetching
                          or do not fetch any tag at all (--no-tags)
    -t, --[no-]track <branch>
                          branch(es) to track
    -m, --[no-]master <branch>
                          master branch
    --[no-]mirror[=(push|fetch)]
                          set up remote as a mirror to push to or fetch from


USER@DESKTOP-7TKVOOD MINGW64 ~/Desktop/elle_coccinelle/learn_git (master)
$ git push -u first-repo main
error: src refspec main does not match any
error: failed to push some refs to 'https://github.com/elle_coccinelle/first-repo.git'

USER@DESKTOP-7TKVOOD MINGW64 ~/Desktop/elle_coccinelle/learn_git (master)
$
