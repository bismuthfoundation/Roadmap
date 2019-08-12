# Ecommerce Plugin

Wordpress has become the reference framework for a lot of websites, including ecommerce websites.  
With an Ecommerce plugin, it's easy to build a simple shop on top of Wordpress.  

Woo commerce is probably the most used or known such plugin for physical goods, whereas Easy digital downloads fits digital goods.  
We target both of these plugins with a payment gateway add-on.

**Status: Open**  
> You can work on this and be rewarded

## Amount

TBD

## Potential extensions to the bounty

Payment gateways for Prestashop and Magento could also be rewarded.  
Please contact us on discord if this is your area of expertise.

## Generic specifications

- Code has to be released as open source, either GPL or MIT licence
- Code has to be your work, port of an existing open source project is ok if mentionned and the added value is real.
- Minimal use of external dependencies and frameworks. The task is small enough vanilla code fits well.
- Minimal user doc has to be provided (install/config/usage)
- Minimal dev doc has to be provided (general lines, code and files architecture)
- variables names and code comments are to be in English
- Texts that will surface into the UI will use gettext so the plugin can be translated via po/mo files, and use english as base language.  
(the translation itself is not part of the bounty, but the plugin has to be translatable)


## Bismuth Related specifications

- The gateway has to rely on wallet servers and protocol (native api or websocket one)
- No private API can be used for chain interaction
- Public, known and stable APIs (like coingecko) can be used for exchange and price data.

## Woo-Commerce


## Easy Digital Downloads


## Reference

- Bismuth API, inc. PHP client
- Hack with Bis
- "How to integrate" document, for exchanges

