# Hi, I'm Nicolai 👋

I'm a Software Engineer based in Denmark, currently finishing my Master's degree in Software Engineering at Aalborg University. I build clean, well-tested, production-grade software — with a particular focus on Python backend systems and data-driven applications.

I care deeply about code quality, architecture, and writing software that is easy to maintain and reason about.

---

## 🎓 Education

| Degree | Institution | Year |
|--------|------------|------|
| MSc Software Engineering *(in progress)* | Aalborg University | Expected 2026 |
| BSc Software Development | Aalborg University | 2023 |

---

## 💻 Tech Stack

**Languages**
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat&logo=postgresql&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=flat&logo=openjdk&logoColor=white)
![VBA](https://img.shields.io/badge/VBA-217346?style=flat&logo=microsoftexcel&logoColor=white)

**Frameworks & Libraries**
![React](https://img.shields.io/badge/React-20232A?style=flat&logo=react&logoColor=61DAFB)
![React Native](https://img.shields.io/badge/React_Native-20232A?style=flat&logo=react&logoColor=61DAFB)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat&logo=nodedotjs&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=flat&logo=flask&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat&logo=springboot&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat&logo=numpy&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?style=flat&logo=scikitlearn&logoColor=white)
![Pydantic](https://img.shields.io/badge/Pydantic-E92063?style=flat&logo=pydantic&logoColor=white)

**Infrastructure & DevOps**
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat&logo=kubernetes&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat&logo=githubactions&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=flat&logo=nginx&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)

**Tools & Practices**
![Git](https://img.shields.io/badge/Git-F05032?style=flat&logo=git&logoColor=white)
![pytest](https://img.shields.io/badge/pytest-0A9EDC?style=flat&logo=pytest&logoColor=white)
![mypy](https://img.shields.io/badge/mypy-checked-2A6DB2?style=flat)
![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=flat&logo=powerbi&logoColor=black)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat&logo=jupyter&logoColor=white)
![Swagger](https://img.shields.io/badge/Swagger-85EA2D?style=flat&logo=swagger&logoColor=black)

---

## 🚀 Featured Projects

### [QuantForge](https://github.com/Mandrupnicolai/quantforge) — Algorithmic Trading & Backtesting Library

[![CI](https://github.com/Mandrupnicolai/quantforge/actions/workflows/ci.yml/badge.svg)](https://github.com/Mandrupnicolai/quantforge/actions)
[![codecov](https://codecov.io/gh/Mandrupnicolai/quantforge/branch/main/graph/badge.svg)](https://codecov.io/gh/Mandrupnicolai/quantforge)
[![Python 3.11+](https://img.shields.io/badge/python-3.11+-blue.svg)](https://www.python.org/downloads/)
[![Ruff](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/astral-sh/ruff/main/assets/badge/v2.json)](https://github.com/astral-sh/ruff)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

> A production-grade Python library for building, backtesting, and evaluating quantitative trading strategies with rigorous statistical validation.

QuantForge demonstrates the engineering standards I bring to professional Python work — from architecture and type safety to testing and CI/CD.

**What's under the hood:**

- **Clean architecture** — `Strategy` is a structural Protocol (duck typing, no inheritance required), keeping the codebase open for extension without modification
- **Immutable domain models** — Pydantic v2 with `Decimal` precision for all monetary values; invalid state is impossible to construct
- **Vectorised backtesting engine** — NumPy-accelerated simulation with realistic slippage and commission modelling, and strict look-ahead bias prevention
- **Full testing pyramid** — 89 passing tests: unit, integration, and Hypothesis property-based tests that explore thousands of edge cases automatically
- **Professional CI/CD** — GitHub Actions running lint, type-check, tests across Ubuntu/macOS/Windows × Python 3.11 & 3.12, security audit, and benchmarks
- **Rich analytics** — Sharpe, Sortino, Calmar, max drawdown, VaR 95%, CVaR 95%, win rate, profit factor

```python
from quantforge import Backtester, Portfolio
from quantforge.strategies import SMACrossoverStrategy

strategy = SMACrossoverStrategy(fast_window=20, slow_window=50)
result = Backtester(Portfolio(100_000), strategy).run(prices)

print(result.metrics.sharpe_ratio)   # 1.47
print(result.metrics.max_drawdown)   # -0.183
print(result.metrics.win_rate)       # 0.54
```

→ **[View repository](https://github.com/Mandrupnicolai/quantforge)**

---

### [Text-to-SQL Natural Language Interface](https://github.com/Mandrupnicolai/text-to-sql-natural-language-interface) — AI-Powered Database Query Tool

![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat&logo=nodedotjs&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat&logo=sqlite&logoColor=white)
![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=flat&logo=openai&logoColor=white)

> A browser-based natural language interface that translates plain English questions into SQL queries — with zero server dependency for instant use.

This project demonstrates my ability to bridge AI tooling with practical data access workflows.

**Key features:**

- **Local WASM execution** — runs a full SQLite engine in-browser via sql.js, no server required for instant query previews
- **AI-powered NL-to-SQL** — optional OpenAI-backed server mode translates natural language questions into valid SQL
- **SQL scratchpad** — per-query explain plans, export-to-CSV, persistent query history, and index suggestions generated from SQL text
- **Schema explorer** — browse table structure with sample values directly in the UI
- **Dual execution modes** — seamlessly toggle between local WASM and Node.js API server

```
"Top 5 customers by revenue"       → SELECT customer_id, SUM(total) ...
"Revenue by category in March 2026" → SELECT category, SUM(amount) ...
"Repeat customers"                  → SELECT customer_id, COUNT(*) ...
```

→ **[View repository](https://github.com/Mandrupnicolai/text-to-sql-natural-language-interface)**

---

### [Home Network Vulnerability Scanner](https://github.com/Mandrupnicolai/home-network-vulnerability-scanner) — Defensive Security Tool

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)

> A lightweight, local-only LAN scanner that discovers devices, audits open ports, and generates human-readable risk reports — built for defensive personal use.

This project reflects my interest in security-aware software development and systems-level Python.

**What it does:**

- **Device discovery** — scans your LAN subnet to enumerate all connected hosts
- **Port scanning & banner grabbing** — checks common TCP ports and captures service banners where available
- **Risk-oriented reporting** — outputs Markdown + JSON reports with heuristic risk ratings per host
- **Web UI** — accessible at `http://127.0.0.1:8080` for a clean scan overview without touching the CLI
- **Configurable & safe** — supports custom port lists, host limits, timeouts, and subnet overrides; no exploitation attempted

```bash
python server.py      # Launch the UI at http://127.0.0.1:8080
python scanner.py --ports 22,80,443,3306 --subnet 192.168.1.0/24
```

→ **[View repository](https://github.com/Mandrupnicolai/home-network-vulnerability-scanner)**

---

## 📫 Let's connect

I'm currently open to graduate positions and internships in software engineering, backend development, and data-intensive systems.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/nicolai-uhre-mandrup-526288220/)
[![Email](https://img.shields.io/badge/Email-D14836?style=flat&logo=gmail&logoColor=white)](mailto:nicolai.uhre.com@gmail.com)
