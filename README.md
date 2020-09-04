# Atlassian Jira Software

Atlassian Jira Software, image is based on the Alpine base image with 0 vulnerabilities.

## Current Docker image (~757MB)

Security scanning using Clair
```
clair-scanner secureimages/jira-software:8.12.0-alpine-3.12.0
2020/09/04 15:21:30 [INFO] ▶ Start clair-scanner
2020/09/04 15:21:39 [INFO] ▶ Server listening on port 9279
2020/09/04 15:21:39 [INFO] ▶ Analyzing 31609b718dd2bed92b93b1ab00c0ff67419a3121d0144bef0dc6ca49718820a7
2020/09/04 15:21:39 [INFO] ▶ Analyzing 5e25fb4df574d5cd8af719ffdc3bbb48734f326a467135d1319e0c7231198256
2020/09/04 15:21:39 [INFO] ▶ Analyzing ce8ea612bf3a84361f6e47092ad06c0a25402c99d91c7f92827ce14e8a2af84a
2020/09/04 15:21:39 [INFO] ▶ Analyzing f7e8d5ae889082e727bec1752314a86f71fed2c61061eb6dee3e24c12f3e3484
2020/09/04 15:21:39 [INFO] ▶ Analyzing 38bb2dd205742f70b001febcff26acbe36ce0ff9cc2b63dbbe6f6882f1aca269
2020/09/04 15:21:39 [INFO] ▶ Analyzing 6831d85b3fd13e28f799a6ba17bb1d1ff3623dffe1724c901fb1c68540daa985
2020/09/04 15:21:39 [INFO] ▶ Analyzing 4f147eb1210f3127b75e2b9039accf31249c801bc10ec7d252a6861e08f04d51
2020/09/04 15:21:40 [INFO] ▶ Image [secureimages/jira-software:8.12.0-alpine-3.12.0] contains NO unapproved vulnerabilities
```

Security scanning using Trivy
```
docker run --rm -v /var/run/docker.sock:/var/run/docker.sock:ro aquasec/trivy:0.11.0 --no-progress secureimages/jira-software:8.12.0-alpine-3.12.0
2020-09-04T15:21:41.932Z        INFO    Need to update DB
2020-09-04T15:21:41.932Z        INFO    Downloading DB...
2020-09-04T15:21:56.055Z        INFO    Detecting Alpine vulnerabilities...

secureimages/jira-software:8.12.0-alpine-3.12.0 (alpine 3.12.0)
===============================================================
Total: 0 (UNKNOWN: 0, LOW: 0, MEDIUM: 0, HIGH: 0, CRITICAL: 0)
```

## Official Docker image (~771MB)

[https://hub.docker.com/r/atlassian/jira-software](https://hub.docker.com/r/atlassian/jira-software)
```
docker pull atlassian/jira-software:8.12.0
```

Security scanning using Clair
```
clair-scanner atlassian/jira-software:8.12.0
2020/09/04 15:22:00 [INFO] ▶ Start clair-scanner
2020/09/04 15:22:13 [INFO] ▶ Server listening on port 9279
2020/09/04 15:22:13 [INFO] ▶ Analyzing c46312971b989857795a66c3a16a6c5ad3faf70f68a86374d05fc98271302d31
2020/09/04 15:22:14 [INFO] ▶ Analyzing d5daf2b531bb4b815a1be1530978615e27bbc862258d1fd287df43a3b662181a
2020/09/04 15:22:14 [INFO] ▶ Analyzing 989dbccc76e96e34b561b0eef7753f3134b58ab454b5b222a965ff87e25cf9fb
2020/09/04 15:22:14 [INFO] ▶ Analyzing 16191067d3bf92aa3d59d244f8b1e91d2c656cbe68304eaade0f4a7d0204648c
2020/09/04 15:22:14 [INFO] ▶ Analyzing aa8841fd4b53337dcecd11d73d685fbc46bb1d8b219ff6b114817cd8418ac853
2020/09/04 15:22:14 [INFO] ▶ Analyzing 44f89f27c07f67d8e17cb7b1104d7c0fb79743713ea0ecc6c4cf29bb447c1cd1
2020/09/04 15:22:14 [INFO] ▶ Analyzing 0f5637d4cc3801dcb2687caf8e3fe1107e11dde83a7c94c58ad1a38dfd22a1fc
2020/09/04 15:22:14 [INFO] ▶ Analyzing 20676038a6589f0f3f8a7d88b89d68094dbad193db21e4a34adbafbcfa64f92b
2020/09/04 15:22:14 [INFO] ▶ Analyzing 1ddeb6bbf7cd7a7860801113b0ef9c7a9aff0e647f604e5e83721f1f2b95b015
2020/09/04 15:22:14 [INFO] ▶ Analyzing 6528c1a2096fb5dc0a139d9a87e8eaaf2d121ff778ac41f1488ebdff41d24582
2020/09/04 15:22:14 [INFO] ▶ Analyzing 252fb92d754ec24087c193f2798b8ecf545ef8952a2962150ff64b4b8ec99cbe
2020/09/04 15:22:14 [INFO] ▶ Analyzing e711203918a5900690a531d36e32f46d89c0f68138a2e19b392ba72c21e7bfad
2020/09/04 15:22:14 [INFO] ▶ Analyzing f588a879bdad31f0318ac451ad9f7ce59543a5dadd77a69864b77a62862a6344
2020/09/04 15:22:14 [INFO] ▶ Analyzing 78e6a33e45b451fe07a2f0e618c724b6bbc7ccddecf56a15b5a48c369db467b9
2020/09/04 15:22:14 [WARN] ▶ Image [atlassian/jira-software:8.12.0] contains 39 total vulnerabilities
2020/09/04 15:22:14 [ERRO] ▶ Image [atlassian/jira-software:8.12.0] contains 39 unapproved vulnerabilities
```

Security scanning using Trivy
```
docker run --rm -v /var/run/docker.sock:/var/run/docker.sock:ro aquasec/trivy:0.11.0 --no-progress atlassian/jira-software:8.12.0
2020-09-04T15:22:16.596Z        INFO    Need to update DB
2020-09-04T15:22:16.596Z        INFO    Downloading DB...
2020-09-04T15:22:33.600Z        INFO    Detecting Ubuntu vulnerabilities...

atlassian/jira-software:8.12.0 (ubuntu 18.04)
=============================================
Total: 87 (UNKNOWN: 0, LOW: 75, MEDIUM: 12, HIGH: 0, CRITICAL: 0)
```
