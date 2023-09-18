```

uka@LAPTOP-RHQOJ899:~$ whoiam
whoiam: command not found
uka@LAPTOP-RHQOJ899:~$ who
uka      pts/1        2023-09-18 08:26
uka@LAPTOP-RHQOJ899:~$ pwd
/home/uka
uka@LAPTOP-RHQOJ899:~$ ls
README.md  github  keyholder  keyholder.pub  python
uka@LAPTOP-RHQOJ899:~$ rm keyholder
uka@LAPTOP-RHQOJ899:~$ rm keyholder.pub
uka@LAPTOP-RHQOJ899:~$ ls
README.md  github  python
uka@LAPTOP-RHQOJ899:~$ cd
uka@LAPTOP-RHQOJ899:~$ cd ../
uka@LAPTOP-RHQOJ899:/home$ cd
uka@LAPTOP-RHQOJ899:~$ touch testfile.txt
uka@LAPTOP-RHQOJ899:~$ nano testfile.txt
uka@LAPTOP-RHQOJ899:~$ touch locfile
uka@LAPTOP-RHQOJ899:~$ cp testfile.txt -b locfile
uka@LAPTOP-RHQOJ899:~$ tail locfile
1234567890
uka@LAPTOP-RHQOJ899:~$ man mv
uka@LAPTOP-RHQOJ899:~$ touch m
uka@LAPTOP-RHQOJ899:~$ mv testfile.txt -f m
uka@LAPTOP-RHQOJ899:~$ ls
README.md  github  locfile  locfile~  m  python
uka@LAPTOP-RHQOJ899:~$ tail m
1234567890
uka@LAPTOP-RHQOJ899:~$ tail testfile.txt
tail: cannot open 'testfile.txt' for reading: No such file or directory
uka@LAPTOP-RHQOJ899:~$ rm testfile.txt
rm: cannot remove 'testfile.txt': No such file or directory
uka@LAPTOP-RHQOJ899:~$ ls
README.md  github  locfile  locfile~  m  python
uka@LAPTOP-RHQOJ899:~$ tail m
1234567890
uka@LAPTOP-RHQOJ899:~$ rm locfile locfile~
uka@LAPTOP-RHQOJ899:~$ ls
README.md  github  m  python
uka@LAPTOP-RHQOJ899:~$ cat --help
Usage: cat [OPTION]... [FILE]...
Concatenate FILE(s) to standard output.

With no FILE, or when FILE is -, read standard input.

  -A, --show-all           equivalent to -vET
  -b, --number-nonblank    number nonempty output lines, overrides -n
  -e                       equivalent to -vE
  -E, --show-ends          display $ at end of each line
  -n, --number             number all output lines
  -s, --squeeze-blank      suppress repeated empty output lines
  -t                       equivalent to -vT
  -T, --show-tabs          display TAB characters as ^I
  -u                       (ignored)
  -v, --show-nonprinting   use ^ and M- notation, except for LFD and TAB
      --help     display this help and exit
      --version  output version information and exit

Examples:
  cat f - g  Output f's contents, then standard input, then g's contents.
  cat        Copy standard input to standard output.

GNU coreutils online help: <https://www.gnu.org/software/coreutils/>
Report any translation bugs to <https://translationproject.org/team/>
Full documentation <https://www.gnu.org/software/coreutils/cat>
or available locally via: info '(coreutils) cat invocation'
uka@LAPTOP-RHQOJ899:~$ cat -A m
1234567890$
uka@LAPTOP-RHQOJ899:~$ ps --help

Usage:
 ps [options]

 Try 'ps --help <simple|list|output|threads|misc|all>'
  or 'ps --help <s|l|o|t|m|a>'
 for additional help text.

For more details see ps(1).
uka@LAPTOP-RHQOJ899:~$ ps m
    PID TTY      STAT   TIME COMMAND
    360 pts/0    -      0:01 -bash
      - -        Ss     0:01 -
    425 pts/1    -      0:00 -bash
      - -        S+     0:00 -
   1087 pts/0    -      0:00 ps m
      - -        R+     0:00 -
uka@LAPTOP-RHQOJ899:~$ tail m
1234567890
uka@LAPTOP-RHQOJ899:~$ nano m
uka@LAPTOP-RHQOJ899:~$ sudo ls -l
[sudo] password for uka:
total 16
-rw-r--r-- 1 uka uka   58 Sep 18 08:58 README.md
drwxr-xr-x 3 uka uka 4096 Sep 18 09:54 github
-rw-r--r-- 1 uka uka   34 Sep 18 11:42 m
drwxr-xr-x 4 uka uka 4096 Sep 18 10:01 python
uka@LAPTOP-RHQOJ899:~$ head -n m
^C
uka@LAPTOP-RHQOJ899:~$ head m -n1
1234567890
uka@LAPTOP-RHQOJ899:~$ tail m
1234567890
234235
547464
6785670

uka@LAPTOP-RHQOJ899:~$ head m -n2
1234567890
234235
uka@LAPTOP-RHQOJ899:~$ grep m 3
grep: 3: No such file or directory
uka@LAPTOP-RHQOJ899:~$ grep 3 m
1234567890
234235
uka@LAPTOP-RHQOJ899:~$ history
    1  history
    2  grep 123
    3  ls
    4  nano file txt
    5  tail file
    6  tail file.txt
    7  ls
    8  rm file
    9  touch file.py
   10  ls
   11  nano file.py
   12  cat file.py
   13  python3
   14  python3 file.py
   15  ls
   16  rm file.py file.txt
   17  ls
   18  sudo ls -l
   19  ls -l
   20  echo 123
   21  echo 11
   22  echo 1
   23  ls
   24  ssh root@185.5.249.140
   25  ls
   26  ssh <ukamai>@185.5.249.140
   27  ssh-keygen
   28  ssh-copy-id
   29  ssh-copy-id root@185.5.249.140
   30  ssh ukamai@185.5.249.140
   31  pwd
   32  ssh ukamai@185.5.249.140
   33  ssh v_frolov@185.5.249.140
   34  ssh-copy-id v_frolov@185.5.249.140
   35  ls ~/.ssh/
   36  ssh-keygen
   37  ssh-copy-id v_frolov@185.5.249.140
   38  ssh v_frolov@185.5.249.140
   39  clear
   40  whoiam
   41  who
   42  pwd
   43  ls
   44  rm keyholder
   45  rm keyholder.pub
   46  ls
   47  cd
   48  cd ../
   49  cd
   50  touch testfile.txt
   51  nano testfile.txt
   52  touch locfile
   53  cp testfile.txt -b locfile
   54  tail locfile
   55  man mv
   56  touch m
   57  mv testfile.txt -f m
   58  ls
   59  tail m
   60  tail testfile.txt
   61  rm testfile.txt
   62  ls
   63  tail m
   64  rm locfile locfile~
   65  ls
   66  cat --help
   67  cat -A m
   68  ps --help
   69  ps m
   70  tail m
   71  nano m
   72  sudo ls -l
   73  head -n m
   74  head m -n1
   75  tail m
   76  head m -n2
   77  grep m 3
   78  grep 3 m
   79  history
uka@LAPTOP-RHQOJ899:~$ mkdir tup
uka@LAPTOP-RHQOJ899:~$ ls
README.md  github  m  python  tup
uka@LAPTOP-RHQOJ899:~$ rmdir tup
uka@LAPTOP-RHQOJ899:~$ rm -f m
uka@LAPTOP-RHQOJ899:~$ ls
README.md  github  python
uka@LAPTOP-RHQOJ899:~$ echo hello
hello
uka@LAPTOP-RHQOJ899:~$ ssh v_frolov@185.5.249.140
Welcome to Ubuntu 20.04.6 LTS (GNU/Linux 5.4.0-162-generic x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage
New release '22.04.3 LTS' available.
Run 'do-release-upgrade' to upgrade to it.

Last login: Mon Sep 18 10:34:44 2023 from 85.143.224.8
v_frolov@vds2476450:~$ touch listing
Could not find command-not-found database. Run 'sudo apt update' to populate it.
ещ�touch: command not found
v_frolov@vds2476450:~$ exit
logout
Connection to 185.5.249.140 closed.
uka@LAPTOP-RHQOJ899:~$ ssh v_frolov@185.5.249.140
Welcome to Ubuntu 20.04.6 LTS (GNU/Linux 5.4.0-162-generic x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage
New release '22.04.3 LTS' available.
Run 'do-release-upgrade' to upgrade to it.

Last login: Mon Sep 18 11:44:52 2023 from 85.143.224.8
v_frolov@vds2476450:~$ exit
logout
Connection to 185.5.249.140 closed.
uka@LAPTOP-RHQOJ899:~$ touch listing
uka@LAPTOP-RHQOJ899:~$ rm listing

```
uka@LAPTOP-RHQOJ899:~$ touch listing.md
uka@LAPTOP-RHQOJ899:~$ nano
