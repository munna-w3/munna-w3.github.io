## Core AMM Concepts
- **Automated Market Maker (AMM)**: Smart contract that provides liquidity using a mathematical formula instead of order books.
- **Liquidity Provider (LP)**: Supplies tokens and earns fees but faces risks (IL/LVR).
- **Impermanent Loss (IL)**: Value difference between LP position and simply holding assets. Formula: `IL = (2√r / (1 + r)) - 1` (r = price ratio change). More severe in volatile pairs.
- **Loss Versus Rebalancing (LVR)**: Alternative metric to IL; quantifies loss from arbitrageurs rebalancing the pool vs. external market. Proportional to volatility² and position gamma. Instantaneous LVR ≈ σ²/8 for constant-product AMMs.
- **Slippage / Price Impact**: Price movement caused by a trade (higher in low-liquidity or concentrated ranges).
- **Constant Product** (`x * y = k`): V1/V2 invariant.
- **Concentrated Liquidity**: V3+ — liquidity active only in chosen price ranges (improves capital efficiency but increases IL risk if price exits range).
- **TWAP (Time-Weighted Average Price)**: Oracle using cumulative price * time; resistant to short-term manipulation (V2+).
- **Flash Swaps/Loans**: Borrow assets, execute logic, repay in same tx (V2+).
