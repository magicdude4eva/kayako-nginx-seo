# kayako-nginx-seo
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
