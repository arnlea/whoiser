# Simple Whois Client for NodeJS
This is a simple whois library to fetch whois information of any domain name. All TLDs are supported, the module can find the whois server of any TLD by querying IANA.

## How to install?
You can install the module with `npm i whoisme` command.

## Example code
```js
const whoisme = require('whoisme');

(async() => {
  let domain = 'google.com';
  let whoisData = await whoisme.getWhois(domain, config);
  console.log(whoisData);
})();
```

### How does it find the whois server?
The library keeps used whois servers in cache. But if it's not used before, it sends a request to [IANA Root DB](https://www.iana.org/domains/root/db) to find the whois server.
