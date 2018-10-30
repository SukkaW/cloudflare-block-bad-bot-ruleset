<p align="center">
<img src="https://i.loli.net/2018/10/30/5bd7b06b077df.png" width="200px">
</p>
<h1 align="center">Cloudflare Block Bad Bot Ruleset</h1>

<p align="center">
<a href="https://suka.moe" target="_blank"><img alt="Author" src="https://img.shields.io/badge/Author-Sukka-b68469.svg?style=flat-square"/></a>
<a href="./LICENSE" target="_blank"><img alt="License" src="https://img.shields.io/github/license/sukkaw/cloudflare-block-bad-bot-rules.svg?style=flat-square"/></a>
<a href="https://www.cloudflare.com" target="_blank"><img alt="Cloudflare" src="https://img.shields.io/badge/integrated-cloudflare-f27f23.svg?style=flat-square"/></a>
</p>

> Block bad, possibly even malicious web crawlers (automated bots) using Cloudflare Firewall Rules<br>
> 使用 Cloudflare Firewall Rules 拦截恶意网络爬虫（自动机器人）和其它恶意流量

## Introduction 简介

`Cloudflare Block Bad Bot Ruleset` projects stop and block Bad Bot, Spam Referrer, Adware, Malware and any other kinds of bad internet traffic ever reaching your web sites. Inspired by [nginx-badbot-blocker](https://github.com/mariusv/nginx-badbot-blocker) & integrated with Cloudflare Firewall Rules.

`Cloudflare Block Bad Bot Ruleset` 可以阻止恶意爬虫、垃圾引荐来源、广告、恶意软件以及任何其他类型的恶意互联网流量到达您的网站。灵感来自 [nginx-badbot-blocker](https://github.com/mariusv/nginx-badbot-blocker) 并与 Cloudflare Firewall Rules 集成。

## Precautions 注意事项

`Cloudflare Block Bad Bot Ruleset` mainly based on User-Agent, which is known to all that could be changed easily. So the project can not replace the Web Application Firewall.

`Cloudflare Block Bad Bot Ruleset` 主要基于 User-Agent，但是众所周知 User-Agent 可以伪装，所以本项目并不能取代正规的 Web Application Firewall。

## Ruleset 规则

Rule Name | File Name | Action | What For
---- | ---- | ---- | ----
Allow Good Bot | [allow-good-bot.rules](./allow-good-bot.rules) | Allow | Allow known good bot.<br>放行已知的正常爬虫
Block Aliyun Yundun | [block-aliyun-yd.rules](./block-aliyun-yd.rules) | Block | Block Aliyun Yundun based on known IP cidr.<br>基于已知 IP 段拦截阿里云盾
Block Bad Bot (Basic) | [block-bad-ua.rules](./block-bad-ua.rules) | Block/Challenge | Block some known bad bot.<br>拦截一些基本的已知的恶意爬虫
Block Bad Bot (Extra) | [block-bad-ua-extra-0.rules](./block-bad-ua-extra-0.rules)<br>[block-bad-ua-extra-1.rules](./block-bad-ua-extra-1.rules)<br>[block-bad-ua-extra-2.rules](./block-bad-ua-extra-2.rules) | Block/Challenge | Block mostly known bad bot, basic ruleset not included.<br>拦截绝大部分已知的恶意爬虫，不包括基本规则

## More Information 更多详情

- [Announcing Firewall Rules | Cloudflare Blog](https://blog.cloudflare.com/announcing-firewall-rules/)
- [Cloudflare Firewall Rules | Cloudflare Documentations](https://developers.cloudflare.com/firewall/)
- [nginx-badbot-blocker | GitHub](https://github.com/mariusv/nginx-badbot-blocker)
- [nginx-ultimate-bad-bot-blocker | GitHub](https://github.com/mitchellkrogza/nginx-ultimate-bad-bot-blocker)

## Todo List

- [ ] Bad referrer list
- [ ] Known bad IP List

## Maintainer 维护者

**Cloudflare Block Bad Bot Ruleset** © [Sukka](https://github.com/SukkaW), Released under the [MIT](./LICENSE) License.

> [Personal Website](https://skk.moe) · [Blog](https://blog.skk.moe) · GitHub [@SukkaW](https://github.com/SukkaW) · Telegram Channel [@SukkaChannel](https://t.me/SukkaChannel) · Twitter [@isukkaw](https://twitter.com/isukkaw) · Keybase [@sukka](https://keybase.io/sukka)
