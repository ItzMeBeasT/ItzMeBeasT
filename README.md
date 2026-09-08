<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0D0D0D,100:B87333&height=190&section=header&text=Regan&fontSize=56&fontColor=F5F5F5&fontAlignY=40&animation=fadeIn"/>

<a href="https://readme-typing-svg.demolab.com">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&size=20&duration=3000&pause=800&color=B87333&center=true&vCenter=true&width=600&lines=Cloud+%26+DevOps+Engineer;Building+systems+that+stay+reliable+at+scale;Security-conscious+infrastructure,+by+design" />
</a>

<br/>

<a href="https://www.linkedin.com/in/regan-jesuraju/"><img src="https://img.shields.io/badge/LinkedIn-0D0D0D?style=for-the-badge&logo=linkedin&logoColor=B87333"/></a>
<a href="https://medium.com/@regannbis"><img src="https://img.shields.io/badge/Medium-0D0D0D?style=for-the-badge&logo=medium&logoColor=D99B63"/></a>
<a href="mailto:regannbis@gmail.com"><img src="https://img.shields.io/badge/Email-0D0D0D?style=for-the-badge&logo=gmail&logoColor=B87333"/></a>

</div>

<br/>

## Currently

```
> role       Computer Engineering student, targeting Cloud/DevOps SDE roles
> building   Kubernetes monitoring platform — Prometheus · Grafana · Alertmanager · RBAC
> roadmap    RHCSA  →  AWS Solutions Architect Associate  →  CCNA  →  CKA
> approach   3 flagship projects, done properly — not 10 done shallow
```

<br/>

## Flagship — Kubernetes Monitoring Platform

A self-hosted observability stack, secured the way a production cluster actually would be: least-privilege RBAC, default-deny NetworkPolicies with explicit egress/ingress rules, and manifest validation on every push.

```mermaid
flowchart LR
    subgraph Cluster["Kubernetes Cluster"]
        direction LR
        NE[Node Exporter] --> P[Prometheus]
        CA[cAdvisor] --> P
        P --> G[Grafana]
        P --> AM[Alertmanager]
    end
    RBAC[RBAC + Secrets] -.guards.-> Cluster
    NP[Default-deny NetworkPolicy] -.guards.-> Cluster
    CI[CI: kubeconform validation] -->|on push| Cluster

    style Cluster fill:#171717,stroke:#B87333,color:#F5F5F5
    style RBAC fill:#0D0D0D,stroke:#D99B63,color:#F5F5F5
    style NP fill:#0D0D0D,stroke:#D99B63,color:#F5F5F5
    style CI fill:#0D0D0D,stroke:#D99B63,color:#F5F5F5
```

`Kubernetes` `Docker` `Prometheus` `Grafana` `Alertmanager` `RBAC` `NetworkPolicies` `CI/CD`

**[→ View repository](https://github.com/ItzMeBeasT/REPLACE-WITH-REPO-NAME)** — swap in your actual repo URL

<br/>

## Other work

| Project | What it proves |
|---|---|
| **AI Incident Copilot** | Shipped a working K8s/DevOps incident-triage assistant in a 36-hour hackathon with a deliberately locked scope — decisiveness under time pressure |
| **Cloud Computing Internship (Corizo)** | AWS fundamentals through to a deployed S3 static site — IAM, storage, hosting basics done hands-on |
| **Gemini LifeOS** | AI reflection-to-action journal built for the Personal Gemini Journal challenge |

<br/>

## Stack

<div align="center">

![Java](https://img.shields.io/badge/Java-0D0D0D?style=for-the-badge&logo=openjdk&logoColor=B87333)
![Python](https://img.shields.io/badge/Python-0D0D0D?style=for-the-badge&logo=python&logoColor=D99B63)
![Bash](https://img.shields.io/badge/Bash-0D0D0D?style=for-the-badge&logo=gnubash&logoColor=B87333)
![AWS](https://img.shields.io/badge/AWS-0D0D0D?style=for-the-badge&logo=amazon-aws&logoColor=D99B63)
![Docker](https://img.shields.io/badge/Docker-0D0D0D?style=for-the-badge&logo=docker&logoColor=B87333)
![Kubernetes](https://img.shields.io/badge/Kubernetes-0D0D0D?style=for-the-badge&logo=kubernetes&logoColor=D99B63)
![Linux](https://img.shields.io/badge/Fedora_Linux-0D0D0D?style=for-the-badge&logo=fedora&logoColor=B87333)
![Prometheus](https://img.shields.io/badge/Prometheus-0D0D0D?style=for-the-badge&logo=prometheus&logoColor=D99B63)
![Grafana](https://img.shields.io/badge/Grafana-0D0D0D?style=for-the-badge&logo=grafana&logoColor=B87333)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-0D0D0D?style=for-the-badge&logo=githubactions&logoColor=D99B63)
![MySQL](https://img.shields.io/badge/MySQL-0D0D0D?style=for-the-badge&logo=mysql&logoColor=B87333)
![Cisco](https://img.shields.io/badge/Cisco-0D0D0D?style=for-the-badge&logo=cisco&logoColor=D99B63)

</div>

<br/>

## Certification roadmap

`RHCSA (in progress)` → `AWS SAA` → `CCNA` → `CKA`

<br/>

## Activity

<div align="center">

<img src="https://github-readme-stats.vercel.app/api?username=ItzMeBeasT&show_icons=true&count_private=true&include_all_commits=true&hide_border=true&bg_color=0D0D0D&title_color=B87333&icon_color=D99B63&text_color=F5F5F5&ring_color=B87333" height="165"/>
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=ItzMeBeasT&layout=compact&hide_border=true&bg_color=0D0D0D&title_color=B87333&text_color=F5F5F5&langs_count=7" height="165"/>

<img src="https://streak-stats.demolab.com/?user=ItzMeBeasT&hide_border=true&background=0D0D0D&ring=B87333&fire=B87333&currStreakLabel=F5F5F5&sideNums=F5F5F5&currStreakNum=F5F5F5&sideLabels=D99B63&dates=8A8A8A&border=0D0D0D" />

</div>

<!--
  Optional but worth doing: an animated "contribution snake" — your commit graph
  turned into a snake game that eats its way across your contributions, regenerated
  daily by a GitHub Action. It's a small flex that also happens to demonstrate CI
  automation, which is directly on-brand for a DevOps profile.
  Workflow file provided separately — see snake.yml. Once it's run once, uncomment
  the line below.
-->
<!-- <img src="https://raw.githubusercontent.com/ItzMeBeasT/ItzMeBeasT/output/github-contribution-grid-snake.svg" width="100%"/> -->

<br/>

## Get in touch

<div align="center">

<a href="https://www.linkedin.com/in/regan-jesuraju/"><img src="https://img.shields.io/badge/Connect-0D0D0D?style=for-the-badge&logo=linkedin&logoColor=B87333"/></a>
<a href="https://medium.com/@regannbis"><img src="https://img.shields.io/badge/Read_my_writing-0D0D0D?style=for-the-badge&logo=medium&logoColor=D99B63"/></a>

<br/><br/>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:B87333,100:0D0D0D&height=100&section=footer"/>

</div>
