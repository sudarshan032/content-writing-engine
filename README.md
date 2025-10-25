# 🤖 AI-Powered Content Writing Engine for Instagram Creators  
### _Automated Reel Idea Generator

![n8n](https://img.shields.io/badge/Automation-n8n-orange?logo=n8n)
![AI Model](https://img.shields.io/badge/AI-Gemini%202.5%20Flash-blue)
![Data Source](https://img.shields.io/badge/Data-Google%20Sheets-green?logo=google-sheets)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

## 🧠 Overview

This project automates the **daily content ideation process** for Instagram creator using a fully integrated **n8n + Gemini AI pipeline**.  
It researches viral topics, scrapes competitor posts, analyzes brand persona data, and generates **20 complete 30–40s Instagram Reel scripts** every morning at 10 AM.

### 🎯 Key Objectives
- Research **10 viral parenting/lifestyle news stories** daily  
- Scrape **recent competitor Instagram content**  
- Use **brand persona insights** to generate unique ideas  
- Deliver **AI-written Reel scripts (with hooks, visuals, CTAs & hashtags)**  
- Run **autonomously every day at 10 AM**

## 🏗️ Architecture

### ⚙️ Workflow Components
| Step | Function | Node Type |
|------|-----------|-----------|
| 1️⃣ | **Trigger** — Starts workflow daily at 10 AM | `Schedule Trigger` |
| 2️⃣ | **Read Competitors & Persona** | `Google Sheets` |
| 3️⃣ | **Fetch Viral News (RSS)** | `RSS Feed Read` |
| 4️⃣ | **Limit Articles (10)** | `Limit` |
| 5️⃣ | **Scrape Instagram via Apify** | `HTTP Request` |
| 6️⃣ | **Format Competitor Data** | `Set` |
| 7️⃣ | **Aggregate News & Competitor Data** | `Aggregate` + `Merge` |
| 8️⃣ | **Format All Data for AI** | `Code Node (data formatter)` |
| 9️⃣ | **Generate Ideas & Scripts (AI)** | `Google Gemini 2.5 Flash` |
| 🔟 | **Parse AI Output** | `Code Node (final ideas)` |

<img width="1469" height="283" alt="Screenshot 2025-10-25 162558" src="https://github.com/user-attachments/assets/e510e666-1b44-497f-af56-90ac68031dfa" />

## 🧾 Data Sources

### 🧍‍♀️ Brand Persona & Competitors
Stored in Google Sheet (example):

| Name | Instagram Handle | Followers | Location | Key Content Focus | Instagram URL |
|------|------------------|------------|-----------|-------------------|----------------|
| Neha Dhupia | @nehadhupia | 7.1M | India | Parenting, Lifestyle, Fitness | [Link](https://www.instagram.com/nehadhupia/) |
| Mandira Bedi | @mandirabedi | 2M | India | Parenting, Wellness, Fitness | [Link](https://www.instagram.com/mandirabedi/) |
| Sameera Reddy | @reddysameera | 1.9M | Goa | Mom Hacks, Family | [Link](https://www.instagram.com/reddysameera/) |
| ... | ... | ... | ... | ... | ... |

### 🌍 Viral News Source
- google news
- RSS news

### Response

<img width="585" height="513" alt="Screenshot 2025-10-25 162334" src="https://github.com/user-attachments/assets/2a8907a0-c932-4de7-adcb-61f4d042e1c9" />


### Resources
[N8N docs](https://docs.n8n.io/)
[Apify](https://apify.com/)
