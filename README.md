# Atlassian Jira Software

Atlassian Jira Software, image is based on the Alpine base image with 0 vulnerabilities.

## Current Docker image (~779MB)

Security scanning using Clair
```
clair-scanner secureimages/jira-software:8.10.0-alpine-3.12.0
2020/06/25 20:41:56 [INFO] ▶ Start clair-scanner
2020/06/25 20:42:16 [INFO] ▶ Server listening on port 9279
2020/06/25 20:42:16 [INFO] ▶ Analyzing 76de98d374759ed05698adec9aa042db7bc0f62c25fb612c0f9be1419a581421
2020/06/25 20:42:16 [INFO] ▶ Analyzing 8adc027d528dbd80cda62ce3c0347475a88781dee4a56872705e3f109140379c
2020/06/25 20:42:16 [INFO] ▶ Analyzing 953f2f4b616e13a9114960e32888094534511066ca99b205f7a6dda378c3749f
2020/06/25 20:42:16 [INFO] ▶ Analyzing e12c1c2372dd98c124d510f81411c173893cd582243071b23d0fb39c4dce2cbb
2020/06/25 20:42:16 [INFO] ▶ Analyzing 0b6cc6ecb49919fb2ec2bfea2fef5fc108124a813d431f938957bb5a548f8973
2020/06/25 20:42:16 [INFO] ▶ Analyzing 5465b38f0346a1bf4e49259f9f943e1074ddf0d9b470703e3ad70e847fcdfe29
2020/06/25 20:42:16 [INFO] ▶ Analyzing 51c55388b149fd078afa032b6041c7e0f538add551a6f49d675aab05cfa1d8fd
2020/06/25 20:42:16 [INFO] ▶ Image [secureimages/jira-software:8.10.0-alpine-3.12.0] contains NO unapproved vulnerabilities
```

Security scanning using Trivy
```
docker run --rm -v /var/run/docker.sock:/var/run/docker.sock:ro aquasec/trivy:0.9.1 --no-progress secureimages/jira-software:8.10.0-alpine-3.12.0
2020-06-25T17:42:19.144Z        INFO    Need to update DB
2020-06-25T17:42:19.144Z        INFO    Downloading DB...
2020-06-25T17:43:04.659Z        INFO    Detecting Alpine vulnerabilities...

secureimages/jira-software:8.10.0-alpine-3.12.0 (alpine 3.12.0)
===============================================================
Total: 0 (UNKNOWN: 0, LOW: 0, MEDIUM: 0, HIGH: 0, CRITICAL: 0)
```

## Official Docker image (~796MB)

[https://hub.docker.com/r/atlassian/jira-software](https://hub.docker.com/r/atlassian/jira-software)
```
docker pull atlassian/jira-software:8.10.0
```

Security scanning using Clair
```
clair-scanner atlassian/jira-software:8.10.0
2020/06/25 20:43:11 [INFO] ▶ Start clair-scanner
2020/06/25 20:43:30 [INFO] ▶ Server listening on port 9279
2020/06/25 20:43:30 [INFO] ▶ Analyzing 4046a0366bf3d63d6ebb165835dd7cd4a72c49d65942a66efb1b4a44bf5803b2
2020/06/25 20:43:30 [INFO] ▶ Analyzing cb6f8e1a8e2c47f2e7eda433f9afb3ce6debe0131ba556f6ab516f1092b589be
2020/06/25 20:43:30 [INFO] ▶ Analyzing f81f5853c77138f4f3bef3fe7a639070314c8b38f66f03f57055b5d9055c5c7a
2020/06/25 20:43:30 [INFO] ▶ Analyzing 5171a8ddd9ca89e576ef04f932cfff352168ff2e06f856cc05d09b998989c8c5
2020/06/25 20:43:30 [INFO] ▶ Analyzing 1f57d26728894cc8af89d0b20d65b58665f2a61b3c79a0bb15dac3f75a87857c
2020/06/25 20:43:30 [INFO] ▶ Analyzing bbbb9e1c8917a5c71485f1bbb149f2b7a7194c890717c9160dc2aabe5d66e6d8
2020/06/25 20:43:30 [INFO] ▶ Analyzing cfd1b519222cfeeb060064e55903e7853034a4b4bec9da12f19e8faece845b32
2020/06/25 20:43:30 [INFO] ▶ Analyzing 471f5a496add6a99fad545c7c5e082fa47678a061871c2ffdb53e2bcdf71df67
2020/06/25 20:43:30 [INFO] ▶ Analyzing 8f1f43b4a8f751ea4c3bff4adce9dc3cd9b2fb463c066d1ad296fadc30d2b0d1
2020/06/25 20:43:30 [INFO] ▶ Analyzing b774feb3fb58d76b07679ec91678ba2fb619c22d7ebafba94bd00b24d58e1c3a
2020/06/25 20:43:30 [INFO] ▶ Analyzing 8c4146a77a994e49b8d704e81a4208bfd8a17a915b517435834b8f2c623a3ba9
2020/06/25 20:43:31 [INFO] ▶ Analyzing c114f213283ae5df10a45b874dc05aeee394ce33bf6bf55fe98b565f047acda2
2020/06/25 20:43:31 [INFO] ▶ Analyzing 77193e458dd1b3184e886038e184fa1fd9052fe18c516d7438e3c225b6a04b99
2020/06/25 20:43:31 [INFO] ▶ Analyzing b969873c01071a17c025410bc83d55713ee7bb7188bed559a5e62b9308e02572
2020/06/25 20:43:31 [WARN] ▶ Image [atlassian/jira-software:8.10.0] contains 48 total vulnerabilities
2020/06/25 20:43:31 [ERRO] ▶ Image [atlassian/jira-software:8.10.0] contains 48 unapproved vulnerabilities
```

Security scanning using Trivy
```
docker run --rm -v /var/run/docker.sock:/var/run/docker.sock:ro aquasec/trivy:0.9.1 --no-progress atlassian/jira-software:8.10.0
2020-06-25T17:43:33.313Z        INFO    Need to update DB
2020-06-25T17:43:33.313Z        INFO    Downloading DB...
2020-06-25T17:43:52.770Z        INFO    Detecting Ubuntu vulnerabilities...

atlassian/jira-software:8.10.0 (ubuntu 18.04)
=============================================
Total: 113 (UNKNOWN: 0, LOW: 82, MEDIUM: 31, HIGH: 0, CRITICAL: 0)
```
