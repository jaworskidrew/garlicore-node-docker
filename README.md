Garlicore Node + Insight API + Insight UI in Docker
=========

To run **testnet** (the default):

`docker run -d -p 3001:3001 -p 42075:42075 -v /root/garlicoin-node/testnet:/root/garlicoin-node/data --name garlicoin-testnet garlicore-node`

To run for **livenet**:

`docker run -e GARLICOIN_LIVENET=1 -d -p 3001:3001 -p 42069:42069 -v /root/garlicoin-node/livenet:/root/garlicoin-node/data --name garlicoin-livenet garlicore-node`


Tip: Ports 42069 (livenet) and 42075 (testnet) are inbound for garlicoind. Exposing them is just recommended.

### Environment variables

- `GARLICOIN_LIVENET` (default: 0) - Set 1 to enable livenet
- `API_ROUTE_PREFIX` (default: api) - Set URL prefix for Insight API
- `UI_ROUTE_PREFIX` (default: "") - Set URL prefix for Insight UI
- `API_CACHE_ENABLE` (default: 1) - Enable/disable Insight API cache
- `API_LIMIT_ENABLE` (default: 1) - Enable/disable Insight API rate limiter
- `API_LIMIT_WHITELIST` (default: "127.0.0.1 ::1") - Whitelist, delimited by space
- `API_LIMIT_BLACKLIST` (default: "") - Blacklist, delimited by space
- `API_LIMIT_COUNT` (default: 10800)
- `API_LIMIT_INTERVAL` (default: 10800000)
- `API_LIMIT_WHITELIST_COUNT` (default: 108000)
- `API_LIMIT_WHITELIST_INTERVAL` (default: 10800000)
- `API_LIMIT_BLACKLIST_COUNT` (default: 0)
- `API_LIMIT_BLACKLIST_INTERVAL` (default: 10800000)
