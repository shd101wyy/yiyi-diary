---
created: 2021-02-15T14:27:37.734Z
modified: 2021-02-15T14:27:55.141Z
---

#ssh 的 `Host key verification failed` 解决方案: https://askubuntu.com/questions/45679/ssh-connection-problem-with-host-key-verification-failed-error

```bash
$ ssh -o StrictHostKeyChecking=no user@something.example.com uptime
```