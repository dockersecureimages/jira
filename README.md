# Atlassian Jira Software

Atlassian Jira Software, image is based on the Alpine base image with 0 vulnerabilities.

## Current Docker image (~757MB)

Security scanning using Clair
```
clair-scanner secureimages/jira-software:8.12.3-alpine-3.12.0
2020/10/15 19:47:43 [INFO] ▶ Start clair-scanner
2020/10/15 19:47:52 [INFO] ▶ Server listening on port 9279
2020/10/15 19:47:52 [INFO] ▶ Analyzing 31609b718dd2bed92b93b1ab00c0ff67419a3121d0144bef0dc6ca49718820a7
2020/10/15 19:47:52 [INFO] ▶ Analyzing a29360a362c416aca6365aafcfcd36848d8d1f58b517748606036b294413d664
2020/10/15 19:47:52 [INFO] ▶ Analyzing 2f8e7b5b65c615c61546ee534a3a2eb6ebb6ac3a91ea7ae156ea38c95c053eb7
2020/10/15 19:47:53 [INFO] ▶ Analyzing b1e4d22d71755c4f30f6ffd8b7694cf8a4c0d5da018fa812fa0c4e279b078f67
2020/10/15 19:47:53 [INFO] ▶ Analyzing cefba092fbb777c4c69912be4d5bb6a37c6a6e96aaf0375c1587e76a95735a7e
2020/10/15 19:47:53 [INFO] ▶ Analyzing 1b4bc6a0089b8d0d61e3c102bdfb6ebc86730f65aec9a1b621ea117504e5c08d
2020/10/15 19:47:53 [INFO] ▶ Analyzing 23a846d04cd832094c7f877538e8e08cdc75d00cbb3069c0cfbaf6d14b92365e
2020/10/15 19:47:53 [INFO] ▶ Image [secureimages/jira-software:8.12.3-alpine-3.12.0] contains NO unapproved vulnerabilities
```

Security scanning using Trivy
```
docker run --rm -v /var/run/docker.sock:/var/run/docker.sock:ro aquasec/trivy:0.12.0 --no-progress secureimages/jira-software:8.12.3-alpine-3.12.0
2020-10-15T19:47:55.412Z        INFO    Need to update DB
2020-10-15T19:47:55.412Z        INFO    Downloading DB...
2020-10-15T19:48:13.345Z        INFO    Detecting Alpine vulnerabilities...

secureimages/jira-software:8.12.3-alpine-3.12.0 (alpine 3.12.0)
===============================================================
Total: 0 (UNKNOWN: 0, LOW: 0, MEDIUM: 0, HIGH: 0, CRITICAL: 0)
```

## Official Docker image (~768MB)

[https://hub.docker.com/r/atlassian/jira-software](https://hub.docker.com/r/atlassian/jira-software)
```
docker pull atlassian/jira-software:8.12.3
```

Security scanning using Clair
```
clair-scanner atlassian/jira-software:8.12.3
2020/10/15 19:48:18 [INFO] ▶ Start clair-scanner
2020/10/15 19:48:32 [INFO] ▶ Server listening on port 9279
2020/10/15 19:48:32 [INFO] ▶ Analyzing 8bf067b107a6f7444876e33c6ed85652355f679ac98ebab97ab3ebad63f0dff3
2020/10/15 19:48:32 [INFO] ▶ Analyzing 468327b5cd7ce539db695bd0ef05dae8a4ff77b02870a8e823ed74dedad4bd55
2020/10/15 19:48:32 [INFO] ▶ Analyzing 6cf145843a8d3af29f9b328595994e1487c110c5adcecc8d7125505cbea1b5b7
2020/10/15 19:48:32 [INFO] ▶ Analyzing 415d0f5c2fff0014bd97ab748cc52035abd28275da951556826b6a351a62e180
2020/10/15 19:48:32 [INFO] ▶ Analyzing 2b9923c3a1e3b39f2e0efc58dd2cfe0126e82cf648c3f3889c88c62e66fb4267
2020/10/15 19:48:32 [INFO] ▶ Analyzing b89e74c6f95ad6b288370e6c7743efe93d414a211c9909b33f220f8ec66b7e40
2020/10/15 19:48:32 [INFO] ▶ Analyzing 7e343aa499a509198a2aae4c721bba989ee538834fd030d794ec89e1fb645b2e
2020/10/15 19:48:33 [INFO] ▶ Analyzing e817f76c3921b7f370622abe220c13b9facff1b1930d5967ce03464fcbbf73f8
2020/10/15 19:48:33 [INFO] ▶ Analyzing d1b29b6fa7316d2abacfc0741bbaaf6ec8683ae703401881558308d6bbc8a723
2020/10/15 19:48:33 [INFO] ▶ Analyzing 1ad35d6de1671305691c0f7a963aa6e2bdc979f8b286f296093a9bbfc23b7138
2020/10/15 19:48:34 [INFO] ▶ Analyzing ecd6194e597aec950322338668d0a0ff8a78d7978527143a6f68ffddf0d8cbd3
2020/10/15 19:48:34 [INFO] ▶ Analyzing 23586e9ce53a18387dde2b9244b7746b59787d34acb352b2dfad3ba245137c5c
2020/10/15 19:48:35 [INFO] ▶ Analyzing e1e4e224079851c71696ce29b58beec26c02fe5081467e59f009c80a056116f5
2020/10/15 19:48:35 [WARN] ▶ Image [atlassian/jira-software:8.12.3] contains 38 total vulnerabilities
2020/10/15 19:48:35 [ERRO] ▶ Image [atlassian/jira-software:8.12.3] contains 38 unapproved vulnerabilities
```

Security scanning using Trivy
```
docker run --rm -v /var/run/docker.sock:/var/run/docker.sock:ro aquasec/trivy:0.12.0 --no-progress atlassian/jira-software:8.12.3
2020-10-15T19:48:36.941Z        INFO    Need to update DB
2020-10-15T19:48:36.941Z        INFO    Downloading DB...
2020-10-15T19:48:56.488Z        INFO    Detecting Ubuntu vulnerabilities...

atlassian/jira-software:8.12.3 (ubuntu 18.04)
=============================================
Total: 77 (UNKNOWN: 0, LOW: 65, MEDIUM: 12, HIGH: 0, CRITICAL: 0)
```
