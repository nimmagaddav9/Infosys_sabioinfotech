# Mock Interview Q&A: Fullstack Developer (React + Python + DB)

## Role Summary:
- **Title**: Fullstack Developer  
- **Focus**: React, Python scripting/automation, database performance tuning  
- **Extras**: T-Mobile tools/process familiarity (nice to have)  
- **Traits**: Problem solvers with 10+ years experience, strong communication

---

## ✅ React (UI) Questions

### Q1: How do you manage complex state in large React apps?
**A**:  
I use a combination of local component state, React Context for global needs, and Redux Toolkit for more structured state across multiple modules.  
I lean on `createSlice` and RTK Query where applicable. For performance, I memoize selectors with Reselect and use `React.memo`, `useMemo`, and `useCallback` strategically.

---

### Q2: What's the difference between useEffect and useLayoutEffect? When do you prefer one over the other?
**A**:  
`useEffect` runs **after** the render is committed to the screen. `useLayoutEffect` runs **synchronously** after render but **before** the browser paints.  
If I'm measuring layout dimensions or making visual DOM changes that could cause flickering, I use `useLayoutEffect`.

---

### Q3: How do you structure reusable components?
**A**:  
I follow the "smart vs dumb" or "container vs presentational" component pattern when possible.  
I design components to be:
- **Stateless**, when possible  
- **Composed**, using children or render props  
- **Typed**, using TypeScript interfaces  
- **Themed**, using a design system or CSS-in-JS library like styled-components or Tailwind

---

## ✅ Python + Scripting/Automation Questions

### Q4: How have you used Python to automate repetitive tasks?
**A**:  
In one project, I built a Python CLI tool using `argparse` to automate A/B test data pulls and aggregations from Snowflake.  
I also used `pandas` for ETL-like transformations, then sent summary emails via `smtplib`.  
For jobs that needed to run regularly, I containerized the script with Docker and scheduled it with Airflow.

---

### Q5: Can you describe a Python script you've written that interfaces with a database?
**A**:  
I built a monitoring script that ran queries against a Postgres DB, checked query execution times, and logged slow queries.  
It used `psycopg2` for connections and `logging` for alerts. In later iterations, I added Prometheus export format to plug into Grafana dashboards.

---

## ✅ Database Tuning Questions

### Q6: Walk me through how you’d tune a slow query in production.
**A**:  
Step 1: Identify slow queries using `EXPLAIN ANALYZE` or the query planner.  
Step 2: Check for missing indexes, table scans, or large joins.  
Step 3: Rewrite the query or break it into smaller pieces.  
Step 4: Add indexes, partition large tables, or denormalize where justified.  
Step 5: Monitor using query stats dashboards (e.g. pg_stat_statements or AWS RDS Insights).

---

### Q7: What’s your approach to designing scalable DB schemas?
**A**:  
I focus on:
- Normalization (up to 3NF) unless performance demands denormalization  
- Proper indexing (composite, partial, covering)  
- Avoiding SELECT * in queries  
- Using UUIDs or ULIDs for distributed systems  
- Planning for growth: partitioning, archiving old data, async writes when needed

---

## ✅ Communication / Soft Skills

### Q8: Give an example of explaining a technical problem to a non-technical stakeholder.
**A**:  
In a data migration project, I explained the concept of **eventual consistency** to a product manager by using a real-world analogy: “It’s like ordering a package—you get a confirmation right away, but the delivery happens later. Same here, data is syncing behind the scenes.”  
That cleared confusion without going deep into tech jargon.

---

### Q9: What do you do when you hit a roadblock and no one around has the answer?
**A**:  
I research using docs, GitHub issues, or Stack Overflow, but I also log and summarize what I've tried before asking for help.  
If it's urgent, I create a minimal reproducible example and share it with a broader engineering group or in a Slack channel.  
I treat blockers as a chance to document tribal knowledge and help the next dev who runs into it.

---

## ✅ T-Mobile Specific / Process Fit

### Q10: Have you worked with large enterprise tools like Jira, Jenkins, or AEM?
**A**:  
Yes. I’ve integrated CI/CD pipelines using Jenkins and GitHub Actions. I’ve worked in Jira-based Agile environments, leading sprint ceremonies.  
In a previous role, I also integrated frontend code with AEM authors via JSON APIs and SPA frameworks.

---

### Q11: T-Mobile favors initiative-takers. How do you prove you're a “thinker,” not just a “doer”?
**A**:  
I challenge assumptions. For example, in one project we were going to automate a complex approval workflow—but I proposed eliminating the workflow altogether by changing a business rule.  
Saved us 3 weeks of work.  
I look for root causes, not just symptoms, and I propose solutions proactively before being asked.

---

## ✅ Bonus Questions

### Q12: What’s your dev environment and go-to stack?
**A**:  
VSCode, Docker, Postman, pgAdmin  
React + TypeScript + Redux Toolkit (or Zustand)  
Node.js for APIs, Python for scripting  
PostgreSQL or DynamoDB depending on use case  
AWS Lambda, S3, API Gateway where applicable

---

### Q13: What’s something new you learned recently?
**A**:  
I recently explored Vite + React for faster local dev. It’s blazing fast and great for micro frontends or lightweight apps.  
On the Python side, I’ve been diving into Pydantic v2 and FastAPI for building APIs with strong type validation.

---
