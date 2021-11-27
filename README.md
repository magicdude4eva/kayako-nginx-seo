# kayako-nginx-seo
[paypal]: https://paypal.me/GerdNaschenweng
![paypal](https://img.shields.io/badge/PayPal--ffffff.svg?style=social&logo=data%3Aimage%2Fpng%3Bbase64%2CiVBORw0KGgoAAAANSUhEUgAAABAAAAAQCAYAAAAf8%2F9hAAAABHNCSVQICAgIfAhkiAAAAZZJREFUOI3Fkb1PFFEUxX%2F3zcAMswFCw0KQr1BZSKUQYijMFibGkhj9D4zYYAuU0NtZSIiNzRZGamqD%2BhdoJR%2FGhBCTHZ11Pt%2B1GIiEnY0hFNzkFu%2FmnHPPPQ%2Buu%2BTiYGjy0ZPa5N1t0SI5m6mITeP4%2B%2FGP%2Fbccvto8j3cuCsQTSy%2FCzLkdxqkXpoUXJoUXJrkfFTLMwHiDYLrFz897Z3jT6ckdBwsiYDMo0tNOIGuBqS%2Beh7sdAkU2g%2BkBFGkd%2FrtSgD8Z%2BrBxj68MAGG1A9efRhVsXrKMU7Y4cNyGOwtDU28OtrqdUMetldvzFKxCYSHJ4NsJ%2BnRJGexHba7VJ%2FTff4BaQFBjVcbqIEZ1bESYn4PRUcHx2N952awUkOHZedUcWm14%2FtjqjREHawUEsgx6Ajg5%2Bsi7jWqBwA%2BmIrXlo9YHUVTmEP%2F6hOO1Ofiyy3pjo%2BsvBDX%2FZpSakhz4BqvQDvdYvrXQEXZViI5rPpBEOwR2l16vtN7bd9SN3L1WXj%2BjGSnN38rq%2B7VL8xXQOdDF%2F0KvXn8BlbuY%2FvUAHysAAAAASUVORK5CYII%3D)
___
:beer: **Please support me**: Although all my software is free, it is always appreciated if you can support my efforts on Github with a [contribution via Paypal][paypal] - this allows me to write cool projects like this in my personal time and hopefully help you or your business. 
___

Kayako nginx example with search-engine friendly URLs - this has been tested with Kayako 4.73.3 running on CentOS 7 with nginx/1.6.3

The nginx configuration includes:
- Gzip compression
- Security configuration
 - Turn off access to hidden files and sensitive context
 - XSS configuration to enforce SAMEORIGIN
 - Limiting buffer overflow issues
 - Restricting request methods
 - CSP in reporting mode (ensure that you register with report-uri.io / or remove)
- Remove logging of favicon.ico and robots.txt
- Custom error pages for nginx (those could be much better)
- Cache control for media images, dynamic data and CSS/JavaScript

With the above settings you have to change /__swift/config/config.php and remove `index.php` from SWIFT_BASENAME:
```
#define('SWIFT_BASENAME', 'index.php?');
define('SWIFT_BASENAME', '');
```

Included MySQL configuration and php.ini settings for a Kayako system running on CentOS7, MySQL 5.7.12, nginx on a 4-core, 10GB single-server.



## Donations are always welcome
:beer: **Please support me**: If the above helped you in any way, then [follow me on Twitter](https://twitter.com/gerdnaschenweng) or send me some coins: 
```
(CRO)    cro1w2kvwrzp23aq54n3amwav4yy4a9ahq2kz2wtmj (Memo: 644996249) or 0xb83c3Fe378F5224fAdD7a0f8a7dD33a6C96C422C (Cronos)
(USDC)   0xb83c3Fe378F5224fAdD7a0f8a7dD33a6C96C422C
(BTC)    3628nqihXvw2RXsKtTR36dN6WvYzaHyr52
(ETH)    0xb83c3Fe378F5224fAdD7a0f8a7dD33a6C96C422C
(BAT)    0xb83c3Fe378F5224fAdD7a0f8a7dD33a6C96C422C
(LTC)    MQxRAfhVU84KDVUqnZ5eV9MGyyaBEcQeDf
(Ripple) rKV8HEL3vLc6q9waTiJcewdRdSFyx67QFb (Tag: 1172047832)
(XLM)    GB67TJFJO3GUA432EJ4JTODHFYSBTM44P4XQCDOFTXJNNPV2UKUJYVBF (Memo ID: 1406379394)
```

Go to [Curve.com to add your Crypto.com card to ApplePay](https://www.curve.com/join#DWPXKG6E) and signup to [Crypto.com for a staking and free Crypto debit card](https://crypto.com/app/ref6ayzqvp).

Use [Binance Exchange](https://www.binance.com/?ref=13896895) to trade #altcoins. Sign up with [Coinbase](https://www.coinbase.com/join/nasche_x) and **instantly get $10 in BTC**. I also accept old-school **[PayPal](https://paypal.me/GerdNaschenweng)**.

If you have no crypto, follow me at least on [Twitter](https://twitter.com/gerdnaschenweng).
