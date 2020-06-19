# Atlassian Jira Software

Atlassian Jira Software, image is based on the Alpine base image with 0 vulnerabilities.

## Current Docker image (~779MB)

Security scanning using Clair
```
clair-scanner secureimages/jira-software:8.9.1-alpine-3.12.0
2020/06/19 20:50:59 [INFO] ▶ Start clair-scanner
2020/06/19 20:51:07 [INFO] ▶ Server listening on port 9279
2020/06/19 20:51:07 [INFO] ▶ Analyzing 76de98d374759ed05698adec9aa042db7bc0f62c25fb612c0f9be1419a581421
2020/06/19 20:51:07 [INFO] ▶ Analyzing 46c07c098a20d8db163765e3d6bac4105714822f1c824da71347ce2f7873f8d0
2020/06/19 20:51:08 [INFO] ▶ Analyzing b46a4d052416d533a9f7bdd6fb6d21ccc1ca38075564fbce6ce9ef175929b286
2020/06/19 20:51:09 [INFO] ▶ Analyzing 321fa6f0ef138a3c6a96ac19a6d14b2c3a2bc3ad35e6314a9897ae0a911dada3
2020/06/19 20:51:09 [INFO] ▶ Analyzing ab661c5eeb86c81af2a1c06d5298eda18dbe22a7bfe275c77a2b319dbe366492
2020/06/19 20:51:09 [INFO] ▶ Analyzing d1d61652f74b1f9c12a8753b876601180e721be06fdd6acd0db67a05de71b000
2020/06/19 20:51:09 [INFO] ▶ Analyzing fd621ae65b3ae20f492e236e53c651b8caf1f6149e4541b440401f60ce18d7bb
2020/06/19 20:51:10 [INFO] ▶ Image [secureimages/jira-software:8.9.1-alpine-3.12.0] contains NO unapproved vulnerabilities
```

Security scanning using Trivy
```
docker run --rm -v /var/run/docker.sock:/var/run/docker.sock:ro aquasec/trivy:0.9.1 --no-progress secureimages/jira-software:8.9.1-alpine-3.12.0
2020-06-19T17:51:12.427Z        INFO    Need to update DB
2020-06-19T17:51:12.427Z        INFO    Downloading DB...
2020-06-19T17:51:28.698Z        INFO    Detecting Alpine vulnerabilities...

secureimages/jira-software:8.9.1-alpine-3.12.0 (alpine 3.12.0)
==============================================================
Total: 0 (UNKNOWN: 0, LOW: 0, MEDIUM: 0, HIGH: 0, CRITICAL: 0)
```

## Official Docker image (~796MB)

[https://hub.docker.com/r/atlassian/jira-software](https://hub.docker.com/r/atlassian/jira-software)
```
docker pull atlassian/jira-software:8.9.1
```

Security scanning using Clair
```
clair-scanner atlassian/jira-software:8.9.1
2020/06/19 20:51:34 [INFO] ▶ Start clair-scanner
2020/06/19 20:51:48 [INFO] ▶ Server listening on port 9279
2020/06/19 20:51:48 [INFO] ▶ Analyzing 6ef5a7b6cc6da3fe4489191c166763832ff732b6c346e7d77a2dbbd3e89a9f08
2020/06/19 20:51:48 [INFO] ▶ Analyzing c774328901d4a9ee5201de46d502b8f56f9b6a5d21c64affa6ca96d3b69cfe68
2020/06/19 20:51:48 [INFO] ▶ Analyzing 67b382b86062872cc280027bfb3cc103cba4e52bb66d23c590e0cb8647dd39fe
2020/06/19 20:51:48 [INFO] ▶ Analyzing 4e0bca968c343d4488ae5b156e0b4a6630a6964bd401264b3fe9060a266f4ce7
2020/06/19 20:51:48 [INFO] ▶ Analyzing 33db261f08cfde61ed408a1688df09cec342cfc8e55dfcf32818a7b0418814f5
2020/06/19 20:51:48 [INFO] ▶ Analyzing 48aac7f877504db33ba7c4f499dc97cb249d21ca4a9912ecbf512e8f81a142ca
2020/06/19 20:51:48 [INFO] ▶ Analyzing 1ddbc9495db9207ef90a28781101e32e4a1720d6189fafc31c8c166588fcdd1d
2020/06/19 20:51:48 [INFO] ▶ Analyzing 5858693005397036a36f83559303eb45f7886429d8707e487ea68e123d8f11b6
2020/06/19 20:51:49 [INFO] ▶ Analyzing 6141c75ec130f723736b4df82d45eb14d19af4b7c82ae7b6dbeaf2cf9de2cbd4
2020/06/19 20:51:49 [INFO] ▶ Analyzing 48d230f677859c4c37ea67c7b0c0333ce9f255792194179994704a13b7029f69
2020/06/19 20:51:49 [INFO] ▶ Analyzing f695450cbd8bf72420b3a6ed91861b6b8670bd181be62e1d3933bdd42742cfd6
2020/06/19 20:51:49 [INFO] ▶ Analyzing f387e89e96c124a81f4e1d2b61511883bb72f1344e9b180e5f4e751702f368c2
2020/06/19 20:51:49 [INFO] ▶ Analyzing e887cca0ff3af02ca2200958feffb898964f4c2cb7de4ec0cb4c80bab66c4146
2020/06/19 20:51:49 [INFO] ▶ Analyzing 52e2c659cdfe4fbd3b6b40981e5159d68c8133a31a56d9d7e37bddf8454fbe3c
2020/06/19 20:51:49 [WARN] ▶ Image [atlassian/jira-software:8.9.1] contains 47 total vulnerabilities
2020/06/19 20:51:49 [ERRO] ▶ Image [atlassian/jira-software:8.9.1] contains 47 unapproved vulnerabilities
```

Security scanning using Trivy
```
docker run --rm -v /var/run/docker.sock:/var/run/docker.sock:ro aquasec/trivy:0.9.1 --no-progress atlassian/jira-software:8.9.1
2020-06-19T17:51:51.672Z        INFO    Need to update DB
2020-06-19T17:51:51.672Z        INFO    Downloading DB...
2020-06-19T17:52:09.809Z        INFO    Detecting Ubuntu vulnerabilities...

atlassian/jira-software:8.9.1 (ubuntu 18.04)
============================================
Total: 110 (UNKNOWN: 0, LOW: 80, MEDIUM: 30, HIGH: 0, CRITICAL: 0)
```
