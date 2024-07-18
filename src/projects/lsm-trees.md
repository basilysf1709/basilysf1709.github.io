---
title: lsm-trees
date: 2024-17-07
repo: btree-lsm-benchmark
topics: ["C++", "Data Structures", "Databases", "System Design"]
lead: Ground up implementation of LSM Trees and benchmarking against normal B-Trees
image: lsm-trees.png
---

This project benchmarks the performance of B-Trees and Log-Structured Merge (LSM) Trees, both crucial for database indexing. B-Trees excel in in-memory operations, providing fast insertion, deletion, and search capabilities, making them ideal for database and file system indexing. LSM Trees, optimized for write-heavy workloads, periodically flush data from memory to disk as SSTables, handling large datasets effectively despite slower read times due to multiple SSTables. The benchmarking tests, implemented in C++, measure insertion and search times for both structures, highlighting their performance differences.

The project's structure includes header and implementation files for B-Trees, LSM Trees, and SSTables, along with a main benchmarking file. Compilation and execution are simple, with commands provided for building, cleaning, and running the project. Results show B-Trees' efficiency in memory-based operations, while LSM Trees are better for large datasets with frequent writes. Future improvements include optimizing LSM Tree performance through compaction, merging, and enhanced I/O operations.

**Links: [GitHub](https://github.com/UsmanBasilAgency/teachify)**
