# Market Terminal

A terminal-based market data dashboard written in Rust.

The goal of this project is to explore real-time market data streaming, asynchronous systems, and terminal user interfaces (TUI) using Rust.

## Features (Planned)

- Real-time market price streaming
- Terminal dashboard UI
- Multi-symbol monitoring
- WebSocket data feeds
- Low-latency updates

## Tech Stack

- Rust
- Tokio (async runtime)
- Ratatui (terminal UI)
- WebSockets for market data

## Motivation

This project is part of a learning journey focused on:

- Rust systems programming
- real-time data pipelines
- terminal-based interfaces
- market microstructure experimentation

             ┌────────────┐
Market Data →│            │
Keyboard  →  │  AppState  │ → UI
Timers    →  │            │
             └────────────┘

AppState
 │
 ├── market_prices
 │       │
 │       ├── BTCUSDT → PriceData
 │       ├── ETHUSDT → PriceData
 │       └── MES → PriceData
 │
 └── last_update

Architecture

             WebSocket Task
                 │
                 ▼
           Price Update
                 │
                 ▼
              Channel
                 │
                 ▼
          Main App Loop
                 │
                 ▼
              AppState
                 │
                 ▼
                UI

## Future Ideas

- order book visualization
- market replay engine
- trading signal prototyping
