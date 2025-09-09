# Road-Network
C CLI for a Palestinian cities road network using graphs and MST. Loads cities/distances from file, builds adjacency lists &amp; edge set, and computes an MST via Prim’s (binary min-heap) and Kruskal’s (union–find + min-heap). Prints MST edges, total cost, runtime, and provides side-by-side comparison.

This project implements a road network in C and computes a Minimum Spanning Tree (MST) using Prim’s and Kruskal’s algorithms, then compares their results and performance.

Key Features

Data model: adjacency lists for the graph, plus an array of edges.

Loading: reads cities.txt lines as Src#Dest#Distance.

Prim’s MST: binary min-heap with decreaseKey, parent tracking, total cost, runtime.

Kruskal’s MST: edge min-heap + Disjoint Set (Union–Find) with path compression & union by rank.

Comparison: prints last run’s total cost, runtime, and notes disconnections.

Memory mgmt: explicit malloc/free, cleanup for adjacency lists and heaps.

What it demonstrates

Graph representation (adjacency lists) and edge processing

Heaps for priority queues, union–find for cycle avoidance

Time measurement via clock() and menu-driven CLI

How to use

Prepare cities.txt with lines like: Ramallah#Nablus#52.

Run program → 1 Load cities → 2 Prim → 3 Kruskal → 4 Compare → 5 Exit.

Notes

Detects disconnected graphs (builds a forest, reports missing edges).

Limits configurable via MAX_CITIES / MAX_EDGES.
