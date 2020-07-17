# Atlassian Jira Software

Atlassian Jira Software, image is based on the Alpine base image with 0 vulnerabilities.

## Current Docker image (~759MB)

Security scanning using Clair
```
clair-scanner secureimages/jira-software:8.11.0-alpine-3.12.0
2020/07/17 14:29:05 [INFO] ▶ Start clair-scanner
2020/07/17 14:29:24 [INFO] ▶ Server listening on port 9279
2020/07/17 14:29:24 [INFO] ▶ Analyzing 76de98d374759ed05698adec9aa042db7bc0f62c25fb612c0f9be1419a581421
2020/07/17 14:29:24 [INFO] ▶ Analyzing c6479ea78d481fb438a7abbbc3b365b8c5c1cfd54ba7340c171f52bed4398139
2020/07/17 14:29:24 [INFO] ▶ Analyzing 99398db29f697075ee8e25616012932a30cac3bf85ac7b03bb470f6f722f8a59
2020/07/17 14:29:24 [INFO] ▶ Analyzing b4cbd6e3a759fdc8baa08cbb80b1ad45fd6e616d220a6f08170ea22207aa3f72
2020/07/17 14:29:24 [INFO] ▶ Analyzing d8d773ad1e8b4e0342ab04d710c27295ad25bc262e91689e8b333a998cdde342
2020/07/17 14:29:25 [INFO] ▶ Analyzing 5635de3bd3ecc40159bb2f7d794078a1588142469948be1d05b3debffa94f878
2020/07/17 14:29:25 [INFO] ▶ Analyzing d68bb380e053a2b45b4bfcec971df14a705860a45b6d2f322a81c022bfead92a
2020/07/17 14:29:25 [INFO] ▶ Image [secureimages/jira-software:8.11.0-alpine-3.12.0] contains NO unapproved vulnerabilities
```

Security scanning using Trivy
```
docker run --rm -v /var/run/docker.sock:/var/run/docker.sock:ro aquasec/trivy:0.9.2 --no-progress secureimages/jira-software:8.11.0-alpine-3.12.0
2020-07-17T11:29:30.152Z        INFO    Need to update DB
2020-07-17T11:29:30.152Z        INFO    Downloading DB...
2020-07-17T11:29:52.982Z        INFO    Detecting Alpine vulnerabilities...

secureimages/jira-software:8.11.0-alpine-3.12.0 (alpine 3.12.0)
===============================================================
Total: 0 (UNKNOWN: 0, LOW: 0, MEDIUM: 0, HIGH: 0, CRITICAL: 0)
```

## Official Docker image (~781MB)

[https://hub.docker.com/r/atlassian/jira-software](https://hub.docker.com/r/atlassian/jira-software)
```
docker pull atlassian/jira-software:8.11.0
```

Security scanning using Clair
```
clair-scanner atlassian/jira-software:8.11.0
2020/07/17 14:29:57 [INFO] ▶ Start clair-scanner
2020/07/17 14:30:14 [INFO] ▶ Server listening on port 9279
2020/07/17 14:30:14 [INFO] ▶ Analyzing eac38f7eb67b83a6e4970a491f1d74a27510b422968961d361d02823049def3f
2020/07/17 14:30:15 [INFO] ▶ Analyzing f09d25849e9828314f5027b75bb398bb7f0ee87d6a84dc0fd49cfbf46de9f02b
2020/07/17 14:30:15 [INFO] ▶ Analyzing 3a1c37708124f6c3c1d1ff1965ed4e13e7ccba99747b9457c35a53db563a874a
2020/07/17 14:30:15 [INFO] ▶ Analyzing bfb1707b3bd6ec47e80900687b5f5c015e9efeb82f234304ed74a8631bc2e75c
2020/07/17 14:30:15 [INFO] ▶ Analyzing 9ae61c13e50c4b87db90be46e5dee77f1b6f8ca6d724746364a7caa429e8c9d1
2020/07/17 14:30:15 [INFO] ▶ Analyzing 6899f2bb115ae38684042463c3aeae731a88d914cf32edac08bc34087869e35c
2020/07/17 14:30:15 [INFO] ▶ Analyzing 7ff8e6c71b3876989565628e8efc5b5b861cef953a8f8d06771fdd00e03daca9
2020/07/17 14:30:15 [INFO] ▶ Analyzing 79764262cf27ed0b9d22bddcb64782d01279ce256439137ce541475a6c5926cf
2020/07/17 14:30:15 [INFO] ▶ Analyzing 9818041698de5a74c2cb4f97780b64b91b86d25c397e6f0b962efa538a2846d6
2020/07/17 14:30:15 [INFO] ▶ Analyzing 521629514f594f8944f233e132cf2a11fd7d6ba70c45be2a322644ef7a4810ec
2020/07/17 14:30:15 [INFO] ▶ Analyzing e6b40e904e9f0ff3632cd5079d880fe0f2d2f67eb78d1ef9590b9e65167ac030
2020/07/17 14:30:16 [INFO] ▶ Analyzing 6eb42f67cd67af121a6a0c288e130eb70a918f0cd03db4eacfadacf11bfc342a
2020/07/17 14:30:16 [INFO] ▶ Analyzing a2c7ccf839708db1b244a994915b96e62a2c1bbef4694fc8b2994ad9fdd42f66
2020/07/17 14:30:16 [INFO] ▶ Analyzing a921169f1a15808bdb0b141ae8d8c3b30fa7ef8a59cc7ba47b2fd9eb4a7f1f69
2020/07/17 14:30:16 [WARN] ▶ Image [atlassian/jira-software:8.11.0] contains 39 total vulnerabilities
2020/07/17 14:30:16 [ERRO] ▶ Image [atlassian/jira-software:8.11.0] contains 39 unapproved vulnerabilities
```

Security scanning using Trivy
```
docker run --rm -v /var/run/docker.sock:/var/run/docker.sock:ro aquasec/trivy:0.9.2 --no-progress atlassian/jira-software:8.11.0
2020-07-17T11:30:28.385Z        INFO    Need to update DB
2020-07-17T11:30:28.385Z        INFO    Downloading DB...
2020-07-17T11:30:47.217Z        INFO    Detecting Ubuntu vulnerabilities...

atlassian/jira-software:8.11.0 (ubuntu 18.04)
=============================================
Total: 87 (UNKNOWN: 0, LOW: 70, MEDIUM: 17, HIGH: 0, CRITICAL: 0)
```
