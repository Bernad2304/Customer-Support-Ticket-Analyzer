<div align="center">

# 🎫 Customer Support Ticket Analyzer
## *Turning Raw Support Tickets Into Priority & Sentiment Insights — Pure Python, No Shortcuts*

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=22&pause=1000&color=2EA3F7&center=true&vCenter=true&width=750&lines=11+Support+Tickets+Analyzed+End-to-End;Raw+Data+%E2%86%92+Cleaned+%E2%86%92+Explored+%E2%86%92+Reported;Built+with+Core+Python+%E2%80%94+No+Libraries%2C+No+Shortcuts;Every+Line+of+Logic+Written+by+Hand" alt="Typing SVG" />

<img src="https://img.shields.io/badge/Python-3.10-blue?logo=python&logoColor=white">
<img src="https://img.shields.io/badge/Core%20Python-Dict%20%26%20Loops-yellow">
<img src="https://img.shields.io/badge/Status-Complete-success">
<img src="https://komarev.com/ghpvc/?username=Bernad2304&label=Repo%20Views&color=blueviolet&style=flat">

</div>

<br>

<div align="center">

## 🗺️ Table of Contents

| | | |
|:---:|:---:|:---:|
| 🎯 [Project Overview](#-project-overview) | 🔄 [The Process](#-the-process--how-this-came-together) | 🗂️ [Repository Structure](#-repository-structure) |
| 📊 [Dataset at a Glance](#-dataset-at-a-glance) | 🧭 [Methodology](#-methodology--section-by-section) | 💡 [Key Insights](#-key-insights) |
| 🔍 [Findings Deep-Dive](#-findings-deep-dive) | 🏢 [Business Value & Outlook](#-business-value--future-outlook) | 📸 [On Visualization](#-on-visualization) |
| 🧠 [Skills Applied](#-skills-applied) | 🚀 [About Me](#-about-me) | 📫 [Let's Connect](#-lets-connect) |

</div>

---

## 🎯 Project Overview

Every support team drowns in the same question: *what are our customers actually telling us, and where should we focus first?* This project tackles that question using nothing but core Python — no Pandas, no NumPy, no external libraries — to prove that solid analytical thinking doesn't require heavy tooling to produce real answers.

Starting from **10 raw customer support tickets**, this analyzer cleans messy real-world text (inconsistent punctuation, capitalization, spacing), accepts new tickets through live user input with validated priority levels, and then mines the cleaned data for patterns: which keywords show up most, how priority levels are distributed, which customer had the most to say, and what the full vocabulary of customer complaints actually looks like.

The point of building this in raw Python first — dictionaries, loops, string methods — was to genuinely understand *what* Pandas automates later, rather than treating it as a black box. Every function here (`clean_text`, `count_tickets_with_word`) was written by hand, tested against real edge cases, and debugged when it didn't behave as expected.

---

## 🔄 The Process — How This Came Together

### 🧹 Data Cleaning
Raw ticket descriptions arrived inconsistent — mixed case, stray punctuation, extra whitespace, and shorthand like "ok" instead of "okay." A custom `clean_text()` function was built to standardize every description: lowercasing, stripping `! . , ? -`, collapsing repeated spaces, and normalizing shorthand, so keyword matching downstream would actually be reliable.

### 📥 Data Collection & Expansion
Rather than working with a static, closed dataset, the analyzer accepts **live input** to add new tickets — with a validation loop that refuses to accept a Priority value outside High/Medium/Low and keeps re-prompting until it gets one. This mirrors how real intake systems have to handle imperfect human input.

### 🔍 Exploration & Keyword Analysis
With clean text in hand, the analysis moves into pattern-finding: counting how often specific sentiment-carrying words ("poor," "good," "slow," "excellent") appear across all tickets, tallying tickets by priority level, and identifying the single longest issue description by word count.

### 📚 Vocabulary Analysis
As a final layer, every unique word across all cleaned descriptions was collected into a set, giving a complete, deduplicated vocabulary of how customers actually describe their problems — a foundation that could later feed into more advanced text analysis.

---

## 🗂️ Repository Structure
