# Atlassian Jira Software

Atlassian Jira Software, image is based on the Alpine base image with 0 vulnerabilities.

## Current Docker image (~778MB)

Security scanning using Clair
```
clair-scanner secureimages/jira-software:8.9.0-alpine-3.11.6
2020/05/20 11:11:51 [INFO] ▶ Start clair-scanner
2020/05/20 11:12:09 [INFO] ▶ Server listening on port 9279
2020/05/20 11:12:09 [INFO] ▶ Analyzing a5304328ea0f44bd1ac8bb5416ad6b7cc3b747ac232c6af66d7d9f12e9854344
2020/05/20 11:12:09 [INFO] ▶ Analyzing b8418fcaa46c3d215536729a77540ab64e93d13a56a9c409dcec796cd2b4a594
2020/05/20 11:12:09 [INFO] ▶ Analyzing 77d2d9daa10e258ac35032d152f0c33b75753e35dbfcf24a96a73b8bdc2b53c6
2020/05/20 11:12:09 [INFO] ▶ Analyzing 7b16dcfdb33bb1b3202bbb4c95d2bd0b9d6b126b40b1966e6c640c866afba9e3
2020/05/20 11:12:09 [INFO] ▶ Analyzing d68349834dc7e1498d4b8390eb0761d9ed85c29b2b656f3366ecf828e30e0a57
2020/05/20 11:12:09 [INFO] ▶ Analyzing 7f3c16a2d7586818cfc48f47abbc485d78042002133e983292c7ec1ad0350e5c
2020/05/20 11:12:09 [INFO] ▶ Analyzing 10ad0ad4744af211df1299f47d3ce03f0e8ff4103dc1f131083e111a8c9fc311
2020/05/20 11:12:09 [INFO] ▶ Image [secureimages/jira-software:8.9.0-alpine-3.11.6] contains NO unapproved vulnerabilities
```

Security scanning using Trivy
```
docker run --rm -v /var/run/docker.sock:/var/run/docker.sock:ro aquasec/trivy:0.7.0 --no-progress secureimages/jira-software:8.9.0-alpine-3.11.6
2020-05-20T08:13:15.366Z        INFO    Need to update DB
2020-05-20T08:13:15.366Z        INFO    Downloading DB...
2020-05-20T08:13:36.954Z        INFO    Detecting Alpine vulnerabilities...

secureimages/jira-software:8.9.0-alpine-3.11.6 (alpine 3.11.6)
==============================================================
Total: 0 (UNKNOWN: 0, LOW: 0, MEDIUM: 0, HIGH: 0, CRITICAL: 0)
```

## Official Docker image (~789MB)

[https://hub.docker.com/r/atlassian/jira-software](https://hub.docker.com/r/atlassian/jira-software)
```
docker pull atlassian/jira-software:8.9.0
```

Security scanning using Clair
```
clair-scanner atlassian/jira-software:8.9.0
2020/05/20 11:13:43 [INFO] ▶ Start clair-scanner
2020/05/20 11:13:59 [INFO] ▶ Server listening on port 9279
2020/05/20 11:13:59 [INFO] ▶ Analyzing 6ef5a7b6cc6da3fe4489191c166763832ff732b6c346e7d77a2dbbd3e89a9f08
2020/05/20 11:13:59 [INFO] ▶ Analyzing c774328901d4a9ee5201de46d502b8f56f9b6a5d21c64affa6ca96d3b69cfe68
2020/05/20 11:13:59 [INFO] ▶ Analyzing 67b382b86062872cc280027bfb3cc103cba4e52bb66d23c590e0cb8647dd39fe
2020/05/20 11:13:59 [INFO] ▶ Analyzing 4e0bca968c343d4488ae5b156e0b4a6630a6964bd401264b3fe9060a266f4ce7
2020/05/20 11:13:59 [INFO] ▶ Analyzing 33db261f08cfde61ed408a1688df09cec342cfc8e55dfcf32818a7b0418814f5
2020/05/20 11:13:59 [INFO] ▶ Analyzing 48aac7f877504db33ba7c4f499dc97cb249d21ca4a9912ecbf512e8f81a142ca
2020/05/20 11:13:59 [INFO] ▶ Analyzing 66fb2870f0412489e7e5a93a6ec10beb65573148f93c656732149d0b2de4f0a0
2020/05/20 11:13:59 [INFO] ▶ Analyzing e2c50d1062fd1139ad32c4e69c22cf95078fd599aef915612fc03f33ebf0ad14
2020/05/20 11:13:59 [INFO] ▶ Analyzing 220b7d54f9f2a623293b1cedca36922d145c0b6e03ad2476e6276c1d460ccdf5
2020/05/20 11:13:59 [INFO] ▶ Analyzing 8dd98114feac04eed68e37ecd78fddcb29a29e834e91296314654b3c7b7a5bd9
2020/05/20 11:13:59 [INFO] ▶ Analyzing 32165d416d656b147abfc2d11ec973748cd6c7e2b1ddb80947cc1e781a53f657
2020/05/20 11:14:00 [INFO] ▶ Analyzing 5732f4371c7c78da3d4d521a1a0eff11ff06646a299e41ffc3ec29430190a1b9
2020/05/20 11:14:00 [INFO] ▶ Analyzing 80fabd3d55e7e3d7a49ce2f598728a0bf2a3c3b210fe53df6a94e26d02a0adbe
2020/05/20 11:14:00 [INFO] ▶ Analyzing 957012cf3a84c717c95a3dce8239ca2d6145de7c882eecd9a826212b01b3cc88
2020/05/20 11:14:00 [WARN] ▶ Image [atlassian/jira-software:8.9.0] contains 48 total vulnerabilities
2020/05/20 11:14:00 [ERRO] ▶ Image [atlassian/jira-software:8.9.0] contains 48 unapproved vulnerabilities
```

Security scanning using Trivy
```
docker run --rm -v /var/run/docker.sock:/var/run/docker.sock:ro aquasec/trivy:0.7.0 --no-progress atlassian/jira-software:8.9.0
2020-05-20T08:14:02.567Z        INFO    Need to update DB
2020-05-20T08:14:02.568Z        INFO    Downloading DB...
2020-05-20T08:14:23.370Z        INFO    Detecting Ubuntu vulnerabilities...

atlassian/jira-software:8.9.0 (ubuntu 18.04)
============================================
Total: 111 (UNKNOWN: 0, LOW: 91, MEDIUM: 20, HIGH: 0, CRITICAL: 0)
```
