# NDRIA Architecture

## Core Components
- **Python Aggregation Daemon**: Async polling engine (asyncio + aiohttp)
- **Feed Adapters**: BlockAnalitica, DeFiScan, DeFiPunk'd, CuratorWatch, Pharos, Credora
- **Storage**: TimescaleDB (append-only, verbatim)
- **On-Chain Monitor**: Foundry scripts for top 20 DeFi protocols
- **API**: FastAPI (REST + GraphQL)
- **Frontend**: L2Beat-inspired, data-dense interface

## Neutrality Invariants
1. No composite scoring
2. Bijective field mapping only
3. Source attribution on every data point
4. Append-only database (REVOKE UPDATE/DELETE)

## Stack
Ubuntu 24.04 LTS | Python 3.12 | TimescaleDB | Foundry | MIT License
