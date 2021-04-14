# GIT 04 training

> This page generated for educational perpose, task git04, rebrain devops course


## Usage
1. Clone this ripository using `git clone`:

`git clone [url to repository]`
2. Copy nginx.conf to you nginx conf directory(e.g. /etc/nginx/):

`cp nginx.conf /etc/nginx/`
3. Reload nginx:

`systemctl reload nginx`
4. Check nginx works with new config

`systemctl status nginx`

outputs

```
[root@sb-test-01v ~]# systemctl status nginx
● nginx.service - The nginx HTTP and reverse proxy server
   Loaded: loaded (/usr/lib/systemd/system/nginx.service; disabled; vendor preset: disabled)
   Active: active (running) since Wed 2021-04-14 03:36:01 EDT; 54s ago
  Process: 31031 ExecReload=/bin/kill -s HUP $MAINPID (code=exited, status=0/SUCCESS)
  Process: 31017 ExecStart=/usr/sbin/nginx (code=exited, status=0/SUCCESS)
  Process: 31015 ExecStartPre=/usr/sbin/nginx -t (code=exited, status=0/SUCCESS)
  Process: 31014 ExecStartPre=/usr/bin/rm -f /run/nginx.pid (code=exited, status=0/SUCCESS)
 Main PID: 31019 (nginx)
    Tasks: 2 (limit: 11083)
   Memory: 7.4M
   CGroup: /system.slice/nginx.service
           ├─31019 nginx: master process /usr/sbin/nginx
           └─31034 nginx: worker process

Apr 14 03:36:00 sb-test-01v systemd[1]: Starting The nginx HTTP and reverse proxy server...
Apr 14 03:36:00 sb-test-01v nginx[31015]: nginx: the configuration file /etc/nginx/nginx.conf syntax is ok
Apr 14 03:36:00 sb-test-01v nginx[31015]: nginx: configuration file /etc/nginx/nginx.conf test is successful
Apr 14 03:36:01 sb-test-01v systemd[1]: nginx.service: Failed to parse PID from file /run/nginx.pid: Invalid>
Apr 14 03:36:01 sb-test-01v systemd[1]: Started The nginx HTTP and reverse proxy server.
Apr 14 03:36:08 sb-test-01v systemd[1]: Reloading The nginx HTTP and reverse proxy server.
Apr 14 03:36:08 sb-test-01v systemd[1]: Reloaded The nginx HTTP and reverse proxy server.

```

## Install

On CentOS:

```
yum install nginx -y
```

## Acknowledgments

- [`rebraid devops training`] (https://rebrainme.com/devops/)
- [`guthub documentation`] (https://git-scm.com/book/ru/v2/)

## See Also

- [`noffle/common-readme`](https://github.com/noffle/common-readme)
- [`nginx documentation`](https://nginx.org/ru/docs/)

## License

BSD

