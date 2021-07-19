# container-docker-2019-docker-in-action-2nd

![](https://img.shields.io/badge/language-bash-blue)
![](https://img.shields.io/badge/technology-docker-blue)
![](https://img.shields.io/badge/development%20year-2020-orange)

![](https://img.shields.io/github/languages/top/shijiansu/container-docker-2019-docker-in-action-2nd)
![](https://img.shields.io/github/languages/count/shijiansu/container-docker-2019-docker-in-action-2nd)
![](https://img.shields.io/github/languages/code-size/shijiansu/container-docker-2019-docker-in-action-2nd)
![](https://img.shields.io/github/repo-size/shijiansu/container-docker-2019-docker-in-action-2nd)
![](https://img.shields.io/github/last-commit/shijiansu/container-docker-2019-docker-in-action-2nd?color=red)

## Outline

- part 1 process isolation and environment independent computing
  - 1 welcome to docker
  - 2 running software in container
  - 3 software installation simplified
  - 4 working with storage and volumes
  - 5 single host networking
  - 6 limiting risk with resource controls
- part 2 packaging software for distribution
  - 7 packaging software in images
  - 8 building images automatically with dockerfiles
  - 9 public and private software distribution
  - 10 image pipelines
- part 3 higher level abstractions and orchestration
  - 11 services with docker and compose
  - 12 first class configuration abstractions
  - 13 orchestrating services on a cluster of docker hosts with swarm

## Lab commands

```bash
# container
docker ps --no-trunc # see all running containers with full info
docker ps --no-trunc -a # see all containers with full info
docker stop $(docker ps -q) # stop all dockers
docker stop ch6_wordpress && docker rm ch6_wordpress # stop and remove
docker container rm -vf ch6_wordpress # forced kill and also clean volumes

# resource
docker system df # show used space, similar to the unix tool df
docker system prune # remove all dangling ((not associated with a container)) resources.
docker system prune -a # remove any stopped containers and all unused images

# service
docker service ls
docker service remove $(docker service ls -q)
```

##  Source code

### Option 1 (version 2019)

```bash
git clone https://github.com/dockerinaction/ch10_patterns-for-building-images.git
git clone https://github.com/dockerinaction/ch3_myotherapp.git
git clone https://github.com/dockerinaction/ch3_myapp.git
git clone https://github.com/dockerinaction/ch6_ipc.git
git clone https://github.com/dockerinaction/ch12_greetings.git
git clone https://github.com/dockerinaction/ch13_multi_tier_app.git
git clone https://github.com/dockerinaction/ch11_coffee_api.git
git clone https://github.com/dockerinaction/ch8_multi_stage_build.git
git clone https://github.com/dockerinaction/materials.git
git clone https://github.com/dockerinaction/ch11_notifications.git
git clone https://github.com/dockerinaction/ch6_stresser.git
git clone https://github.com/dockerinaction/ch6_htop.git
git clone https://github.com/dockerinaction/ch12_coffee_api.git
git clone https://github.com/dockerinaction/ch12_coffee_proxy.git
git clone https://github.com/dockerinaction/ch12_coffee.git
git clone https://github.com/dockerinaction/ch12_painted.git
git clone https://github.com/dockerinaction/ch12_coffee_tests.git
git clone https://github.com/dockerinaction/ch11_wp_environment.git
git clone https://github.com/dockerinaction/ch10_calaca.git
git clone https://github.com/dockerinaction/ch10_webhook_es_pump.git
git clone https://github.com/dockerinaction/ch10_htpasswd.git
git clone https://github.com/dockerinaction/ch10_curl.git
git clone https://github.com/dockerinaction/ch10_webhook_listener.git
git clone https://github.com/dockerinaction/ch9_registry_bound.git
git clone https://github.com/dockerinaction/ch9_ftp_client.git
git clone https://github.com/dockerinaction/ch9_ftpd.git
git clone https://github.com/dockerinaction/ch4_polyapp.git
git clone https://github.com/dockerinaction/ch4_ia.git
git clone https://github.com/dockerinaction/ch4_packed_config.git
git clone https://github.com/dockerinaction/ch4_tools.git
git clone https://github.com/dockerinaction/ch4_packed.git
git clone https://github.com/dockerinaction/ch4_writers.git
git clone https://github.com/dockerinaction/ch3_ex2_huntanswer.git
git clone https://github.com/dockerinaction/ch3_ex2_hunt.git
git clone https://github.com/dockerinaction/ch2_mailer.git
git clone https://github.com/dockerinaction/ch2_agent.git
git clone https://github.com/dockerinaction/ch3_dockerfile.git
git clone https://github.com/dockerinaction/ch3_hello_registry.git
git clone https://github.com/dockerinaction/ch5_expose.git
git clone https://github.com/dockerinaction/ch5_nmap.git
git clone https://github.com/dockerinaction/ch5_ff.git
git clone https://github.com/dockerinaction/busybox.git
git clone https://github.com/dockerinaction/hello_world.git
```

### Option 2 (version 2016)

- https://www.manning.com/books/docker-in-action

## Execute all tests in repo

`/bin/bash run-repo-test.sh`
