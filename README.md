# Ngordnet

Java tool that links a WordNet semantic graph with Google NGrams word-frequency history.

## Problem

Explore how word meaning and word usage relate over time: given a word (or several), find its hyponyms and rank them by how popular they have been historically. Built as a course project for a Data Structures course at UC Berkeley.

## Approach

- Stored WordNet as a directed graph (adjacency list from synset ID to child IDs) and resolved every reachable hyponym with a recursive DFS and a visited set.
- Handled multi-word queries with set intersection across each word's hyponyms.
- Ranked results by historical frequency to return the k most popular words in a category; k = 0 returns all hyponyms alphabetically.
- Wrote unit tests for cycles, self-loops, diamonds, disconnected components, and deep chains.
- Fixed a subtle bug where synset IDs split across multiple lines were overwritten instead of merged, which silently dropped hyponyms.

## Result

Hyponym lookup for single and multi-word queries, ranked by historical frequency, with graph edge cases covered by tests.

## Tools

Java.

## Code availability

This project was completed as coursework. Per course policy, solution code isn't posted publicly here. I'm glad to walk through the implementation directly, reach out at vdkarthikeya@berkeley.edu.
