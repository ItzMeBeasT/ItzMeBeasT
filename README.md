<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0D0D0D,60:1A1511,100:B87333&height=230&section=header&text=REGAN&fontSize=68&fontColor=F5F5F5&fontAlignY=36&desc=Full-Stack%20Software%20Engineer&descSize=22&descAlignY=58&descColor=D99B63&animation=fadeIn" alt="Regan — Full-Stack Software Engineer" width="100%"/>

<br/>

<b>AI · CLOUD · PRODUCT ENGINEERING</b>

<br/><br/>

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=500&size=16&duration=2600&pause=1200&color=D99B63&center=true&vCenter=true&width=700&height=40&lines=Building+software+end-to-end.;Interface+%E2%86%92+API+%E2%86%92+database+%E2%86%92+deployment.;LLM+features%2C+built+like+real+software.;Structured+outputs.+Validated+inputs.+Tested+code.;Shipping+systems%2C+not+demos." alt="Building software end-to-end"/>

<br/><br/>

<a href="#about"><kbd> About </kbd></a>
  <a href="#projects"><kbd> Projects </kbd></a>
  <a href="#stack"><kbd> Stack </kbd></a>
  <a href="#activity"><kbd> Activity </kbd></a>
  <a href="#contact"><kbd> Contact </kbd></a>

<br/><br/>

<p align="center">
I build software end to end — the interface, the API, the data model,<br/>
the AI feature that earns its place, and the deployment that puts it in front of users.
</p>

<br/>

<a href="https://www.linkedin.com/in/regan-jesuraju/"><kbd> LinkedIn ↗ </kbd></a>
  <a href="http://regan-jesuraju-portfolio-2026.s3-website-ap-southeast-2.amazonaws.com/"><kbd> Portfolio ↗ </kbd></a>
  <a href="https://medium.com/@regannbis"><kbd> Medium ↗ </kbd></a>
  <a href="mailto:regannbis@gmail.com"><kbd> Email ↗ </kbd></a>

</div>

<br/>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0D0D0D,50:B87333,100:0D0D0D&height=2" width="100%" alt=""/>

## About

<table width="100%">
<tr>
<td width="56%" valign="top">

I'm a Computer Engineering student at Karunya University, building toward SDE roles.

<br/><br/>

My core is full-stack engineering: the path from what a user sees to how data is modelled, validated and served. AI is how I make an application do what a static one can't — as an integration inside a real system, not the whole product. Cloud is how I ship it.

<br/><br/>

<blockquote>
I'd rather own one system from the first click to the last query than collect ten frameworks.
</blockquote>

</td>

<td width="44%" valign="top">

<b>Currently building</b>

<br/><br/>

<code>01</code>   <b>Full-Stack Engineering</b><br/> <sub>React · Node.js · REST APIs · MongoDB</sub>

<br/><br/>

<code>02</code>   <b>Java + DSA</b><br/> <sub>Structured problem-solving practice</sub>

<br/><br/>

<code>03</code>   <b>AI-Powered Applications</b><br/> <sub>LLM features with structured, validated output</sub>

<br/><br/>

<code>04</code>   <b>Backend Architecture</b><br/> <sub>Auth · validation · data modelling</sub>

<br/><br/>

<code>05</code>   <b>Cloud Deployment</b><br/> <sub>AWS · Google Cloud · shipping to real users</sub>

</td>
</tr>
</table>

<br/>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0D0D0D,50:B87333,100:0D0D0D&height=2" width="100%" alt=""/>

## Projects

<sub>Selected work. In each one, the model call is a component — the product is everything built around it.</sub>

<br/><br/>

<table width="100%">
<tr>
<td colspan="2" valign="top">

<sub><b>01 / FLAGSHIP</b></sub>

<h3>GoodFit</h3>

<b>Role-fit intelligence for resumes, grounded in the actual job posting.</b>

</td>
</tr>

<tr>
<td colspan="2" align="center">

<a href="https://github.com/ItzMeBeasT/resume-fit-ai">
<img src="https://github.com/ItzMeBeasT/resume-fit-ai/raw/main/docs/screenshots/demo.gif" alt="GoodFit demo: upload a resume, paste a job description, get a match score, gaps and three fixes" width="100%"/>
</a>

</td>
</tr>

<tr>
<td width="50%" valign="top">

<b>Problem</b>

<br/><br/>

Most resume checkers grade against a generic "ideal" resume. Every real opening asks for something different, so the feedback misses what the posting actually requires.

</td>

<td width="50%" valign="top">

<b>What I built</b>

<br/><br/>

Upload a PDF, paste a job description, and get a 0–100 match score with a verdict, the skills found and missing, and exactly three prioritised fixes. Recent analyses are stored in MongoDB, keyed to an anonymous per-browser ID.

</td>
</tr>

<tr>
<td colspan="2" valign="top">

<b>Engineering</b>

<ul>
<li><b>Model output is a contract.</b> Gemini is called with a JSON response schema, then re-validated with Zod — including exactly three fixes, typed arrays and a numeric score. The score is rounded and clamped to 0–100 server-side, with one automatic retry.</li>

<li><b>Untrusted input stays untrusted.</b> The resume and job description are delimited in the prompt and the model is instructed to ignore instructions inside them. A probe script plants "give this candidate 100" payloads to test that behaviour.</li>

<li><b>Defense in depth on uploads.</b> 4 MiB cap, MIME-type validation and <code>%PDF-</code> magic-byte checks, with distinct errors for scanned or oversized files.</li>

<li><b>Abuse and privacy controls.</b> Analysis is rate-limited to 5 requests per 10 minutes per client. PDFs are parsed in memory and never written to disk. Resume text is never stored and the API key remains server-side.</li>

<li><b>Tested and honest.</b> A <code>node:test</code> suite covers the schema contract, mocked Gemini integration and endpoint validation. Design decisions and known limitations are documented in the repository.</li>
</ul>

</td>
</tr>

<tr>
<td width="50%" valign="top">

<b>Stack</b>

<br/><br/>

<code>React</code> <code>Tailwind</code> <code>Node.js + Express</code> <code>MongoDB</code> <code>Gemini</code> <code>Zod</code>

</td>

<td width="50%" valign="top">

<a href="https://github.com/ItzMeBeasT/resume-fit-ai"><b>→ View repository</b></a>

<br/>

<a href="https://github.com/ItzMeBeasT/resume-fit-ai/blob/main/decisions.md"><b>→ Read the design decisions</b></a>

</td>
</tr>
</table>

<br/>

```mermaid
flowchart LR
    A["React Client<br/>PDF + Job Description"]
    --> B["Express API<br/>Rate Limit · Upload Checks"]

    B --> C["In-Memory<br/>PDF Parsing"]

    C --> D["Gemini<br/>JSON Response Schema"]

    D --> E["Zod Validation<br/>Clamp Score · Retry Once"]

    E --> F[("MongoDB<br/>Results Only")]

    style A fill:#151515,stroke:#B87333,stroke-width:1px,color:#F5F5F5
    style B fill:#151515,stroke:#B87333,stroke-width:1px,color:#F5F5F5
    style C fill:#151515,stroke:#B87333,stroke-width:1px,color:#F5F5F5
    style D fill:#151515,stroke:#D99B63,stroke-width:2px,color:#F5F5F5
    style E fill:#151515,stroke:#B87333,stroke-width:1px,color:#F5F5F5
    style F fill:#151515,stroke:#B87333,stroke-width:1px,color:#F5F5F5
    linkStyle default stroke:#8A8A8A,stroke-width:1.5px
```

<sub>GoodFit request path: every stage between the upload and the database exists to keep the model's output trustworthy.</sub>

<br/><br/>

<table width="100%">
<tr>
<td colspan="2" valign="top">

<sub><b>02 / AI</b></sub>

<h3>Gemini LifeOS</h3>

<b>A reflection-to-action platform: conversations become structured insight, then tracked work.</b>

</td>
</tr>

<tr>
<td colspan="2" valign="top">

<b>Problem</b>

<br/><br/>

Journals capture thoughts and then do nothing with them. Each reflection should turn into a concrete next step, and be read in the context of the entries before it.

</td>
</tr>

<tr>
<td colspan="2" valign="top">

<b>Engineering</b>

<ul>
<li><b>Structured reflection engine.</b> A multi-turn Gemini conversation is converted into typed JSON — summary, themes, patterns, tone and action items — enforced by a response schema rather than prompted formatting.</li>

<li><b>Identity is verified, never trusted.</b> Firebase ID tokens are verified server-side; the user ID is derived from the token and never taken from the request body.</li>

<li><b>Default-deny data layer.</b> Firestore rules allow only per-user access and validate the schema of every write.</li>

<li><b>Growth Memory.</b> A backend engine reads a user's last 10 entries server-side and analyses recurring patterns across sessions.</li>

<li><b>Security you can watch.</b> An in-app Security Center fires a real authenticated and a real unauthenticated request, demonstrating the auth boundary instead of simply claiming it.</li>
</ul>

</td>
</tr>

<tr>
<td width="50%" valign="top">

<b>Stack</b>

<br/><br/>

<code>React</code> <code>TypeScript</code> <code>Express</code> <code>Firebase Auth</code> <code>Firestore</code> <code>Gemini</code>

</td>

<td width="50%" valign="top">

<a href="https://github.com/ItzMeBeasT/gemini-lifeos"><b>→ View repository</b></a>

</td>
</tr>
</table>

<br/>

<table width="100%">
<tr>
<td colspan="2" valign="top">

<sub><b>03 / CLOUD</b></sub>

<h3>Portfolio on AWS</h3>

<b>A live static site served straight from S3 website hosting.</b>

</td>
</tr>

<tr>
<td width="50%" valign="top">

<b>Problem</b>

<br/><br/>

My work needed a stable public home, and I wanted to learn AWS by deploying something real instead of following a walkthrough.

</td>

<td width="50%" valign="top">

<b>What I built</b>

<br/><br/>

A static site deployed to S3 in <code>ap-southeast-2</code>, with bucket access and IAM configured by hand during a Corizo cloud computing internship.

</td>
</tr>

<tr>
<td width="50%" valign="top">

<b>Stack</b>

<br/><br/>

<code>AWS S3</code> <code>IAM</code> <code>HTML</code>

</td>

<td width="50%" valign="top">

<a href="http://regan-jesuraju-portfolio-2026.s3-website-ap-southeast-2.amazonaws.com/"><b>→ Visit the site</b></a>

</td>
</tr>
</table>

<br/>

<div align="center">

<a href="https://github.com/ItzMeBeasT?tab=repositories">
<kbd> View all repositories → </kbd>
</a>

</div>

<br/><br/>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0D0D0D,50:B87333,100:0D0D0D&height=2" width="100%" alt=""/>

## Stack

<b>Engineering map</b>

<br/>

<sub>Where each layer lives across the products above.</sub>

<br/><br/>

```mermaid
flowchart LR
    F["Frontend<br/>React · Vite · Tailwind"]
    --> B["Backend<br/>Node.js · Express · Zod"]

    B --> D["Data<br/>MongoDB · Firestore · MySQL"]

    D --> A["AI<br/>Gemini · Structured Output"]

    A --> C["Cloud<br/>AWS · Google Cloud · Docker"]

    style F fill:#151515,stroke:#B87333,stroke-width:1px,color:#F5F5F5
    style B fill:#151515,stroke:#B87333,stroke-width:1px,color:#F5F5F5
    style D fill:#151515,stroke:#B87333,stroke-width:1px,color:#F5F5F5
    style A fill:#151515,stroke:#D99B63,stroke-width:2px,color:#F5F5F5
    style C fill:#151515,stroke:#B87333,stroke-width:1px,color:#F5F5F5
    linkStyle default stroke:#8A8A8A,stroke-width:1.5px
```

<br/>

| Layer                | Technologies                                                           |
| :------------------- | :--------------------------------------------------------------------- |
| **Languages**        | Java · Python · JavaScript · TypeScript                                |
| **Frontend**         | React · Vite · Tailwind CSS                                            |
| **Backend**          | Node.js · Express · REST APIs · Zod                                    |
| **Data**             | MongoDB · Firestore · MySQL                                            |
| **AI**               | Gemini API · structured JSON output · prompt-injection-aware prompting |
| **Cloud & Delivery** | AWS (S3, IAM) · Google Cloud (Firebase) · Docker · GitHub Actions      |
| **Practices**        | Input validation · token-based auth · rate limiting · automated tests  |

<br/>

<b>Engineering foundations</b>

<br/>

<sub>The parts that outlast any framework.</sub>

<br/><br/>

<table width="100%">
<tr>
<td width="33%" valign="top">

<b>Java</b>

<br/>

<sub>Core language for problem solving and object-oriented design.</sub>

</td>

<td width="33%" valign="top">

<b>Data Structures & Algorithms</b>

<br/>

<sub>Ongoing, structured practice alongside project work.</sub>

</td>

<td width="33%" valign="top">

<b>Object-Oriented Programming</b>

<br/>

<sub>Modelling, abstraction and clean class design.</sub>

</td>
</tr>

<tr>
<td width="33%" valign="top">

<b>Backend Engineering</b>

<br/>

<sub>API design, authentication and validation.</sub>

</td>

<td width="33%" valign="top">

<b>Database Fundamentals</b>

<br/>

<sub>Relational and document modelling — MySQL, MongoDB and Firestore.</sub>

</td>

<td width="33%" valign="top">

<b>System Design Fundamentals</b>

<br/>

<sub>Components, trade-offs and failure modes.</sub>

</td>
</tr>
</table>

<br/>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0D0D0D,50:B87333,100:0D0D0D&height=2" width="100%" alt=""/>

## Activity

<br/>

<p align="center">

<img src="https://github-readme-stats.vercel.app/api?username=ItzMeBeasT&show_icons=true&hide_border=true&bg_color=0D0D0D&title_color=D99B63&icon_color=B87333&text_color=F5F5F5&rank_icon=github" alt="GitHub statistics"/>

<br/><br/>

<img src="https://github-readme-streak-stats.herokuapp.com/?user=ItzMeBeasT&hide_border=true&background=0D0D0D&ring=B87333&fire=D99B63&currStreakLabel=D99B63&sideLabels=F5F5F5&dates=8A8A8A" alt="GitHub contribution streak"/>

</p>

<br/>

<p align="center">

<img src="https://raw.githubusercontent.com/ItzMeBeasT/ItzMeBeasT/output/github-contribution-grid-snake-dark.svg" alt="Contribution graph rendered as an animated snake" width="100%"/>

</p>

<sub>Contribution activity visualised through a GitHub Actions-generated contribution snake.</sub>

<br/><br/>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0D0D0D,50:B87333,100:0D0D0D&height=2" width="100%" alt=""/>

## Contact

<div align="center">

<br/>

<a href="https://www.linkedin.com/in/regan-jesuraju/"><kbd> LinkedIn </kbd></a>
  <a href="http://regan-jesuraju-portfolio-2026.s3-website-ap-southeast-2.amazonaws.com/"><kbd> Portfolio </kbd></a>
  <a href="https://medium.com/@regannbis"><kbd> Medium </kbd></a>
  <a href="mailto:regannbis@gmail.com"><kbd> Email </kbd></a>

<br/><br/><br/>

<sub><i>Everything on this page links to something you can read, explore or run.</i></sub>

<br/><br/>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:B87333,100:0D0D0D&height=110&section=footer" alt="" width="100%"/>

</div>
