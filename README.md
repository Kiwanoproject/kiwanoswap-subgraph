1) Exchange API: Tracks all kiwanoswap Exchange data with price, volume, liquidity.
https://api.thegraph.com/subgraphs/name/kiwanoproject/exchange

2) Blocks API: Tracks all blocks on Binance Smart Chain.
https://api.thegraph.com/subgraphs/name/kiwanoproject/blocks


3) Pairs: Tracks all kiwanoproject Pairs and Tokens.
 https://api.thegraph.com/subgraphs/name/kiwanoproject/pairs

For now we have only 3  Active Api





# kiwanoswap Subgraph

TheGraph exposes a GraphQL endpoint to query the events and entities within the Binance Smart Chain and kiwanoswap ecosystem.

Currently, there are multiple subgraphs, but additional subgraphs can be added to this repository, following the current architecture.
cd
## Subgraphs

1. **[Blocks](https://thegraph.com/legacy-explorer/subgraph/kiwanoproject/blocks)**: Tracks all blocks on Binance Smart Chain.

2. **[Exchange](https://thegraph.com/legacy-explorer/subgraph/kiwanoproject/exchange)**: Tracks all kiwanoproject Exchange data with price, volume, liquidity, ...

3. **[Farm Auctions](https://thegraph.com/legacy-explorer/subgraph/kiwanoproject/farm-auctions)**: Tracks all kiwanoproject Farm Auctions with auctions and bids.

4. **[Lottery](https://thegraph.com/legacy-explorer/subgraph/kiwanoproject/lottery)**: Tracks all kiwanoproject Lottery with rounds, draws and tickets.

5. **[NFT Market (v1)](https://thegraph.com/legacy-explorer/subgraph/kiwanoproject/nft-market)**: Tracks all kiwanoproject NFT Market for ERC-721.

6. **[Pairs](https://thegraph.com/legacy-explorer/subgraph/kiwanoproject/pairs)**: Tracks all kiwanoproject Pairs and Tokens.

7. **[Pancake Squad](https://thegraph.com/legacy-explorer/subgraph/kiwanoproject/pancake-squad)**: Tracks all Pancake Squad metrics with Owners, Tokens (including metadata), and Transactions.

8. **[Prediction (v1)](https://thegraph.com/legacy-explorer/subgraph/kiwanoproject/prediction)**: Tracks all kiwanoproject Prediction (v1) with market, rounds, and bets.

9. **[Prediction (v2)](https://thegraph.com/legacy-explorer/subgraph/kiwanoproject/prediction-v2)**: Tracks all kiwanoproject Prediction (v2) with market, rounds, and bets.

10. **[Profile](https://thegraph.com/legacy-explorer/subgraph/kiwanoproject/profile)**: Tracks all kiwanoproject Profile with teams, users, points and campaigns.

11. **[SmartChef](https://thegraph.com/legacy-explorer/subgraph/kiwanoproject/smartchef)**: Tracks all kiwanoproject SmartChef (a.k.a. Syrup Pools) with tokens and rewards.

12. **[Timelock](https://thegraph.com/legacy-explorer/subgraph/kiwanoproject/timelock)**: Tracks all kiwanoproject Timelock queued, executed, and cancelled transactions.

13. **[Trading Competition (v1)](https://thegraph.com/legacy-explorer/subgraph/kiwanoproject/trading-competition-v1)**: Tracks all metrics for the Easter Battle (April 07—14, 2021).

14. **[MasterChef (v2)](https://thegraph.com/hosted-service/subgraph/kiwanoproject/masterchef-v2)**: Tracks data for MasterChefV2.


## Dependencies

- [Graph CLI](https://github.com/graphprotocol/graph-cli)
    - Required to generate and build local GraphQL dependencies.

```shell
yarn global add @graphprotocol/graph-cli
```

## Deployment

For any of the subgraph: `blocks` as `[subgraph]`

1. Run the `cd subgraphs/[subgraph]` command to move to the subgraph directory.

2. Run the `yarn codegen` command to prepare the TypeScript sources for the GraphQL (generated/*).

3. Run the `yarn build` command to build the subgraph, and check compilation errors before deploying.

4. Run `graph auth --product hosted-service '<ACCESS_TOKEN>'`

5. Deploy via `yarn deploy`.
