# Part 1

## 1.1
~~~~
[janne@Janne-Thinkpad ~]$ docker container ps -a
CONTAINER ID        IMAGE               COMMAND                  CREATED             STATUS                       PORTS               NAMES
2d197bb54d9a        nginx               "nginx -g 'daemon of…"   5 minutes ago       Exited (137) 4 minutes ago                       optimistic_lewin
aaa770dcc14e        nginx               "nginx -g 'daemon of…"   5 minutes ago       Exited (137) 4 minutes ago                       reverent_mayer
2308a48b6d90        nginx               "nginx -g 'daemon of…"   5 minutes ago       Up 5 minutes                 80/tcp              youthful_lovelace
~~~~

## 1.2
~~~~
[janne@Janne-Thinkpad ~]$ docker ps -a
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES
[janne@Janne-Thinkpad ~]$ docker images
REPOSITORY          TAG                 IMAGE ID            CREATED             SIZE
[janne@Janne-Thinkpad ~]$ 
~~~~

## 1.3
~~~~
[janne@Janne-Thinkpad part1]$ docker run -it devopsdockeruh/pull_exercise
Unable to find image 'devopsdockeruh/pull_exercise:latest' locally
latest: Pulling from devopsdockeruh/pull_exercise
8e402f1a9c57: Pull complete 
5e2195587d10: Pull complete 
6f595b2fc66d: Pull complete 
165f32bf4e94: Pull complete 
67c4f504c224: Pull complete 
Digest: sha256:7c0635934049afb9ca0481fb6a58b16100f990a0d62c8665b9cfb5c9ada8a99f
Status: Downloaded newer image for devopsdockeruh/pull_exercise:latest
Give me the password: basics
You found the correct password. Secret message is:
"This is the secret message"
~~~~

## 1.4

~~~~
[janne@Janne-Thinkpad part1]$ docker run --detach devopsdockeruh/exec_bash_exercise
Unable to find image 'devopsdockeruh/exec_bash_exercise:latest' locally
latest: Pulling from devopsdockeruh/exec_bash_exercise
741437d97401: Pull complete 
34d8874714d7: Pull complete 
0a108aa26679: Pull complete 
7f0334c36886: Pull complete 
65c95cb8b3be: Pull complete 
a36b708560f8: Pull complete 
4090f912e6c7: Pull complete 
ce5fe2607c2e: Pull complete 
9400f5f657d6: Pull complete 
c4919883f7fa: Pull complete 
Digest: sha256:c463832132d1fb0b8b3b60348a6fc36fda7512a4ef2d1050e8bea7b6a6d7a2f3
Status: Downloaded newer image for devopsdockeruh/exec_bash_exercise:latest
d946b92a0db44d08fe844d465b7ca54371920a1ab32f89c97cb332bd4a3335c1
[janne@Janne-Thinkpad part1]$ docker exec -it d946b92a0db4 tail -f ./logs.txt
Thu, 23 May 2019 12:05:26 GMT
Thu, 23 May 2019 12:05:29 GMT
Thu, 23 May 2019 12:05:32 GMT
Thu, 23 May 2019 12:05:35 GMT
Secret message is:
"Docker is easy"
Thu, 23 May 2019 12:05:41 GMT
Thu, 23 May 2019 12:05:44 GMT
Thu, 23 May 2019 12:05:47 GMT
Thu, 23 May 2019 12:05:50 GMT
Secret message is:
"Docker is easy"
Thu, 23 May 2019 12:05:56 GMT
~~~~

## 1.5

~~~~
[janne@Janne-Thinkpad ~]$ docker run -it ubuntu
root@c51e9e04dad1:/# apt-get update
.........
root@c51e9e04dad1:/# apt-get install curl  
.........
root@c51e9e04dad1:/# exit
[janne@Janne-Thinkpad ~]$ docker container ls -a
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS                      PORTS               NAMES
c51e9e04dad1        ubuntu              "/bin/bash"         3 minutes ago       Exited (0) 42 seconds ago                       blissful_torvalds
[janne@Janne-Thinkpad ~]$ docker start c51e9e04dad1
c51e9e04dad1
[janne@Janne-Thinkpad ~]$ docker exec -it c51e9e04dad1 sh -c 'echo "Input website:"; read website; echo "Searching.."; sleep 1; curl http://$website;'
Input website:
helsinki.fi
Searching..
<!DOCTYPE HTML PUBLIC "-//IETF//DTD HTML 2.0//EN">
<html><head>
<title>301 Moved Permanently</title>
</head><body>
<h1>Moved Permanently</h1>
<p>The document has moved <a href="http://www.helsinki.fi/">here</a>.</p>
</body></html>
~~~~
