# 👋 Hi, I'm Saqib Younas 

# Associate Software Engineer | Full Stack Developer    
       
---
**How to reach me:**   
 
<p align="left"> 
  <a href="https://portfolio-github-io-seven-gamma.vercel.app/" target="_blank">
    <img src="https://img.shields.io/badge/Portfolio-000000?style=for-the- badge&logo=vercel&logoColor=white" alt="Portfolio"/> 
  </a>
  <a  href="https://www.linkedin.com/in/muhammad-saqib-younas-0123aa329" target="_blank">
    <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/>
  </a>
  <a href="https://github.com/SaqibYounas" target="_blank">
    <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub"/>
  </a>
</p>

**Email:** saqibyounas.dev@gmail.com

**Pronouns:** He/Him
**Fun fact:** I enjoy solving real-world problems by converting ideas into interactive web apps. 

---

### 🎯 Professional Summary

Associate Software Engineer and final year BSIT student with hands on experience building and deploying scalable, production-ready full-stack applications using React, Next.js, TypeScript, Tailwind CSS, Node.js, Express.js, NestJS, MongoDB, and PostgreSQL.

Currently working at KCloudAI as an Associate Software Engineer, contributing to production e-commerce applications, POS systems, Salesforce B2B Commerce solutions, backend APIs, and business integrations. Experienced in transforming Figma designs into responsive production interfaces and developing scalable REST APIs, authentication systems, database driven features, and real-time functionality.

Experienced in building AI-powered applications and RAG (Retrieval-Augmented Generation) systems, including vector search and AI business assistants. Strong experience in Salesforce B2B Commerce, Apex, SOQL, Connect Search API optimization, caching, rate limiting, circuit breakers, and configuration-driven API protection.

Skilled in database design, query optimization, search optimization, SEO, API integrations, real-time communication, and production problem solving. Experienced with Docker, AWS EC2, S3, RDS, Nginx, CI/CD, and Vercel for containerized application deployment and reliable production delivery.

Passionate about building maintainable software, solving real-world business problems, optimizing application performance, and continuously learning modern technologies.

---
## 📊 GitHub Statistics

[![GitHub Streak](https://github-readme-streak-stats.herokuapp.com?user=SaqibYounas)](https://git.io/streak-stats)

---

### 🎓 Education

**Bachelor of Science in Information Technology (BSIT)**
*The Superior University, Lahore*
Start: October 2023 — 🎓 Expected: 2027

---

### 💼 Experience

- **KCloudAI — Associate Software Engineer**
     Onsite | 📅 Mar 2026 – Present
  - Working on **production e-commerce applications** using Next.js, React, TypeScript, NestJS, and Salesforce B2B Commerce.
  - Developing responsive and production-ready **e-commerce UIs** from Figma designs using Next.js, React, and Tailwind CSS.
  - Building scalable **backend APIs, authentication, and business logic** using Node.js and NestJS.
  - Developing and maintaining a **POS system** with product, pricing, sales, inventory, and business workflow integrations.
  - Contributing to **ERP integration** and business workflows across products, inventory, orders, customers, and store operations.
  - Designed and implemented a layered **Salesforce Connect Search API protection architecture** using input validation, caching, token-based controls, rate limiting, circuit breakers, and audit telemetry.
  - Implemented **configuration-driven Salesforce controls** using Custom Metadata, allowing API limits and protection settings to be changed without code deployment.
  - Worked with **Apex, SOQL, Salesforce B2B Commerce, Connect Search API, Platform Events, and Custom Metadata** on production features.
  - Developed backend solutions for **location-based pickup shop filtering**, combining country-level filtering with latitude/longitude logic.
  - Designed database-driven **courier tracking functionality**, mapping tracking numbers to courier websites for direct order tracking.
  - Investigated and resolved **SEO and Google indexing issues**, implementing backend noindex/nofollow handling for restricted product pages.
  - Built responsive **mobile filtering experiences** and resolved production pagination and UI issues.
  - Worked with **PostgreSQL, MongoDB, TypeORM, REST APIs, and database relationships** for production applications.
  - Implemented and integrated **AI/RAG functionality**, including vector search and natural-language business assistants.
  - Dockerized applications and supported **AWS EC2, Nginx, CI/CD, S3, and RDS**-based deployments.
  - Collaborated with the development team to troubleshoot and resolve production issues across **frontend, backend, Salesforce, database, API, and infrastructure layers**.
  - Performed functional and regression testing to ensure reliable production releases and maintainable software.

- **Xpert Prime — MERN Stack Developer Intern**
  Onsite | 📅 Nov 2025 – Mar 2026
  - Developed and managed end-to-end web solutions using the MERN stack for real client projects.
  - Direct client coordination to gather requirements and deliver custom IT solutions.
  - Built scalable dashboards with advanced role based access control (RBAC).
  - Led integration of third party services including Stripe and real time notifications via Socket.io.
  - Deployed containerized applications on **AWS EC2** using **Docker**, with full **CI/CD pipelines**.
  - Utilized **AWS S3** for file storage and **AWS RDS** for relational database management.
  - Managed project lifecycles from database design to final deployment on EC2 and Vercel.

- **Appaura — Frontend Developer Intern**
  Remote | 📅 Jul 2025 – Sep 2025
  - Built responsive web interfaces using **React.js** and **Next.js**.
  - Translated design mockups into functional, pixel perfect components.
  - Debugged and optimized frontend code for performance.
  - Integrated REST APIs and participated in code reviews.

- **TechTommy — Backend Developer Intern**
  Remote | 📅 Aug 2025 – Sep 2025
  - Created REST APIs using **Node.js**, **Express.js**, and **PostgreSQL**.
  - Designed and implemented database schemas for scalability and performance.
  - Integrated backend services with frontend features.
  - Worked on deployment, containerization with **Docker**, and Git version control.

---



Updated portfolio sections
The Problem (revised)
Category pages on the Canadian storefront rendered empty. A URL such as /ca/category/Automation/Accessories returned a valid page with working header, breadcrumbs and layout — but no products. The same category opened by its record ID worked correctly.

The failure was silent: no error surfaced to the user or the logs. The page simply showed nothing where a product grid should be.

Critically, the ID-based URLs were already indexed and ranking in production. They appeared in organic search results and in paid campaign landing pages. This ruled out the obvious fix of retiring them in favour of clean slugs — any URL that stopped resolving would render a blank page and forfeit its existing ranking. Both URL forms had to keep working indefinitely.

Constraints (revised)
Three constraints shaped the solution.

Every existing URL had to keep resolving. ID-based URLs carried live rankings and live ad spend. Breaking them was not an option, so the work was additive: introduce readable slugs without retiring anything.

Redirects were unavailable. The platform commits an HTTP 200 response and the page shell before any custom code executes, so a 301 — the conventional answer to duplicate URLs — cannot be issued from within Salesforce.

Resolution had to stay conditional. Correctness could not come at the cost of an extra query on the pages that already worked.

The Duplicate-Content Problem (new section)
Keeping every URL alive created a second, subtler problem. A single category became reachable at five or more distinct addresses — ID-based, slug-based, lower-cased, prefixed and trailing-slash variants — each serving identical content.

To a search engine these are separate pages. The result is self-competition: ranking signals that should accumulate on one authoritative URL are instead divided among several near-identical ones, and the engine picks a winner on its own — frequently the least readable option, the raw ID URL.

With redirects ruled out by the platform, canonical consolidation was the available mechanism. Every alternate URL declares the configured slug URL as its canonical, and the slug URL declares itself — a self-referencing canonical, which search engines weigh more heavily than a one-directional claim.

Because a canonical is a hint rather than a directive, the surrounding signals had to agree with it. Internal links were the weak point: breadcrumbs on product pages emitted ID-based URLs while the tag nominated the slug, and the platform's own language-alternate tags were generated from the requested path rather than the canonical one. Both were corrected so that the tag, the internal links and the language annotations all name the same address.




### 📜 Certifications

**AWS (Amazon Web Services)**
- AWS Cloud Practitioner Essentials — *Issued Dec 2025*

**HackerRank Certifications**
- JavaScript (Basic) — *Issued Oct 2025*
- SQL (Basic) — *Issued Sep 2025*
- SQL (Intermediate) — *Issued Sep 2025*
- CSS (Basic) — *Issued Sep 2025*

---

## 🛠️ Tech Stack

### Frontend
![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?logo=react&logoColor=61DAFB)
![Next.js](https://img.shields.io/badge/Next.js-000000?logo=nextdotjs&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/TailwindCSS-06B6D4?logo=tailwindcss&logoColor=white)
![Bootstrap](https://img.shields.io/badge/Bootstrap-7952B3?logo=bootstrap&logoColor=white)
![Redux](https://img.shields.io/badge/Redux-764ABC?logo=redux&logoColor=white)
![Zustand](https://img.shields.io/badge/Zustand-000000?logo=zustand&logoColor=white)

### Backend & APIs
![Node.js](https://img.shields.io/badge/Node.js-339933?logo=nodedotjs&logoColor=white)
![Express.js](https://img.shields.io/badge/Express.js-000000?logo=express&logoColor=white)
![NestJS](https://img.shields.io/badge/NestJS-E0234E?logo=nestjs&logoColor=white)
![Django](https://img.shields.io/badge/Django-092E20?logo=django&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?logo=fastapi&logoColor=white)
![REST API](https://img.shields.io/badge/REST_API-FF69B4?logo=api&logoColor=white)
![GraphQL](https://img.shields.io/badge/GraphQL-E10098?logo=graphql&logoColor=white)
![Socket.io](https://img.shields.io/badge/Socket.io-010101?logo=socket.io&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-000000?logo=jsonwebtokens&logoColor=white)
![OAuth2](https://img.shields.io/badge/OAuth2.0-0066A1?logo=auth0&logoColor=white)
![Prisma](https://img.shields.io/badge/Prisma-2D3748?logo=prisma&logoColor=white)
![Mongoose](https://img.shields.io/badge/Mongoose-47A248?logo=mongodb&logoColor=white)

### Databases
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?logo=mongodb&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?logo=postgresql&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?logo=mysql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?logo=redis&logoColor=white)

### DevOps & Cloud
![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?logo=github&logoColor=white)
![CI/CD](https://img.shields.io/badge/GitHub_Actions-2088FF?logo=githubactions&logoColor=white)
![AWS EC2](https://img.shields.io/badge/AWS_EC2-FF9900?logo=amazonaws&logoColor=white)
![AWS S3](https://img.shields.io/badge/AWS_S3-569A31?logo=amazons3&logoColor=white)
![AWS RDS](https://img.shields.io/badge/AWS_RDS-527FFF?logo=amazonrds&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?logo=amazonaws&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?logo=vercel&logoColor=white)
![Railway](https://img.shields.io/badge/Railway-000000?logo=railway&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?logo=nginx&logoColor=white)

### Automation & Integrations
![n8n](https://img.shields.io/badge/n8n-000000?style=flat&logo=n8n)
![ChatGPT API](https://img.shields.io/badge/ChatGPT_API-00C878?style=flat&logo=openai)

### Testing
![Jest](https://img.shields.io/badge/Jest-C21325?logo=jest&logoColor=white)
![Vitest](https://img.shields.io/badge/Vitest-6E9F18?logo=vitest&logoColor=white)
![Postman](https://img.shields.io/badge/Postman-FF6C37?logo=postman&logoColor=white)
![RTL](https://img.shields.io/badge/React_Testing_Library-E33332?logo=testinglibrary&logoColor=white)

---

### 🤝 Soft Skills
Problem Solving
Communication
Teamwork
