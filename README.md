Cryptocurrency exchange monitoring.

This repository aims to implement a real-time monitoring of cryptocurrency exchanges.

## Exchange Support Table

| Exchange | REST API | Streaming API | FIX API |
|----------|------|-----------|-----|
| Alphapoint | Yes  | Yes        | NA  |
| ANXPRO | Yes  | No        | NA  |
| Binance| Yes  | Yes        | NA  |
| Bitfinex | Yes  | Yes        | NA  |
| Bitflyer | Yes  | No      | NA  |
| Bithumb | Yes  | NA       | NA  |
| BitMEX | Yes | No | NA |
| Bitstamp | Yes  | Yes       | No  |
| Bittrex | Yes | No | NA |
| BTCC | Yes  | Yes     | No  |
| BTCMarkets | Yes | No       | NA  |
| COINUT | Yes | No | NA |
| Exmo | Yes | NA | NA |
| CoinbasePro | Yes | Yes | No|
| GateIO | Yes | No | NA |
| Gemini | Yes | No | No |
| HitBTC | Yes | Yes | No |
| Huobi.Pro | Yes | No | NA |
| Huobi.Hadax | Yes | No | NA |
| ItBit | Yes | NA | No |
| Kraken | Yes | NA | NA |
| LakeBTC | Yes | No | NA |
| Liqui | Yes | No | NA |
| LocalBitcoins | Yes | NA | NA |
| OKCoin China | Yes | Yes | No |
| OKCoin International | Yes | Yes | No |
| OKEX | Yes | No | No |
| Poloniex | Yes | Yes | NA |
| WEX     | Yes  | NA        | NA  |
| Yobit | Yes | NA | NA |
| ZB.COM | Yes | No | NA |

We are aiming to support the top 20 highest volume exchanges based off the [CoinMarketCap exchange data](https://coinmarketcap.com/exchanges/volume/24-hour/).

** NA means not applicable as the Exchange does not support the feature.

## Current Features

+ Support for all Exchange fiat and digital currencies, with the ability to individually toggle them on/off.
+ AES256 encrypted config file.
+ REST API support for all exchanges.
+ Websocket support for applicable exchanges.
+ Ability to turn off/on certain exchanges.
+ Ability to adjust manual polling timer for exchanges.
+ Communication packages (Slack, SMS via SMSGlobal, Telegram and SMTP)
+ HTTP rate limiter package.
+ Forex currency converter packages (CurrencyConverterAPI, CurrencyLayer, Fixer.io, OpenExchangeRates)
+ Packages for handling currency pairs, tickers and orderbooks.
+ Portfolio management tool; fetches balances from supported exchanges and allows for custom address tracking.
+ Basic event trigger system.
+ WebGUI.

## Planned Features

Planned features can be found on our [community Trello page](https://trello.com/b/ZAhMhpOy/gocryptotrader).

## Contribution

Please feel free to submit any pull requests or suggest any desired features to be added.

When submitting a PR, please abide by our coding guidelines:

+ Code must adhere to the official Go [formatting](https://golang.org/doc/effective_go.html#formatting) guidelines (i.e. uses [gofmt](https://golang.org/cmd/gofmt/)).
+ Code must be documented adhering to the official Go [commentary](https://golang.org/doc/effective_go.html#commentary) guidelines.
+ Code must adhere to our [coding style](https://github.com/thrasher-/gocryptotrader/blob/master/.github/CONTRIBUTING.md).
+ Pull requests need to be based on and opened against the `master` branch.

## Compiling instructions

Download and install Go from [Go Downloads](https://golang.org/dl/) for your
platform.

### Linux/OSX

GoCryptoTrader is built using [Go Modules](https://github.com/golang/go/wiki/Modules) and requires Go 1.11 or above
Using Go Modules you now clone this repository **outside** your GOPATH

```bash
git clone https://github.com/thrasher-/gocryptotrader.git
cd gocryptotrader
go build
mkdir ~/.gocryptotrader
cp config_example.json ~/.gocryptotrader/config.json
```

### Windows

```bash
git clone https://github.com/thrasher-/gocryptotrader.git
cd gocryptotrader
go build
copy config_example.json %APPDATA%\GoCryptoTrader\config.json
```

+ Make any neccessary changes to the `config.json` file.
+ Run the `gocryptotrader` binary file inside your GOPATH bin folder.

