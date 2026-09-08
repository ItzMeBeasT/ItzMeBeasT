<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0D0D0D,100:B87333&height=180&section=header&text=Regan&fontSize=54&fontColor=F5F5F5&fontAlignY=40&animation=fadeIn"/>

<h3>Software Engineer — Systems, Cloud & Reliability</h3>

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&size=17&duration=3200&pause=900&color=B87333&center=true&vCenter=true&width=650&lines=Software+first%2C+infrastructure+by+necessity;Cloud+%26+DevOps+as+a+specialization%2C+not+the+whole+story;Exploring+AI+as+an+engineering+tool%2C+not+a+buzzword" />

<a href="https://www.linkedin.com/in/regan-jesuraju/"><img src="https://img.shields.io/badge/LinkedIn-0D0D0D?style=for-the-badge&logo=linkedin&logoColor=B87333"/></a>
<a href="https://medium.com/@regannbis"><img src="https://img.shields.io/badge/Medium-0D0D0D?style=for-the-badge&logo=medium&logoColor=D99B63"/></a>
<a href="mailto:regannbis@gmail.com"><img src="https://img.shields.io/badge/Email-0D0D0D?style=for-the-badge&logo=gmail&logoColor=B87333"/></a>

</div>

<br/>

I build software, then go find out how it actually runs in production — which is how Linux, containers, and Kubernetes ended up permanently in my stack. I'd rather ship three systems I understand end-to-end than ten I've only glued together.

<br/>

## Featured engineering

### Kubernetes Monitoring Platform

Most monitoring setups stop at `docker-compose up`. This one is built to answer a harder question: *what does it take to run observability safely inside a cluster, not just visibly?*

It started as a Docker Compose stack — Prometheus, Grafana, and Node Exporter, version-pinned, with credentials externalized rather than hardcoded. Once the scrape targets were verified and the dashboards were auto-provisioning correctly, I migrated it onto Kubernetes and treated security as part of the design, not an afterthought bolted on at the end:

- **RBAC + Secrets** — scoped service accounts instead of default-namespace access
- **Default-deny NetworkPolicy** — with explicit egress/ingress rules carved out for Prometheus specifically, rather than one blanket allow rule
- **Persistent storage** — PVCs so metrics survive pod restarts
- **CI validation** — every manifest is checked with `kubeconform` before it can merge

```mermaid
flowchart LR
    subgraph Cluster["Kubernetes Cluster"]
        direction LR
        NE[Node Exporter] --> P[Prometheus]
        CA[cAdvisor] --> P
        P --> G[Grafana]
        P --> AM[Alertmanager]
        P -.persists to.-> PVC[(PVC)]
    end
    RBAC[RBAC + Secrets] -.guards.-> Cluster
    NP[Default-deny NetworkPolicy] -.guards.-> Cluster
    CI[CI: kubeconform validation] -->|on push| Cluster

    style Cluster fill:#171717,stroke:#B87333,color:#F5F5F5
    style RBAC fill:#0D0D0D,stroke:#D99B63,color:#F5F5F5
    style NP fill:#0D0D0D,stroke:#D99B63,color:#F5F5F5
    style CI fill:#0D0D0D,stroke:#D99B63,color:#F5F5F5
    style PVC fill:#0D0D0D,stroke:#D99B63,color:#F5F5F5
```

`Kubernetes` `Docker` `Prometheus` `Grafana` `Alertmanager` `RBAC` `NetworkPolicies` `CI/CD`

<!-- Replace the line below with your actual repo URL -->
**[→ View repository](https://github.com/ItzMeBeasT/REPLACE-WITH-REPO-NAME)**

<br/>

## Other builds

| Project | Engineering angle |
|---|---|
| **AI Incident Copilot** | Built and shipped inside a 36-hour hackathon window with a deliberately locked scope — the constraint was time, and the deliverable had to work, not be exhaustive. |
| **Cloud Computing Internship (Corizo)** | Hands-on AWS fundamentals — IAM, storage, hosting — through to a working static site deployed on S3. |
| **Gemini LifeOS** | An AI-assisted app that turns daily reflection into structured next steps, built for the Personal Gemini Journal challenge. |

<br/>

## What I work with

**Languages & foundations** — Java, Python, Bash, and ongoing DSA practice

**Systems & cloud** — Linux (Fedora, daily driver), AWS, Docker, Kubernetes

**Observability & automation** — Prometheus, Grafana, GitHub Actions

**Data & networking** — MySQL, Cisco networking fundamentals

<div align="center">

![Java](https://img.shields.io/badge/Java-0D0D0D?style=for-the-badge&logo=openjdk&logoColor=B87333)
![Python](https://img.shields.io/badge/Python-0D0D0D?style=for-the-badge&logo=python&logoColor=D99B63)
![Linux](https://img.shields.io/badge/Linux-0D0D0D?style=for-the-badge&logo=linux&logoColor=B87333)
![AWS](https://img.shields.io/badge/AWS-0D0D0D?style=for-the-badge&logo=amazon-aws&logoColor=D99B63)
![Docker](https://img.shields.io/badge/Docker-0D0D0D?style=for-the-badge&logo=docker&logoColor=B87333)
![Kubernetes](https://img.shields.io/badge/Kubernetes-0D0D0D?style=for-the-badge&logo=kubernetes&logoColor=D99B63)
![Prometheus](https://img.shields.io/badge/Prometheus-0D0D0D?style=for-the-badge&logo=prometheus&logoColor=B87333)
![Grafana](https://img.shields.io/badge/Grafana-0D0D0D?style=for-the-badge&logo=grafana&logoColor=D99B63)
![MySQL](https://img.shields.io/badge/MySQL-0D0D0D?style=for-the-badge&logo=mysql&logoColor=B87333)

</div>

<br/>

## Current focus

Software engineering fundamentals (Java, DSA) running in parallel with infrastructure depth — Linux administration first, then cloud architecture, then networking and Kubernetes administration.

| Certification | Area | Status |
|---|---|---|
| RHCSA | Linux administration | In progress |
| AWS Solutions Architect Associate | Cloud architecture | Planned |
| CCNA | Networking | Planned |
| CKA | Kubernetes administration | Planned |

<br/>

## Activity

<div align="center">

<img src="https://github-readme-stats.vercel.app/api?username=ItzMeBeasT&show_icons=true&count_private=true&include_all_commits=true&hide_border=true&bg_color=0D0D0D&title_color=B87333&icon_color=D99B63&text_color=F5F5F5&ring_color=B87333" height="160"/>
<img src="https://streak-stats.demolab.com/?user=ItzMeBeasT&hide_border=true&background=0D0D0D&ring=B87333&fire=B87333&currStreakLabel=F5F5F5&sideNums=F5F5F5&currStreakNum=F5F5F5&sideLabels=D99B63&dates=8A8A8A&border=0D0D0D" height="160"/>

<!-- Uncomment once the snake.yml workflow has run at least once and the `output` branch exists -->
<!-- <img src="https://raw.githubusercontent.com/ItzMeBeasT/ItzMeBeasT/output/github-contribution-grid-snake.svg" width="100%"/> -->

</div>

<br/>

<div align="center">

<a href="https://www.linkedin.com/in/regan-jesuraju/"><img src="https://img.shields.io/badge/Connect-0D0D0D?style=for-the-badge&logo=linkedin&logoColor=B87333"/></a>
<a href="https://medium.com/@regannbis"><img src="https://img.shields.io/badge/Read_my_writing-0D0D0D?style=for-the-badge&logo=medium&logoColor=D99B63"/></a>

<br/><br/>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:B87333,100:0D0D0D&height=100&section=footer"/>

</div>
