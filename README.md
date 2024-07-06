## /etc/hosts on MacOS

* see https://raw.githubusercontent.com/StevenBlack/hosts/master/hosts

* Need to whitelist several items from that (e.g. anything that resolves to 0.0.0.0)

```console
cd /tmp
wget https://raw.githubusercontent.com/StevenBlack/hosts/master/hosts
cat hosts | grep -v 'googleadservices' | grep - v 'ad.doubleclick.net' > /etc/hosts
```


## AdGuard

### Add to AdGuard

https://raw.githubusercontent.com/rsnodgrass/dns-blocklists/main/adblock/personal-rules.txt

## My Recommended

* [HaGeZi's Pro Blocklist](https://adguardteam.github.io/HostlistsRegistry/assets/filter_48.txt)
* [HaGeZi's Theat Intelligence](https://adguardteam.github.io/HostlistsRegistry/assets/filter_44.txt)
* [HaGeZi's Personal](https://raw.githubusercontent.com/hagezi/dns-blocklists/main/adblock/personal.txt)

Read all about [HaGeZi's blocklists](https://github.com/hagezi/dns-blocklists).

## Sync Config

[AdGuard Home Sync](https://github.com/bakito/adguardhome-sync) can be used on replica instances to synchronize all configuration from a primary AdGuard instance. This enables running AdGuard in more of a high-availability model.

This can also be used to synchronize config between several sites so only one has to be configured and all others can follow along. Another optionn is to use [keepalived](https://www.virtualizationhowto.com/2023/09/keepalived-high-availability-for-self-hosted-services/) with virtual IPs (VRRP).

For static IP DNS resolvers, consider x.x.x.53 (or .51/.52).
