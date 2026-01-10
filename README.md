<!-- =========================
     GOOGLE THEMED PROFILE
     AI DATA ANALYST
     ========================= -->

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=rounded&height=160&text=Hi,%20I%27m%20<<YOUR%20NAME>>&fontSize=42&desc=AI%20Data%20Analyst%20%7C%20Insights%20to%20Impact&descSize=18&animation=fadeIn" />
</p>

<!-- Google-like logo text -->
<h1 align="center" style="font-family: Product Sans, Arial;">
  <span style="color:#4285F4">G</span><span style="color:#EA4335">o</span><span style="color:#FBBC05">o</span><span style="color:#4285F4">g</span><span style="color:#34A853">l</span><span style="color:#EA4335">e</span>
  <span style="color:#5f6368"> • Profile</span>
</h1>

<p align="center">
  <b>AI Data Analyst</b> • SQL • Python • BI • ML • Experimentation • Dashboards
</p>

<!-- "Search bar" (fake) -->
<p align="center">
  <img alt="Search Bar" src="https://readme-typing-svg.demolab.com?font=Arial&size=18&pause=1200&color=5F6368&center=true&vCenter=true&width=780&lines=Search+my+profile...;AI+Data+Analyst+%7C+Data+Storytelling+%7C+Model+to+Metric;SQL+%2B+Python+%2B+Power+BI+%2B+Machine+Learning;Open+to+AI%2FData+roles+%7C+Remote+%7C+<<YOUR%20CITY>>" />
</p>

<!-- Google buttons -->
<p align="center">
  <a href="<<YOUR_PORTFOLIO_LINK>>"><img src="https://img.shields.io/badge/Google%20Search%20Me-4285F4?style=for-the-badge&logo=google&logoColor=white"/></a>
  <a href="<<YOUR_RESUME_LINK>>"><img src="https://img.shields.io/badge/I%27m%20Feeling%20Lucky-34A853?style=for-the-badge&logo=google&logoColor=white"/></a>
</p>

<br/>

<!-- Google "Knowledge Panel" style -->
<table align="center">
<tr>
<td width="60%">
  
## 🔎 About (Knowledge Panel)

- 📌 Role: **AI Data Analyst**
- 🧠 Focus: **forecasting, segmentation, churn, anomaly detection, KPI design**
- 📊 I build: **dashboards + models + decision-ready insights**
- 🧪 I love: **A/B testing, causal thinking, clean metrics**
- 🧰 Tools: **Python, SQL, Power BI/Tableau, Excel, Git, BigQuery/Snowflake**
- 🌱 Currently learning: **<<TOPIC (e.g., causal inference / dbt / MLOps)>>**
- 🤝 Open to: **AI/Data Analyst roles, freelance analytics, collabs**

</td>
<td width="40%">

## 📌 Quick Links
- 🌐 Portfolio: **<<LINK>>**
- 🧾 Resume: **<<LINK>>**
- ✍️ Blog: **<<LINK>>**
- 💼 LinkedIn: **<<LINK>>**
- 🧪 Kaggle: **<<LINK>>**
- 📫 Email: **<<EMAIL>>**

</td>
</tr>
</table>

---

## 🧩 “Google Features” (What I offer)

<table>
<tr>
<td width="33%">
  
### 🗺️ Maps (Business Insight)
I find *where* performance changes:
- geo / cohort analysis  
- funnel drop-offs  
- attribution support  

</td>
<td width="33%">

### 📈 Trends (What’s rising?)
I detect patterns:
- time-series forecasting  
- anomaly detection  
- seasonality & drivers  

</td>
<td width="33%">

### 🤖 Assistant (Decision Support)
I automate insight delivery:
- KPI alerts  
- auto reports  
- narrative summaries  

</td>
</tr>
</table>

---

## 📰 Latest Blog Posts (Auto-updating)

<!-- BLOG-POST-LIST:START -->
- Coming soon: **Add your blog RSS to auto-update this section**
<!-- BLOG-POST-LIST:END -->

✅ To auto-fill this: use GitHub Action **"blog-post-workflow"** (steps below)

---

## 🧰 Tech Stack

<p>
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/SQL-000000?style=flat&logo=postgresql&logoColor=white"/>
  <img src="https://img.shields.io/badge/Power%20BI-F2C811?style=flat&logo=powerbi&logoColor=000"/>
  <img src="https://img.shields.io/badge/Tableau-E97627?style=flat&logo=tableau&logoColor=white"/>
  <img src="https://img.shields.io/badge/BigQuery-4285F4?style=flat&logo=googlecloud&logoColor=white"/>
  <img src="https://img.shields.io/badge/Snowflake-29B5E8?style=flat&logo=snowflake&logoColor=white"/>
  <img src="https://img.shields.io/badge/scikit--learn-F7931E?style=flat&logo=scikitlearn&logoColor=white"/>
</p>

---

## 📌 Featured Projects (Pin these)

- ⭐ **<<Project 1: e.g., Churn Prediction>>** — brief impact line  
- ⭐ **<<Project 2: e.g., Sales Forecasting>>** — brief impact line  
- ⭐ **<<Project 3: e.g., Customer Segmentation>>** — brief impact line  
- ⭐ **<<Project 4: e.g., Power BI Executive Dashboard>>** — brief impact line  

---

## 📊 GitHub Stats (Optional)

<p align="center">
  <img height="160" src="https://github-readme-stats.vercel.app/api?username=<<YOUR_USERNAME>>&show_icons=true&rank_icon=github" />
  <img height="160" src="https://github-readme-streak-stats.herokuapp.com/?user=<<YOUR_USERNAME>>" />
</p>

<p align="center">
  <img height="180" src="https://github-readme-stats.vercel.app/api/top-langs/?username=<<YOUR_USERNAME>>&layout=compact" />
</p>

---

## ✅ How to enable Blog Auto-Update (2 minutes)

1) Create a file at: `.github/workflows/blog-post-workflow.yml`  
2) Paste this:

```yaml
name: Latest blog posts workflow
on:
  schedule:
    - cron: '0 */12 * * *'
  workflow_dispatch:

jobs:
  update-readme-with-blog:
    name: Update this repo's README with latest blog posts
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: gautamkrishnar/blog-post-workflow@v1
        with:
          feed_list: "<<YOUR_RSS_FEED_URL>>"
