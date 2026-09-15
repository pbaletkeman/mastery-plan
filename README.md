# 30-Day Backend Foundations Mastery Plan

A structured, self-guided 30-day interview preparation curriculum for backend software engineering roles. Covers concurrency primitives, data structures, algorithms, system design, and concurrency theory — with dual-language implementation in **Java** and **Python**.

## Overview

This plan is broken into four progressive segments:

| Week | Focus | Topics |
|------|-------|--------|
| **Week 1** | Core Concurrency Primitives | Mutex, condition variables, fair semaphore, append-only list, LRU cache, token bucket, worker pool |
| **Week 2** | Graphs, Arrays & Strings | DFS/BFS, cycle detection, topological sort, connected components, sliding window, intervals, string patterns |
| **Week 3** | Backtracking & Permutations | 4 levels of increasing difficulty — unique permutations, next permutation, k-th permutation |
| **Week 4** | System Design + Theory | Rate limiter, URL shortener, caching, job queue, autocomplete, logging pipeline, mock interviews |

Each day follows a 4-hour block structure:
1. **Concept Study** (1 hr) — Read and internalize the theory
2. **Java Implementation** (1 hr) — Build it in Java
3. **Python Implementation** (1 hr) — Build it in Python
4. **Practice Problem** (1 hr) — Apply the pattern to a coding problem

## Repository Structure

```
.
├── README.md            # This file
├── the-plan.md          # Master curriculum — categorized list of all problems and concepts
├── study-guide.md       # Detailed 30-day day-by-day schedule
└── warm-up.md           # Quick-reference flashcard-style notes for rapid review
```

## How to Use

1. **Start with `the-plan.md`** — get a bird's-eye view of all topics and what's expected.
2. **Follow `study-guide.md`** day by day — it tells you exactly what to study and implement each day.
3. **Use `warm-up.md`** for quick review — condensed problem statements, key insights, and pattern summaries.

## Prerequisites

- Java (JDK) and Python 3 installed
- A code editor
- No build system or package manager required — all exercises are standalone files

## Running the Exercises

**Java:**
```bash
javac <file>.java && java <classname>
```

**Python:**
```bash
python <file>.py
```
