---
created: 2022-03-07T11:14:26.375Z
modified: 2022-03-08T10:21:22.241Z
---
Server:

https://git-scm.com/book/en/v2/Git-on-the-Server-Setting-Up-the-Server

```bash
$ git clone --bare https://github.com/shd101wyy/test-public.git
$ cd test-public
$ git fetch --all -a -p

```


Client:

```bash
$ git clone git@localhost:/home/git/test-public.git
```


---

Server:

```
mkdir -p  ~/Desktop/amp_repos/test-server
cd ~/Desktop/amp_repos/test-server

git init --bare
git remote add origin https://github.com/shd101wyy/test-public.git

git fetch --depth 1 origin f40d6765365fd9fd9915c64e3458e58b9da567e6
git update-ref refs/heads/f40d6765365fd9fd9915c64e3458e58b9da567e6 f40d6765365fd9fd9915c64e3458e58b9da567e6

git fetch --depth 1 origin bf7f0ebebaa18de248dc66afa6b199ba3b9ddf53
git update-ref refs/heads/bf7f0ebebaa18de248dc66afa6b199ba3b9ddf53 bf7f0ebebaa18de248dc66afa6b199ba3b9ddf53
```

Client:

```
git clone yiyiwang@localhost:/home/yiyiwang/Desktop/amp_repos/test-server
cd test-server
```