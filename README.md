# SQL: Zero to Production

[![Learning in Public](https://img.shields.io/badge/learning-in%20public-2ea44f)](https://github.com/sauryansh/sql-zero-to-production)
![SQL](https://img.shields.io/badge/SQL-PostgreSQL-336791?logo=postgresql&logoColor=white)
![Progress](https://img.shields.io/badge/progress-Day%201-blue)

A beginner-friendly, hands-on journey from writing a first SQL query to designing and optimizing databases for **backend engineering, system design, and AI applications**.

This repository documents my consistent SQL practice with concepts, exercises, mistakes, corrections, interview questions, and production-oriented projects.

## Why this repository?

SQL is more than query syntax. Backend and AI engineers use it to:

- Model reliable application data
- Build APIs and transactional workflows
- Diagnose slow production queries
- Design indexes and scalable schemas
- Prepare data for analytics and machine learning
- Store and retrieve metadata for RAG and AI systems

The goal is to progress from fundamentals to practical, production-level understanding over approximately five months.

## Learning roadmap

| Phase | Weeks | Topics |
|---|---:|---|
| Foundations | 1–4 | Tables, rows, columns, keys, `SELECT`, filtering, sorting, `NULL`, and CRUD |
| Core querying | 5–8 | Aggregations, `GROUP BY`, `HAVING`, joins, `CASE`, functions, and subqueries |
| Backend SQL | 9–12 | CTEs, window functions, schema design, normalization, transactions, locks, and JPA |
| Performance | 13–16 | Indexes, query plans, pagination, partitioning, batching, and production debugging |
| SQL for AI | 17–18 | RAG schemas, vector metadata, evaluation data, feedback, and retrieval filters |
| Interview and capstone | 19–20 | Senior-level problems, optimization exercises, and an end-to-end project |

## Progress

| Day | Topic | Status |
|---:|---|---|
| [Day 1](foundations/day-01-sql-foundations.md) | Query foundations: `SELECT`, `WHERE`, sorting, ranges, `NULL`, `DISTINCT`, and `LIMIT` | In progress |

## Repository structure

```text
sql-zero-to-production/
├── README.md
├── foundations/
├── joins-and-aggregation/
├── intermediate-sql/
├── database-performance/
├── backend-sql/
├── ai-data-systems/
├── interview-problems/
└── projects/
```

Directories will be added as the learning journey progresses.

## Practice method

Each session follows a repeatable structure:

1. Learn the concept in plain language.
2. Study a small guided example.
3. Attempt exercises before seeing solutions.
4. Record mistakes and corrections.
5. Finish with a recap challenge.
6. Revisit weak topics using spaced repetition.

Examples use realistic payments, logistics, insurance, SaaS, and AI-platform scenarios.

## Current focus

- [x] Selecting columns
- [x] Filtering text and numeric values
- [x] Combining conditions with `AND`, `OR`, and `IN`
- [x] Handling `NULL`
- [x] Using `BETWEEN`, `DISTINCT`, and `LIMIT`
- [ ] Consistently choosing the correct `ASC` or `DESC` direction
- [ ] Complete the Day 1 recap challenge

## Tech focus

- **Primary dialect:** PostgreSQL
- **Enterprise comparison:** Oracle SQL
- **Backend integration:** Java, Spring Boot, JPA, and JDBC
- **AI/data applications:** analytics, embeddings, vector search, RAG, evaluation, and observability

## Learning principle

> Understand the data, define the expected result, write the simplest correct query, and optimize only after measuring.

## Contributions

This is a learning-in-public repository. Suggestions, alternative solutions, query improvements, and beginner-friendly explanations are welcome.

---

If you are also learning SQL, follow the repository and practise along from [Day 1](foundations/day-01-sql-foundations.md).
