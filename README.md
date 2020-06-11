# Atlassian Jira Software

Atlassian Jira Software, image is based on the Alpine base image with 0 vulnerabilities.

## Current Docker image (~779MB)

Security scanning using Clair
```
clair-scanner secureimages/jira-software:8.9.0-alpine-3.12.0
2020/06/11 13:14:07 [INFO] ▶ Start clair-scanner
2020/06/11 13:14:19 [INFO] ▶ Server listening on port 9279
2020/06/11 13:14:19 [INFO] ▶ Analyzing 76de98d374759ed05698adec9aa042db7bc0f62c25fb612c0f9be1419a581421
2020/06/11 13:14:19 [INFO] ▶ Analyzing 802ea3382a22d128f605aa00d4ee3394447644a7e9fbd890b698c18bb85be70a
2020/06/11 13:14:19 [INFO] ▶ Analyzing 4f258daee546a8b66dc61d325219740ad28be72137bae9c2f59bac83617aa29c
2020/06/11 13:14:19 [INFO] ▶ Analyzing 959c6915107576a4ed44d09ac568a27eb91965e94be0ad0bc3dc431be0451e4c
2020/06/11 13:14:19 [INFO] ▶ Analyzing 1d12fcdf29f47f2ea9b7ed7b50bd4fedfb7ed74f465a9ea44bceb0bbceb73064
2020/06/11 13:14:21 [INFO] ▶ Analyzing 8749d1730d97f8b86939600275398dac02d45340e12a3084faee80c15a3b7d04
2020/06/11 13:14:21 [INFO] ▶ Analyzing 120a63b3ad61073ebb845ac409ab2fddfc8b5aea3bcb121c55e521086e0f6d5e
2020/06/11 13:14:21 [INFO] ▶ Image [secureimages/jira-software:8.9.0-alpine-3.12.0] contains NO unapproved vulnerabilities
```

Security scanning using Trivy
```
docker run --rm -v /var/run/docker.sock:/var/run/docker.sock:ro aquasec/trivy:0.9.1 --no-progress secureimages/jira-software:8.9.0-alpine-3.12.0
2020-06-11T10:14:23.967Z        INFO    Need to update DB
2020-06-11T10:14:23.967Z        INFO    Downloading DB...
2020-06-11T10:14:40.477Z        INFO    Detecting Alpine vulnerabilities...

secureimages/jira-software:8.9.0-alpine-3.12.0 (alpine 3.12.0)
==============================================================
Total: 0 (UNKNOWN: 0, LOW: 0, MEDIUM: 0, HIGH: 0, CRITICAL: 0)
```

## Official Docker image (~795MB)

[https://hub.docker.com/r/atlassian/jira-software](https://hub.docker.com/r/atlassian/jira-software)
```
docker pull atlassian/jira-software:8.9.0
```

Security scanning using Clair
```
clair-scanner atlassian/jira-software:8.9.0
2020/06/11 13:14:48 [INFO] ▶ Start clair-scanner
2020/06/11 13:15:03 [INFO] ▶ Server listening on port 9279
2020/06/11 13:15:03 [INFO] ▶ Analyzing 6ef5a7b6cc6da3fe4489191c166763832ff732b6c346e7d77a2dbbd3e89a9f08
2020/06/11 13:15:03 [INFO] ▶ Analyzing c774328901d4a9ee5201de46d502b8f56f9b6a5d21c64affa6ca96d3b69cfe68
2020/06/11 13:15:03 [INFO] ▶ Analyzing 67b382b86062872cc280027bfb3cc103cba4e52bb66d23c590e0cb8647dd39fe
2020/06/11 13:15:03 [INFO] ▶ Analyzing 4e0bca968c343d4488ae5b156e0b4a6630a6964bd401264b3fe9060a266f4ce7
2020/06/11 13:15:03 [INFO] ▶ Analyzing 33db261f08cfde61ed408a1688df09cec342cfc8e55dfcf32818a7b0418814f5
2020/06/11 13:15:03 [INFO] ▶ Analyzing 48aac7f877504db33ba7c4f499dc97cb249d21ca4a9912ecbf512e8f81a142ca
2020/06/11 13:15:03 [INFO] ▶ Analyzing 078b58b864f2bc7460386982ce901edda04de3e5f9a23b69c6884cda510c60fb
2020/06/11 13:15:03 [INFO] ▶ Analyzing f901d666453e2e6a41a77623768c0b35e52660470f466a593d5a28172b1aa2e8
2020/06/11 13:15:03 [INFO] ▶ Analyzing 33dc4d94b159ed71f82ae33a9facbdc982ecc0721b2ea1c8e8c261e81b625dab
2020/06/11 13:15:03 [INFO] ▶ Analyzing 12516fb586c682b3510f2ef4574fe3a88dfe177eed1669f10c62706445475029
2020/06/11 13:15:03 [INFO] ▶ Analyzing 23d6b2aa2afe375db18ae408de152899a9fc423f37703c06ed33b7b9f000602d
2020/06/11 13:15:03 [INFO] ▶ Analyzing ebef1b8865c66667377a2f84c25cdef61a9b25cd1a588c62bac440e1b36c1224
2020/06/11 13:15:03 [INFO] ▶ Analyzing d765c90a32f3f844ed9f4b76885868c0b5dfd3c1187e3fabc52010d9dffaf782
2020/06/11 13:15:03 [INFO] ▶ Analyzing 599f6c540fb48b5ef787c375894a302df0186e51aa1b540f26c48745389e0e62
2020/06/11 13:15:03 [WARN] ▶ Image [atlassian/jira-software:8.9.0] contains 49 total vulnerabilities
2020/06/11 13:15:03 [ERRO] ▶ Image [atlassian/jira-software:8.9.0] contains 49 unapproved vulnerabilities
```

Security scanning using Trivy
```
docker run --rm -v /var/run/docker.sock:/var/run/docker.sock:ro aquasec/trivy:0.9.1 --no-progress atlassian/jira-software:8.9.0
2020-06-11T10:15:07.493Z        INFO    Need to update DB
2020-06-11T10:15:07.493Z        INFO    Downloading DB...
2020-06-11T10:15:25.775Z        INFO    Detecting Ubuntu vulnerabilities...

atlassian/jira-software:8.9.0 (ubuntu 18.04)
============================================
Total: 110 (UNKNOWN: 0, LOW: 83, MEDIUM: 27, HIGH: 0, CRITICAL: 0)
```
