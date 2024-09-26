<div align="center">
    <a href="https://dilending.portfolio-as.com">
        <img alt="logo" src="https://github.com/petro1912/DILendingXFI-Frontend/blob/main/public/images/logo.png?raw=true" style="width: 160px;">
    </a>
    <h1 style="border-bottom: none">
        <b><a href="https://dilending.portfolio-as.com">DI Lending</a></b><br />
    </h1>
</div>

**DI Lending** Protocol is the DeFI Lending protocol which puts the idle liquidity (principal) and collateral assets into other external staking/yield farming protocols to maximize capital utilization and revenue in the pool.

Author: Denys Ivanenko

This repository serves as the hub for the Next.js and Smart Contract(Solidity) projects.

- [Frontend Repository: https://github.com/petro1912/DILendingXFI-Frontend](https://github.com/petro1912/DILendingXFI-Frontend) 
- [Backend Repository: https://github.com/petro1912/DILendingXFI](https://github.com/petro1912/DILendingXFI)

## What is the major problem in current lending protocols?
### Introduction to DeFi Lending
Decentralized Finance (DeFi) lending revolutionizes traditional financial systems by leveraging blockchain technology to enable peer-to-peer lending and borrowing without intermediaries. Unlike traditional models, where banks act as gatekeepers and extensive personal information or credit assessments are required, DeFi operates within a trustless system. In this environment, users maintain full control over their assets, providing flexibility, transparency, and efficiency.
<br/>**How DeFi Lending Works?** <br/>
In DeFi lending platforms, borrowers can secure loans by providing collateral, typically in the form of cryptocurrencies. This over-collateralization ensures that lenders are protected from default risks, as the collateral is held in a smart contract until the loan is repaid or liquidated in case of default. On the other hand, lenders earn interest on their deposits, with interest rates fluctuating based on the supply and demand dynamics of the platform.
### Utilization Ratio: A Key Indicator
The utilization ratio is a critical measure of the health and performance of a lending protocol. It reflects the percentage of assets in a lending pool that are actively being borrowed.
- High Utilization suggests strong demand for loans, which drives up interest rates for borrowers and offers higher returns for lenders.
- Low Utilization indicates excess liquidity, leading to reduced interest rates and lower efficiency for the capital deployed.
In current lending protocols like Aave and Compound, the utilization ratio often falls below the optimal threshold, creating inefficiencies in capital usage.

For instance:
- Aave shows utilization ratios of 78.22% (USDT) and 83.9% (USDC), below the optimal rate of 92%.
- Compound reports utilization ratios of 68.61% (USDT) and 74.35% (USDC), against an optimal target of 90%.

### Contradictory between revenue of lenders and interest of borrowers
Borrowers need low utilization to borrow at low interest rates, while lenders want high utilization to avoid dilution of income. This is a major problem for lending pools and contradict between lenders and borrowers, leading to capital inefficiencies.

### Capital Inefficiency in DeFi Lending
The low utilization of lending pools results in significant capital inefficiency. The collateral provided by borrowers, which is often over-collateralized, remains locked and unproductive. This means a substantial amount of capital sits idle, failing to generate any return for either the borrowers or the platform. Current lending protocols miss opportunities to put these locked assets to work, resulting in missed revenue opportunities.

### Comparison to Traditional Lending
In Traditional Lending, collateral assets (Real Estate, Gold, or etc) should not be used and processed but secured by lender organization because those can be unique and lost, damaged, or modified.
However in DeFi, collateral assets can be used if those can be redeemed instantly (in time) and traded securely in external of the protocol.

## So what is actual utilization, and does current utilization reflect proper capital utilization?
The most important thing to keep in mind when dealing with market yields is to consider the return on total capital (TVL).
TVL (Total Values Locked) reflects total capitals invested in the market and is composed of principal (liquidity) and collateral assets in lending markets.
In the most lending protocols, however, only the pool's principal assets are considered utilized, which is less than half of the TVL.

We can calculate actual capital utilization in below (Assume that pool's utilization ratio is 80% at this time).
```javascript
TVL = TotalPrincipal + TotalCollateral
ActualUtilizationRatio = UtilizedPrincipal / TVL // utilized capital is only principal

UtilizedPrincipal = UtiliztionRatio * TotalPrincipal
TotalCollateral >= CollateralizationRatio * UtilizedPrincipal = UtilizationRatio * CollateralRatio * TotalPrincipal

TVL >= TotalPrincipal * (1 + UtilizationRatio * CollateralizationRatio)
ActualUtilizationRatio = UtilizedPrincipal / TVL <= UtilizaitonRatio / (1 + UtilizationRatio * CollateralizationRatio)

// when collateral ratio is 1.2 and utilization ratio is 0.8 
TVL >= TotalPrincipal * 1.96
ActualUtilizationRatio <= 0.8 / 1.96 = ~0.408 (40.8 %)

// when utilization rate is 0.9 (optimal rate)
TVL >= TotalPrincipal * 2.08
ActualUtilizationRatio <= 0.9 / 2.08 = ~0.432 (43.2%)
```

In the above explanation, 1.2 refers to the collateralization ratio, that is, the amount of collateral required to borrow 1 unit of value.
We can see the graph that shows relashion between total capital uitilization(actual utilization) and pool's utilization.
<p align="center">
  <img src="https://github.com/petro1912/DILending/blob/main/utilization-graph.png" alt="Utilization Graph" width="640" height="540">
</p>

<p align="center">
  <strong>Capital Utilization Ratio by Pool's utilization (principal)</strong>
</p>


In practice, borrowers lock up more collateral than the collateralization ratio to better secure their assets. 
When utilization is 80%, value of total collaterals is 96% of principal and it is nearly about 50% of TVL. 
We can see that the actual capital utilization is at most 45% even when optimal rate is reached. 
If the utilization of lending is 80% in current lending protocols, it means that only 40% of the total capital are actually utilized.

## DI Lending's Solution

### Introduction to DI Lending Protocol:
**DI Lending** Protocol is the one to put the idle liquidity (principal) and collateral assets into other staking/yield farming protocols to maximize capital utilization and revenue in the pool.
This protocol addresses capital inefficiency by maximizing the use of idle assets in the pool. The core innovation lies in the strategic allocation of unutilized borrowing and collateral assets into other secure revenue protocols.

### Key Features
- **Dynamic Capital Allocation:** Idle liquidity from both borrowing and collateral reserves is invested in staking pools to generate additional returns for all participants, enhancing the capital efficiency of the platform.
- **Revenue Generation for Borrowers:** Borrowers also benefit, as their collateral is no longer sitting idle but is actively generating income through staking. This not only covers some of the interest costs of their loans but also provides them with a new revenue stream.
- **Enhanced Returns for Lenders:** Lenders gain higher returns as the excess liquidity is utilized, increasing the overall yield on their deposits.
- **Balanced Risk Management:** The allocation of assets into staking pools is managed dynamically based on real-time data of supply, demand, and utilization ratios, ensuring that the protocol always maintains sufficient liquidity for borrowers while maximizing earnings from staking/yield farming protocols.

### Benefits of DI Lending
- **Capital Efficiency:** Idle liquidity is dynamically allocated to staking pools, maximizing the utilization of the platform’s capital and providing consistent returns.
- **Staking-Enhanced Income:** Lenders and borrowers alike benefit from staking rewards, creating a more balanced and fair distribution of income in the system.
- **Sustainable Growth:** By ensuring higher utilization rates and increasing returns for all parties, the protocol fosters a healthy, growing ecosystem.

## DILending Diagram
<p align="center">
  <img src="https://github.com/petro1912/DILending/blob/main/Flowchart-dilending.png" alt="Utilization Graph" width="960" height="540">
</p>
