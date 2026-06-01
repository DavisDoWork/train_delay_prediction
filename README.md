# NYC Train Delay Prediction with Graph Neural Networks

This project builds a machine learning pipeline for predicting NYC subway delay changes using MTA GTFS and GTFS-Realtime data. The system collects real-time train updates, processes train and stop-level information, engineers operational features, converts the subway network into graph data, and trains Graph Neural Network models.

## Project Goal

The goal is to predict future train delay changes at subway stops using graph-based learning. Each subway stop is treated as a graph node, and train movement between stops is represented as graph edges.

## Data Sources

- MTA GTFS static schedule data
- MTA GTFS-Realtime trip updates
- MTA GTFS-Realtime vehicle positions
- MTA service alerts

Large raw data files are not included in this repository because they are too large for GitHub and are collected dynamically from MTA feeds.

## Pipeline Overview

```text
1. Collect GTFS-Realtime snapshots
2. Parse realtime trip updates
3. Merge realtime data with planned GTFS schedule data
4. Align vehicle positions with trip updates
5. Clean and refine operational train records
6. Engineer delay, headway, dwell, rush-hour, and congestion features
7. Build subway stop graph nodes and edges
8. Convert graph snapshots into PyTorch Geometric Data objects
9. Train GCN, GAT, and GraphSAGE models
10. Inspect and plot model predictions
```
