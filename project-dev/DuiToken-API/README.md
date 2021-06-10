---
#### <img src="https://raw.githubusercontent.com/DuiToken/DuiToken/master/assets/Dui-icon.png" width="12" height="12" /> [Root](https://github.com/DuiToken/DuiToken) | [Assets](https://github.com/DuiToken/DuiToken/tree/master/assets) | [Audit](https://github.com/DuiToken/DuiToken/tree/master/audit) | [Contract & Dev Notes](https://github.com/DuiToken/DuiToken/tree/master/contract) | [LP Wallet log](https://github.com/DuiToken/DuiToken/blob/master/contract/LP-Wallet-log.md) | [```DuiToken API```](https://github.com/DuiToken/DuiToken/tree/master/project-dev/DuiToken-API)
---

[![ci](https://github.com/Triex/DuiToken-API/actions/workflows/ci.yml/badge.svg)](https://github.com/Triex/DuiToken-API/actions/workflows/ci.yml)

# DuiToken API

A Node.js based API for $DUI.

## Features

- Circulating supply (total supply - total burned tokens)
- Total burned
- Price (USD or BNB)
- Volume (USD or BNB)

## Usage

### Circulating Supply

```
GET https://api.duitoken.com/v1/circulating-supply
```

```json
{ "circulatingSupply": 000000000000.000 }
```

### Total Burned

```
GET https://api.duitoken.com/v1/total-burned
```

```json
{ "totalBurned": 000000000000.0000 }
```

### Price

```
GET https://api.duitoken.com/v1/price?currency=bnb|usd
```

```json
{ "currency": "bnb", "price": "0.000000000000000000" }
```

```json
{ "currency": "usd", "price": "0.0000000000000000000000000000000000000000" }
```

### Volume

```
GET https://api.duitoken.com/v1/volume?currency=bnb|usd
```

```json
{ "currency": "bnb", "bnb_24h_vol": 00.000000000000000000 }
```

```json
{ "currency": "usd", "usd_24h_vol": 000000.000000000000 }
```

---

© 2021 [DúiToken](https://DuiCrypto.com)
