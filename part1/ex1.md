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
