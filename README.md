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
If this helped you in any way, you can always leave me a tip at
```
(Ripple) rPz4YgyxPpk7xqQQ9P7CqNFvK17nhBdfoy
(BTC)    1Mhq9SY6DzPhs7PNDx7idXFDWsGtyn7GWM
(ETH)    0xb0f2d091dcdd036cd26017bb0fbd6c1488fc8d04
(LTC)    LTfP7yJSpGFvuPqjSEKaqcjue6KSA9118y
(XVG)    D5nBpFBaD6vmVJ5CBUhkz8E4SNWscf6pMu
(BNB)    0xb0f2d091dcdd036cd26017bb0fbd6c1488fc8d04
```

Sign up to [Cointracking](https://cointracking.info?ref=M263159) which uses APIs to connect to all exchanges and helps you with tax. Use [Binance Exchange](https://www.binance.com/?ref=13896895) to trade #altcoins. Join [TradingView](http://tradingview.go2cloud.org/aff_c?offer_id=2&aff_id=7432) to get trend-reports.

If you are poor, follow me at least on [Twitter](https://twitter.com/gerdnaschenweng)!
