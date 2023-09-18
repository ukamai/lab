# Отчет по лабораторной работе № 1 по курсу "Фундаментальная информатика"
## Студент группы М8О-108Б-23 Фролов Вячеслав Витальевич

Работа выполнена

Преподаватель: каф. 806 Севастьянов Виктор Сергеевич

1. Тема: Создание Репозитория

2. Цель работы: Создать и подключить репозиторий


3. Протокол: 
```
Welcome to Ubuntu 22.04.2 LTS (GNU/Linux 5.15.90.1-microsoft-standard-WSL2 x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage


This message is shown once a day. To disable it please create the
/home/uka/.hushlogin file.
uka@LAPTOP-RHQOJ899:~$ git clone https://github.com/ukamai/test.git
Cloning into 'test'...
warning: You appear to have cloned an empty repository.
uka@LAPTOP-RHQOJ899:~$ echo "# test" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/ukamai/test.git
git push -u origin main
Reinitialized existing Git repository in /home/uka/.git/
[main bfca26e] first commit
 1 file changed, 1 insertion(+)
error: remote origin already exists.
Password for 'https://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@github.com':
remote: Support for password authentication was removed on August 13, 2021.
remote: Please see https://docs.github.com/en/get-started/getting-started-with-git/about-remote-repositories#cloning-with-https-urls for information on currently recommended modes of authentication.
fatal: Authentication failed for 'https://github.com/ukamai/homework.git/'
uka@LAPTOP-RHQOJ899:~$ git remote add origin https://github.com/ukamai/test.git
git branch -M main
git push -u origin main
error: remote origin already exists.
Password for 'https://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@github.com':
remote: Support for password authentication was removed on August 13, 2021.
remote: Please see https://docs.github.com/en/get-started/getting-started-with-git/about-remote-repositories#cloning-with-https-urls for information on currently recommended modes of authentication.
fatal: Authentication failed for 'https://github.com/ukamai/homework.git/'
uka@LAPTOP-RHQOJ899:~$ git remote add origin https://github.com/ukamai/test.git
error: remote origin already exists.
uka@LAPTOP-RHQOJ899:~$ git push -u origin main
Password for 'https://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@github.com':
remote: Support for password authentication was removed on August 13, 2021.
remote: Please see https://docs.github.com/en/get-started/getting-started-with-git/about-remote-repositories#cloning-with-https-urls for information on currently recommended modes of authentication.
fatal: Authentication failed for 'https://github.com/ukamai/homework.git/'
uka@LAPTOP-RHQOJ899:~$ git push -u origin main
Password for 'https://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@github.com':
remote: Support for password authentication was removed on August 13, 2021.
remote: Please see https://docs.github.com/en/get-started/getting-started-with-git/about-remote-repositories#cloning-with-https-urls for information on currently recommended modes of authentication.
fatal: Authentication failed for 'https://github.com/ukamai/homework.git/'
uka@LAPTOP-RHQOJ899:~$ git push -u origin main
Password for 'https://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@github.com':
remote: Support for password authentication was removed on August 13, 2021.
remote: Please see https://docs.github.com/en/get-started/getting-started-with-git/about-remote-repositories#cloning-with-https-urls for information on currently recommended modes of authentication.
fatal: Authentication failed for 'https://github.com/ukamai/homework.git/'
uka@LAPTOP-RHQOJ899:~$ git push -u origin main
Password for 'https://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@github.com':
To https://github.com/ukamai/homework.git
 ! [rejected]        main -> main (fetch first)
error: failed to push some refs to 'https://github.com/ukamai/homework.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
uka@LAPTOP-RHQOJ899:~$ git fetch
remote: Enumerating objects: 47, done.
remote: Counting objects: 100% (47/47), done.
remote: Compressing objects: 100% (32/32), done.
remote: Total 45 (delta 7), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (45/45), 11.81 KiB | 310.00 KiB/s, done.
From https://github.com/ukamai/homework
   aacb5c2..eead5be  main       -> origin/main
uka@LAPTOP-RHQOJ899:~$ git push -u origin main
Password for 'https://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@github.com':
To https://github.com/ukamai/homework.git
 ! [rejected]        main -> main (non-fast-forward)
error: failed to push some refs to 'https://github.com/ukamai/homework.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. Integrate the remote changes (e.g.
hint: 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
uka@LAPTOP-RHQOJ899:~$ git push -u origin main
Password for 'https://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@github.com':
To https://github.com/ukamai/homework.git
 ! [rejected]        main -> main (non-fast-forward)
error: failed to push some refs to 'https://github.com/ukamai/homework.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. Integrate the remote changes (e.g.
hint: 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
uka@LAPTOP-RHQOJ899:~$ git push -uf origin main
Password for 'https://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@github.com':
Enumerating objects: 11, done.
Counting objects: 100% (11/11), done.
Delta compression using up to 8 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (9/9), 722 bytes | 240.00 KiB/s, done.
Total 9 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/ukamai/homework.git
 + eead5be...bfca26e main -> main (forced update)
Branch 'main' set up to track remote branch 'main' from 'origin'.
uka@LAPTOP-RHQOJ899:~$ git repo list -L 10
git: 'repo' is not a git command. See 'git --help'.

The most similar commands are
        grep
        reflog
        remote
        repack
uka@LAPTOP-RHQOJ899:~$ gh repo
Command 'gh' not found, but can be installed with:
sudo snap install gh       # version 2.6.0-15-g1a10fd5a, or
sudo apt  install gh       # version 2.4.0+dfsg1-2
sudo apt  install gitsome  # version 0.8.0+ds-6ubuntu1
See 'snap info gh' for additional versions.
uka@LAPTOP-RHQOJ899:~$ git reset --hard @{u}
HEAD is now at bfca26e first commit
uka@LAPTOP-RHQOJ899:~$ echo "# lab" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/ukamai/lab.git
git push -u origin main
Reinitialized existing Git repository in /home/uka/.git/
[main be03793] first commit
 1 file changed, 1 insertion(+)
error: remote origin already exists.
Password for 'https://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@github.com':
remote: Repository not found.
fatal: repository 'https://github.com/ukamai/homework.git/' not found
uka@LAPTOP-RHQOJ899:~$ git push -uf origin main
Password for 'https://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@github.com':
remote: Repository not found.
fatal: repository 'https://github.com/ukamai/homework.git/' not found
uka@LAPTOP-RHQOJ899:~$ mkdir
mkdir: missing operand
Try 'mkdir --help' for more information.
uka@LAPTOP-RHQOJ899:~$ ls
README.md  python  test
uka@LAPTOP-RHQOJ899:~$ mkdir github
uka@LAPTOP-RHQOJ899:~$ ls
README.md  github  python  test
uka@LAPTOP-RHQOJ899:~$ cd github
uka@LAPTOP-RHQOJ899:~/github$ echo "# lab" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/ukamai/lab.git
git push -u origin main
hint: Using 'master' as the name for the initial branch. This default branch name
hint: is subject to change. To configure the initial branch name to use in all
hint: of your new repositories, which will suppress this warning, call:
hint:
hint:   git config --global init.defaultBranch <name>
hint:
hint: Names commonly chosen instead of 'master' are 'main', 'trunk' and
hint: 'development'. The just-created branch can be renamed via this command:
hint:
hint:   git branch -m <name>
Initialized empty Git repository in /home/uka/github/.git/
[master (root-commit) 74e0431] first commit
 1 file changed, 1 insertion(+)
 create mode 100644 README.md
Username for 'https://github.com': ukamai
Password for 'https://ukamai@github.com':
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 222 bytes | 222.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/ukamai/lab.git
 * [new branch]      main -> main
Branch 'main' set up to track remote branch 'main' from 'origin'.
uka@LAPTOP-RHQOJ899:~/github$
```
4. Выводы: я изучил как работает github и считаю, что умение с ним работать поможет мне в дальнейшем обучении и в будущей работе. 
