<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/banner-dark.svg">
  <img src="assets/banner-light.svg" alt="Omar Elgenidy: Data Science Student, AI & Robotics, Full-Stack Developer" width="100%">
</picture>

<p align="center">
  <a href="https://www.linkedin.com/in/omar-elgenidy-405231360/"><img src="https://img.shields.io/badge/LinkedIn-Omar%20Elgenidy-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="mailto:omarelgenidy727@gmail.com"><img src="https://img.shields.io/badge/Email-omarelgenidy727%40gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"></a>
  <img src="https://img.shields.io/badge/Based%20in-Cairo%2C%20Egypt-2A78D6?style=for-the-badge&logo=googlemaps&logoColor=white" alt="Cairo, Egypt">
</p>

## About me

I'm a final-year **Computer Science student majoring in Data Science** at the German International University (GIU) in Cairo, and I spent my Spring 2026 semester at **GIU Berlin**.

I like projects where data, software and the physical world meet. Right now that means teaching a humanoid robot to show emotions with its voice and body. Before that, I built data pipelines over millions of records, payroll and booking backends, and relational databases with dozens of tables.

- 🤖 **Currently:** my bachelor thesis on emotional expression in humanoid robots (due January 2027)
- 📊 **Interested in:** machine learning, data engineering, human–robot interaction, backend systems
- 🎓 **Graduating:** July 2027

---

## 🤖 Current focus: Bachelor thesis

### Voice Meets Body: Evaluating Coherent Multimodal Emotional Expression in Humanoid Robots

*Supervised by Assoc. Prof. Nada Sharaf · GIU*

Can people recognise a robot's emotion better when its voice and body move together? I built everything needed to test that question on a real **UBTECH Yanshee** humanoid robot, and the user study is next.

| <h3>63</h3>study conditions | <h3>7</h3>emotions | <h3>21</h3>whole-body expressions | <h3>0</h3>issues in safety checks |
|:---:|:---:|:---:|:---:|

```mermaid
flowchart LR
    A["<b>Design</b><br/>7 emotions × 3 levels<br/>= 21 expressions + sounds"] --> B["<b>Verify</b><br/>URDF model checks<br/>kinematics · balance · collisions"]
    B --> C["<b>Run</b><br/>Python REST layer<br/>→ Yanshee robot"]
    C --> D["<b>Test</b><br/>sound · gesture · both<br/>= 63 conditions"]
    D -.->|next| E["<b>User study</b><br/>recognition accuracy"]
```

- **Expressions:** each emotion has 3 intensity levels, each based on a recognisable human reaction, with arm, head and leg movement plus eye and chest LED colours. Designs draw on body-language research and animation principles.
- **Safety first:** every pose is checked on UBTECH's own robot model with forward kinematics, a leg solver that keeps both feet flat, a balance check and collision checks. The control code also enforces joint, speed and battery limits and returns to neutral on any error.
- **Tooling:** a dependency-free Python control layer, a mock robot server for testing, and a one-click menu tool that finds every robot on the network.
- **Simulation:** expressions were first prototyped on Unitree G1, R1 and Go2 robots in Webots.

`Python` `REST APIs` `Webots` `URDF` `Forward Kinematics` `Human–Robot Interaction` `LaTeX`

---

## 🚀 Featured projects

### 📊 NYC Motor Vehicle Collisions Analytics

[![Repo](https://img.shields.io/badge/View%20repo-181717?style=flat-square&logo=github)](https://github.com/omarelgenidy2005/motor-vehicle-collisions-analysis)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white)
![Plotly](https://img.shields.io/badge/Plotly%20Dash-3F4F75?style=flat-square&logo=plotly&logoColor=white)
![Render](https://img.shields.io/badge/Deployed%20on%20Render-46E3B7?style=flat-square&logo=render&logoColor=black)

A team data-engineering project that turns NYC Open Data into an interactive dashboard.

- Merged **8M+ crash and person records** into a clean **4.8M-row dataset** with a 5-person team; I owned the post-merge cleaning.
- Co-built **7 interactive Plotly charts** (line, bar, heatmap, pie, map) driven by 6 filters, a year slider and text search.
- Deployed the dashboard publicly on Render with Gunicorn, serving a 95K-row sample.

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/nyc-heatmap-dark.png">
  <img src="assets/nyc-heatmap-light.png" alt="Heatmap of NYC collisions by day of week and hour. Crashes peak on weekday afternoons around 16:00 to 17:00 and are lowest between 02:00 and 05:00." width="100%">
</picture>

<sub>Made from the project's own sample data: crashes peak on weekday afternoons and drop sharply overnight.</sub>

### 💼 HR System: Payroll Processing & Execution

[![Repo](https://img.shields.io/badge/View%20repo-181717?style=flat-square&logo=github)](https://github.com/hr-platform-w25/Payroll-Subsystem)
![NestJS](https://img.shields.io/badge/NestJS-E0234E?style=flat-square&logo=nestjs&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)

The subsystem that takes a company's monthly payroll from draft to payout, with approvals at every step.

```mermaid
stateDiagram-v2
    direction LR
    [*] --> Draft
    Draft --> UnderReview: submit
    UnderReview --> PendingFinance: manager approves
    PendingFinance --> Approved: finance approves
    UnderReview --> Rejected
    PendingFinance --> Rejected
    Approved --> Locked: lock for payout
    Locked --> Unlocked: correction needed
    Unlocked --> Locked
```

- Wrote **10 DTOs with 270 validation rules** so bad payroll input (runs, payslips, bonuses, termination benefits) is rejected at the API.
- Built an exceptions page that flags employees with **missing bank details** before payout, so staff can fix them first.

### 🎟️ Online Event Ticketing System

[![Repo](https://img.shields.io/badge/View%20repo-181717?style=flat-square&logo=github)](https://github.com/yousef-89/event-ticketing-system)
![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=flat-square&logo=express&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-000000?style=flat-square&logo=jsonwebtokens&logoColor=white)

A full-stack MERN platform for browsing, booking and managing events.

- Serves **3 roles** (users, organizers, admins) through **24 REST endpoints** and **27 React components**.
- Protects every route with JWT authentication, bcrypt password hashing and role-based access control.
- Prevents overbooking by checking availability and updating ticket counts on every booking and cancellation.

### 🗄️ Gamified Educational Platform Database

[![Repo](https://img.shields.io/badge/View%20repo-181717?style=flat-square&logo=github)](https://github.com/yousef-89/DBM3)
![SQL Server](https://img.shields.io/badge/SQL%20Server-CC2927?style=flat-square&logo=microsoftsqlserver&logoColor=white)
![.NET](https://img.shields.io/badge/ASP.NET%20Core%20MVC-512BD4?style=flat-square&logo=dotnet&logoColor=white)

- Designed an EERD and a **44-table** relational schema with **52 foreign keys** for learners, courses, quests, badges and leaderboards.
- Wrote **57 T-SQL stored procedures** that power **14 ASP.NET Core MVC controllers**.

### 🍽️ Restaurant Reservation & Management System

[![Repo](https://img.shields.io/badge/View%20repo-181717?style=flat-square&logo=github)](https://github.com/omarelgenidy2005/restaurant-reservation-m2)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=flat-square&logo=express&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)
![Jest](https://img.shields.io/badge/Jest-C21325?style=flat-square&logo=jest&logoColor=white)

- A **52-endpoint** Express/MongoDB API, layered with services over the Repository and Factory patterns.
- Verified every core user story with **39 Jest tests** (25 unit, 6 integration, 8 end-to-end), written test-first.

---

## 🛠️ Tech stack

**Languages**

<img src="https://skillicons.dev/icons?i=py,js,ts,java,cpp,cs&perline=12" alt="Python, JavaScript, TypeScript, Java, C++, C#">

**Data, AI & robotics**

<img src="https://skillicons.dev/icons?i=pytorch,sklearn&perline=12" alt="PyTorch, scikit-learn"> &nbsp; Pandas · NumPy · Matplotlib · Plotly · Dash · Webots · URDF

**Backend & full-stack**

<img src="https://skillicons.dev/icons?i=nodejs,express,nestjs,nextjs,react,fastapi,dotnet&perline=12" alt="Node.js, Express, NestJS, Next.js, React, FastAPI, .NET">

**Databases**

<img src="https://skillicons.dev/icons?i=mongodb,postgres,redis&perline=12" alt="MongoDB, PostgreSQL, Redis"> &nbsp; SQL Server

**Tools & cloud**

<img src="https://skillicons.dev/icons?i=git,github,docker,aws,linux,postman,latex&perline=12" alt="Git, GitHub, Docker, AWS, Linux, Postman, LaTeX"> &nbsp; Power BI · Render

---

## 📫 Let's connect

I'm open to internships and graduate roles in **data science, machine learning, robotics and backend engineering**.

<p>
  <a href="https://www.linkedin.com/in/omar-elgenidy-405231360/"><img src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="mailto:omarelgenidy727@gmail.com"><img src="https://img.shields.io/badge/Email-Say%20hello-EA4335?style=flat-square&logo=gmail&logoColor=white" alt="Email"></a>
</p>
