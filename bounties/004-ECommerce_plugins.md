# Ecommerce Plugins

Wordpress has become the reference framework for a lot of websites, including ecommerce websites.  
With an Ecommerce plugin, it's easy to build a simple shop on top of Wordpress.  

Woo commerce is probably the most used or known such plugin for physical goods, whereas Easy digital downloads fits digital goods.  
We target both of these plugins with a payment gateway add-on.

**Status: Open**  
> You can work on this and be rewarded

## Amount

TBD

## Potential extensions to the bounty

Payment gateways for Prestashop and Magento could also be rewarded.  
Please contact us on discord if this is your area of expertise.

## Generic specifications

- Code has to be released as open source, either GPL or MIT licence
- Code has to be your work, port of an existing open source project is ok if mentionned and the added value is real.
- Minimal use of external dependencies and frameworks. The task is small enough for vanilla code to fit well.
- variables names and code comments are to be in English

Things that can be worked on in a second step, by further exchanges with devs:

- Minimal user doc has to be provided (install/config/usage)
- Minimal dev doc has to be provided (general lines, code and files architecture)
- Texts that will surface into the UI will use gettext so the plugin can be translated via po/mo files, and use english as base language.  (the translation itself is not part of the bounty, but the plugin has to be translatable eventually)

The add on can support Woo Commerce alone, EDD alone, or both.  
A single plugin supporting both would be easier to maintain and could get a bonus.  
MyCryptocheckout for instance supports both https://wordpress.org/plugins/mycryptocheckout/

At every stage, the Bismuth Team is willing to help and assist with code sample, tools, doc, specs, test cases, architecture choice, anything we can. You are not necessarily alone. Even junior developers can give it a try.  
Teams also are allowed (with one representative).


## Bismuth Related specifications

- The gateway has to rely on wallet servers and protocol (native api or websocket one)
- No private API can be used for chain interaction
- Public, known and stable APIs (like coingecko) can be used for exchange and price data.
- Uses custom data field of bismuth transactions to link order and payment
- Use of polling to get the transactions status (1/min at most)
- connects to a specific wallet server (can be a private one) or use the Bismuth wallet API to get a list of working public ones.

> We provide unlimited support for that side.

## Woo-Commerce specifications

https://wordpress.org/plugins/woocommerce/

- Extension has to support current versions of WP and the woocommerce plugin
- Integration with woocommerce payment options
- code/template separation
- No redirection or iframes
- Generate bisurl and bisurl qrcode
- Display raw payment address and data as well for wallets not supporting bis urls

- ex: https://wordpress.org/plugins/gourl-woocommerce-bitcoin-altcoin-payment-gateway-addon/  
  (but uses custom api)
- ex: https://wordpress.org/plugins/woo-altcoin-payment-gateway/  
  (but uses custom api)
- ex: https://wordpress.org/plugins/spectrocoin-accepting-bitcoin/  
  (older but simpler)
- ex: https://github.com/Pennykoin-Dev-Team/Woocommerce-Pennycoin-Payment  
  user made one for penny coin


## Easy Digital Downloads

https://wordpress.org/plugins/easy-digital-downloads/  

- Has to support current versions of WP and the Easy Digital Downloads plugin
- code/template separation
- No redirection or iframes
- Generate bisurl and bisurl qrcode
- Display raw payment address and data as well for wallets not supporting bis urls

Easy digital download lists a lot of gateways add on, including github to thirs party ones.

## Bismuth References

WIP, to be completed with links.

- Bismuth API, inc. PHP client
- TODO: php bisurl class
- Hack with Bis
- "How to integrate" document, for exchanges
- TODO: Bismuth wallet API: how to get/use the list of working servers
- Ask in #dev Discord channel https://discord.gg/8KvA3JU

