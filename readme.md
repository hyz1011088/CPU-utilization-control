# CPU Utilization control in linux

## method1：

####. step

   use the commond of linux:

1. install cpulimit

   in root state
   ubuntu/debian:
```
sudo su
apt-get install cpulimit

```
   centos/redhat:
```
sudo su
apt-get install cpulimit

```

2. use cpulimit to limit the pid or programm

   in user state

```
cpulimit -e firefox -l 30

```
   or:
```
cpulimit -p 2783 -l 30

```

####. tag:

1. how to get the pid:

```
ps aux | less
ps aux | grep firefox
pgrep -u vivek php-cgi
pgrep lighttpd

```
   or use the absolute path:

```
cpulimit -P /opt/firefox/firebox -l 30

```

2. one core or mulitcore:

   one core limit: 0-100
   four core limit: 0-400
