---
layout: post
title:  "精算ちゃん"
categories: product
tags: Flutter, Firebase
image: /assets/image/screen-seisan.png
---

グループで精算を行うアプリです。

- [App Store](https://apps.apple.com/jp/app/%E7%B2%BE%E7%AE%97%E3%81%A1%E3%82%83%E3%82%93-%E3%82%B7%E3%83%B3%E3%83%97%E3%83%AB%E5%89%B2%E3%82%8A%E5%8B%98%E3%82%A2%E3%83%97%E3%83%AA/id6444388748)
- [Google Play](https://play.google.com/store/apps/details?id=com.guntamania.seisanchan&pcampaignid=web_share)

## 概要

複数人でイベントをしたときに割り勘や精算を行うツールです。
FireStoreにてデータの共有を行いますが、そのときに払い出されるハッシュ使ったURLを共有することで、ログインなしで精算結果を共有することができます。

## 技術背景

Flutterで制作しており、両OSをワンコードで管理しています。
また、状態管理には `hooks_riverpod` を用いており、またマルチレイヤーによるモダンな設計を採用しています。
