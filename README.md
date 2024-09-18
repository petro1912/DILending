<div align="center">
    <a href="https://dilending.portfolio-as.com">
        <img alt="logo" src="https://github.com/petro1912/DILendingXFI-Frontend/blob/main/public/images/logo.png?raw=true" style="width: 160px;">
    </a>
    <h1 style="border-bottom: none">
        <b><a href="https://dilending.portfolio-as.com">DI Lending</a></b><br />
    </h1>
</div>
## DILending Protocol
“DI Lending” Protocol is the DeFI Lending protocol which puts the idle liquidity (principal) and collateral assets into other external staking/yield farming protocols to maximize capital utilization and revenue in the pool.

Author: Denys Ivanenko

This repository serves as the hub for the Next.js and Smart Contract(Solidity) projects.

- [Frontend Repository: https://github.com/petro1912/DILendingXFI-Frontend](https://github.com/petro1912/DILendingXFI-Frontend) 
- [Backend Repository: https://github.com/petro1912/DILendingXFI](https://github.com/petro1912/DILendingXFI)

## What is the major problem in current lending protocols?
### Introduction to DeFi Lending
Decentralized Finance (DeFi) lending revolutionizes traditional financial systems by leveraging blockchain technology to enable peer-to-peer lending and borrowing without intermediaries. Unlike traditional models, where banks act as gatekeepers and extensive personal information or credit assessments are required, DeFi operates within a trustless system. In this environment, users maintain full control over their assets, providing flexibility, transparency, and efficiency.
How DeFi Lending Works
In DeFi lending platforms, borrowers can secure loans by providing collateral, typically in the form of cryptocurrencies. This over-collateralization ensures that lenders are protected from default risks, as the collateral is held in a smart contract until the loan is repaid or liquidated in case of default. On the other hand, lenders earn interest on their deposits, with interest rates fluctuating based on the supply and demand dynamics of the platform.
### Utilization Ratio: A Key Indicator
The utilization ratio is a critical measure of the health and performance of a lending protocol. It reflects the percentage of assets in a lending pool that are actively being borrowed.
•	High Utilization suggests strong demand for loans, which drives up interest rates for borrowers and offers higher returns for lenders.
•	Low Utilization indicates excess liquidity, leading to reduced interest rates and lower efficiency for the capital deployed.
In current lending protocols like Aave and Compound, the utilization ratio often falls below the optimal threshold, creating inefficiencies in capital usage. For instance:
•	Aave shows utilization ratios of 78.22% (USDT) and 83.9% (USDC), below the optimal rate of 92%.
•	Compound reports utilization ratios of 68.61% (USDT) and 74.35% (USDC), against an optimal target of 90%.
Contradictory between revenue of lenders and interest of borrowers
Borrowers need low utilization to borrow at low interest rates, while lenders want high utilization to avoid dilution of income. This is a major problem for loan pools and contradict between lenders and borrowers, leading to capital inefficiencies.
### Capital Inefficiency in DeFi Lending
The low utilization of lending pools results in significant capital inefficiency. The collateral provided by borrowers, which is often over-collateralized, remains locked and unproductive. This means a substantial amount of capital sits idle, failing to generate any return for either the borrowers or the platform. Current lending protocols miss opportunities to put these locked assets to work, resulting in missed revenue opportunities.
### Comparison to Traditional Lending
In Traditional Lending, collateral assets (Real Estate, Gold, or etc) should not be used and processed but secured by lender organization because those can be unique and lost, damaged, or modified.
However in DeFi, collateral assets can be used if those can be redeemed instantly (in time) and traded securely in external of the protocol.
What is actual utilization, and does current utilization reflect capital utilization?
TVL(Total Values Locked in protocol) reflects total capitals invested in the market and it consists of principal (liquidity) and collateral assets.
In current Lending, utilization related to principal assets of the pool, and this value is less than half of TVL.

In practice, borrowers lock up more collateral than the liquidation threshold to better protect their assets. This means that at least 55% of total capital is underutilized.
So we can see that the actual capital utilization is at most 45% of the principal utilization. So if the utilization of lending is 80% in current lending protocols, it means that only 36% of the total capital are actually utilized.

## DI Lending's Solution

###Introduction to DI Lending Protocol:
“DI Lending” Protocol is the one to put the idle liquidity (principal) and collateral assets into other staking/yield farming protocols to maximize capital utilization and revenue in the pool.
This protocol addresses capital inefficiency by maximizing the use of idle assets in the pool. The core innovation lies in the strategic allocation of unutilized borrowing and collateral assets into other secure revenue protocols.
Key Features
•	Dynamic Capital Allocation: Idle liquidity from both borrowing and collateral reserves is invested in staking pools to generate additional returns for all participants, enhancing the capital efficiency of the platform.
•	Revenue Generation for Borrowers: Borrowers also benefit, as their collateral is no longer sitting idle but is actively generating income through staking. This not only covers some of the interest costs of their loans but also provides them with a new revenue stream.
•	Enhanced Returns for Lenders: Lenders gain higher returns as the excess liquidity is utilized, increasing the overall yield on their deposits.
•	Balanced Risk Management: The allocation of assets into staking pools is managed dynamically based on real-time data of supply, demand, and utilization ratios, ensuring that the protocol always maintains sufficient liquidity for borrowers while maximizing earnings from staking/yield farming protocols.
###Benefits of DI Lending
•	Capital Efficiency: Idle liquidity is dynamically allocated to staking pools, maximizing the utilization of the platform’s capital and providing consistent returns.
•	Staking-Enhanced Income: Lenders and borrowers alike benefit from staking rewards, creating a more balanced and fair distribution of income in the system.
•	Sustainable Growth: By ensuring higher utilization rates and increasing returns for all parties, the protocol fosters a healthy, growing ecosystem.
