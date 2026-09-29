🎯 The “6 patterns” were the core primitives, not the full universe
Each item begins with a Guided Link.

The original six were the foundational backend patterns:

Global mutex + condition variable

Counter + queue + fairness flag

Append‑only list + binary search

Hash map + linked list

Token bucket math

Queue + worker threads
---
🧠 Category 4 — Concurrency‑focused micro‑design

13. Design a Thread‑Safe Counter
Locks, CAS, atomic operations.

14. Design a Worker Pool
Queue, workers, backpressure, graceful shutdown.

15. Design a Read‑Write Lock
Fairness, starvation, concurrency.

Category 3 — Web infrastructure questions
These test HTTP knowledge + backend reasoning.

10. Design an Idempotent API
PUT vs PATCH, idempotency keys, retries.

11. Design a Pagination System
Offset vs cursor, consistency, performance.

12. Design a Logging Pipeline
Batching, ingestion, storage, querying.

Category 2 — Data‑flow & CRUD‑heavy questions
Houseful is a real‑estate platform → lots of CRUD, search, and filtering.

6. Design a Search Autocomplete
Trie vs prefix index, caching, ranking, latency.

7. Design a “Favorites” Feature
Idempotent writes, pagination, DB schema.

8. Design a Listing Recommendation Engine
Signals, scoring, caching, batch jobs.

9. Design a File Upload Service
Chunking, resumable uploads, virus scanning, CDN.

---
Category 1 — High‑frequency micro‑design questions
These appear constantly in short interviews.

1. Design a Rate Limiter
Token bucket, sliding window, fixed window.
Key topics: Redis, atomic counters, fairness, burst handling.

2. Design a URL Shortener
Hashing, collision avoidance, DB schema, read/write patterns.

3. Design a Caching Layer
Eviction (LRU), TTL, invalidation, cache stampede protection.

4. Design a Job Queue
Workers, retries, DLQ, visibility timeout.

5. Design a Notification System
Fan‑out, retries, rate limiting, multi‑channel delivery.

---
🧩 Essential Graph Problems

1. Graph Traversal (DFS/BFS)
The foundation of everything.

Typical prompt:

Given an adjacency list, print all nodes reachable from a starting node.

Tests: recursion, queue usage, visited sets.

2. Detect Cycle in Directed Graph
Classic interview question.

Key idea:
Use three states:

unvisited

visiting

visited

Cycle exists if you revisit a “visiting” node.

3. Detect Cycle in Undirected Graph
Simpler:
DFS with parent tracking.

4. Topological Sort
Used for dependency resolution.

Example:

Course schedule
Build order
Task dependencies

Two approaches:

DFS postorder

Kahn’s algorithm (BFS + in‑degree)

5. Connected Components
Given a graph, count how many connected components exist.

Used in:

Clustering

Islands problems

Social networks

Grouping

6. Shortest Path in Unweighted Graph
Use BFS.

Example:

Find minimum number of steps from A to B.

7. Shortest Path in Weighted Graph (Dijkstra)
Use a priority queue.

Interviewers rarely ask you to implement this fully, but they may ask conceptually.

8. Clone a Graph
Very common.

Key idea:
Use a map: original → cloned node.

DFS or BFS both work.

9. Number of Islands
This is a grid graph problem.

Use DFS/BFS to mark visited land.

10. Word Ladder
A BFS shortest‑path problem disguised as a string puzzle.

🧠 Patterns You MUST Know
These patterns appear in almost every graph question.

🔁 DFS
Recursive or stack‑based.

🪟 BFS
Queue‑based, level‑order traversal.

🔄 Visited sets
Prevent infinite loops.

🧮 Adjacency lists
Most common representation.

🧱 In‑degree counting
Used in topological sort.
---
📚 Essential Array Problems
1. Two Sum
Tests: hash maps, O(n) reasoning.

2. Move Zeroes
Tests: in‑place operations, stable ordering.

3. Rotate Array
Tests: reverse‑three‑times trick.

4. Merge Intervals
Tests: sorting + merging logic.

5. Insert Interval
Tests: interval overlap reasoning.

6. Product of Array Except Self
Tests: prefix/suffix arrays, O(n), no division.

7. Sliding Window Maximum
Tests: deque, O(n) optimization.

8. Find Missing Number
Tests: XOR trick or sum trick.

===
🧠 Patterns You MUST Know
These patterns appear repeatedly across string/array problems.

🔁 Two Pointers
Used for: palindromes, sorted arrays, merging.

🪟 Sliding Window
Used for: longest substring, max window, frequency windows.

🧮 Hash Map Frequency Counting
Used for: anagrams, duplicates, substring windows.

🔄 Prefix/Suffix Arrays
Used for: product except self, range sums.

🧱 Sorting + Merging
Used for: intervals, anagrams, grouping.
---
🔡 Essential String Problems

1. Reverse Words
Given "the sky is blue" → "blue is sky the"
Tests: pointer manipulation, trimming, splitting.

2. String Compression
aabccc → a2b1c3
Tests: run‑length encoding, counting, edge cases.

3. First Non‑Repeating Character
Tests: frequency maps, O(n) passes.

4. Longest Substring Without Repeating Characters
Classic sliding window.
Tests: hash sets, window expansion/contraction.

5. Check if Two Strings Are Anagrams
Tests: frequency counting, sorting.

6. Group Anagrams
Tests: hashing canonical forms.

7. Valid Palindrome
Tests: two‑pointer technique.

8. Longest Palindromic Substring
Tests: expand‑around‑center pattern.

---
Small system design questions
Not full system design — micro‑design.

Examples:

Design a rate limiter

Design a job scheduler

Design a notification system

Design a caching layer


---
Concurrency correctness questions
You’re already strong here — but they may ask conceptual questions:

What is a race condition?

What is a deadlock?

What is a lost wakeup?

What is a thundering herd problem?

What is a critical section?

What is atomicity?

What is a memory barrier?
---
Graph reasoning (lightweight)

Detect cycles

Topological sort

BFS/DFS traversal

Shortest path in an unweighted graph


Graph‑like data models

---
⭐ Level 1 — Warm‑up (core pattern)
These test whether you can implement the basic backtracking template cleanly.

Generate all permutations of a string
Input: "abc"
Output: ["abc","acb","bac","bca","cab","cba"]

Generate permutations of an integer array
Input: [1,2,3]
Output: all 3! permutations

Count permutations instead of listing them
Input: n = 5
Output: 120
(Tests whether you understand factorial growth)

⭐ Level 2 — Interview‑standard permutation problems
These are the ones companies actually ask.

Next permutation
Input: [1,2,3] → Output: [1,3,2]
Input: [3,2,1] → Output: [1,2,3]
(Tests lexicographic reasoning)

Permutations with duplicates
Input: [1,1,2]
Output: ["112","121","211"]
(Tests pruning + sorting + skip‑duplicate logic)

K‑th permutation
Input: n=4, k=9
Output: "2314"
(Tests factorial number system)

⭐ Level 3 — Harder backtracking variations
These test whether you can adapt the permutation template to constraints.

Permutations of length k
Input: nums=[1,2,3], k=2
Output: ["12","13","21","23","31","32"]

Letter case permutations
Input: "a1b"
Output: ["a1b","a1B","A1b","A1B"]
(Tests branching on characters)

Phone keypad permutations
Input: "23"
Output: ["ad","ae","af","bd","be","bf","cd","ce","cf"]
(Tests mapping + recursion)

⭐ Level 4 — Advanced (if they want to push you)
These are rare but show mastery.

Permutation sequence with constraints
Example: “Generate permutations where no two adjacent numbers differ by 1.”

Permutation of a linked list
Tests pointer manipulation + recursion.

Permutation of multiset with frequency map
Tests using a hashmap instead of sorting + skipping.
---

🧩 High‑frequency micro‑design questions
1. Design a Rate Limiter
Token bucket vs sliding window, Redis atomic ops, fairness, burst handling.

2. Design a URL Shortener
Hashing, collision avoidance, DB schema, read/write patterns.

3. Design a Caching Layer
LRU, TTL, invalidation, cache stampede protection.

4. Design a Job Queue
Workers, retries, DLQ, visibility timeout.

5. Design a Notification System
Fan‑out, retries, multi‑channel delivery, rate limiting.

🧱 CRUD‑heavy & data‑flow questions
6. Design a Search Autocomplete
Trie vs prefix index, ranking, caching, latency.

7. Design a Favorites / Likes Feature
Idempotent writes, pagination, DB schema.

8. Design a File Upload Service
Chunking, resumable uploads, virus scanning, CDN.

9. Design a Listing Recommendation Engine
Signals, scoring, caching, batch jobs.

🌐 Web infrastructure questions
10. Design an Idempotent API
Idempotency keys, retries, PUT vs PATCH.

11. Design Pagination
Offset vs cursor, consistency, performance.

12. Design a Logging Pipeline
Batching, ingestion, storage, querying.

🧠 Concurrency‑focused micro‑design
13. Design a Thread‑Safe Counter
Locks, CAS, atomic operations.

14. Design a Worker Pool
Queue, workers, backpressure, graceful shutdown.

15. Design a Read‑Write Lock
Fairness, starvation, concurrency.
