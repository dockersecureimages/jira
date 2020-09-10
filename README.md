# Atlassian Jira Software

Atlassian Jira Software, image is based on the Alpine base image with 0 vulnerabilities.

## Current Docker image (~757MB)

Security scanning using Clair
```
clair-scanner secureimages/jira-software:8.12.1-alpine-3.12.0
2020/09/10 19:13:51 [INFO] ▶ Start clair-scanner
2020/09/10 19:14:00 [INFO] ▶ Server listening on port 9279
2020/09/10 19:14:00 [INFO] ▶ Analyzing 31609b718dd2bed92b93b1ab00c0ff67419a3121d0144bef0dc6ca49718820a7
2020/09/10 19:14:00 [INFO] ▶ Analyzing 3976d1b9666c5cbe28c7ea487a5e27eac6d4234df00928b45698a1255bafc2f6
2020/09/10 19:14:00 [INFO] ▶ Analyzing 1329196a4de820b1b5924d029813a5ece4bba37609f02d975d6e2aad895f462e
2020/09/10 19:14:01 [INFO] ▶ Analyzing 1e8258e1d908cbae762e26e7a036bfb4d8d116f664347e82fb4b69cad08d71ff
2020/09/10 19:14:01 [INFO] ▶ Analyzing afbada72da9106ce085d3235c31fd670ef63a0f4117dca21dc1b6e9f99da1387
2020/09/10 19:14:06 [INFO] ▶ Analyzing 28aeb668ceeeee715aae5e589f87a826e527df2b3dcdef93a9bae6d23a12d015
2020/09/10 19:14:06 [INFO] ▶ Analyzing 44af29d960215aa1a0e0afdd102a05694c97268e25421a7689ca1e4e0f68606a
2020/09/10 19:14:07 [INFO] ▶ Image [secureimages/jira-software:8.12.1-alpine-3.12.0] contains NO unapproved vulnerabilities
```

Security scanning using Trivy
```
docker run --rm -v /var/run/docker.sock:/var/run/docker.sock:ro aquasec/trivy:0.11.0 --no-progress secureimages/jira-software:8.12.1-alpine-3.12.0
2020-09-10T19:14:08.688Z        INFO    Need to update DB
2020-09-10T19:14:08.688Z        INFO    Downloading DB...
2020-09-10T19:14:24.935Z        INFO    Detecting Alpine vulnerabilities...

secureimages/jira-software:8.12.1-alpine-3.12.0 (alpine 3.12.0)
===============================================================
Total: 0 (UNKNOWN: 0, LOW: 0, MEDIUM: 0, HIGH: 0, CRITICAL: 0)
```

## Official Docker image (~771MB)

[https://hub.docker.com/r/atlassian/jira-software](https://hub.docker.com/r/atlassian/jira-software)
```
docker pull atlassian/jira-software:8.12.1
```

Security scanning using Clair
```
clair-scanner atlassian/jira-software:8.12.1
2020/09/10 19:14:32 [INFO] ▶ Start clair-scanner
2020/09/10 19:14:46 [INFO] ▶ Server listening on port 9279
2020/09/10 19:14:46 [INFO] ▶ Analyzing c46312971b989857795a66c3a16a6c5ad3faf70f68a86374d05fc98271302d31
2020/09/10 19:14:46 [INFO] ▶ Analyzing d5daf2b531bb4b815a1be1530978615e27bbc862258d1fd287df43a3b662181a
2020/09/10 19:14:46 [INFO] ▶ Analyzing 989dbccc76e96e34b561b0eef7753f3134b58ab454b5b222a965ff87e25cf9fb
2020/09/10 19:14:46 [INFO] ▶ Analyzing 16191067d3bf92aa3d59d244f8b1e91d2c656cbe68304eaade0f4a7d0204648c
2020/09/10 19:14:46 [INFO] ▶ Analyzing aa8841fd4b53337dcecd11d73d685fbc46bb1d8b219ff6b114817cd8418ac853
2020/09/10 19:14:46 [INFO] ▶ Analyzing 44f89f27c07f67d8e17cb7b1104d7c0fb79743713ea0ecc6c4cf29bb447c1cd1
2020/09/10 19:14:50 [INFO] ▶ Analyzing 511007489f92d5fcd7b8e8c053a68cb375c8d98c26608f79966e304e235144e0
2020/09/10 19:14:50 [INFO] ▶ Analyzing 4f970808b2a36208d65282b3aca288005e3e0e5eb8ef800d0a3558efebfe0a4e
2020/09/10 19:14:50 [INFO] ▶ Analyzing edfab43a5f37d2f460addbac5e014694c5d0a89ce1e7755093e9fd2770399a84
2020/09/10 19:14:51 [INFO] ▶ Analyzing 77f86c942c750e03170e4e7c3940add0654748816deca3dce8fa1c97535e363b
2020/09/10 19:14:51 [INFO] ▶ Analyzing cfbd367e363a899b28d476ea8c28c9c829d2489858aee76da66b030f8e3f79e3
2020/09/10 19:14:51 [INFO] ▶ Analyzing 865d336820212606a07740d41f0980b6ed319ae10d1d15b4a75e1515c4abe9e4
2020/09/10 19:14:51 [INFO] ▶ Analyzing 55994a3a819b78e98e00569c960e2360b3d442e6a2a75272bd096defce311c71
2020/09/10 19:14:51 [INFO] ▶ Analyzing 9a057a3de2137656a6a2a1d808a312c32df7c149ae3f3959c7091037ba0565ac
2020/09/10 19:14:51 [WARN] ▶ Image [atlassian/jira-software:8.12.1] contains 39 total vulnerabilities
2020/09/10 19:14:51 [ERRO] ▶ Image [atlassian/jira-software:8.12.1] contains 39 unapproved vulnerabilities
```

Security scanning using Trivy
```
docker run --rm -v /var/run/docker.sock:/var/run/docker.sock:ro aquasec/trivy:0.11.0 --no-progress atlassian/jira-software:8.12.1
2020-09-10T19:14:53.477Z        INFO    Need to update DB
2020-09-10T19:14:53.477Z        INFO    Downloading DB...
2020-09-10T19:15:11.918Z        INFO    Detecting Ubuntu vulnerabilities...

atlassian/jira-software:8.12.1 (ubuntu 18.04)
=============================================
Total: 87 (UNKNOWN: 0, LOW: 75, MEDIUM: 12, HIGH: 0, CRITICAL: 0)
```
