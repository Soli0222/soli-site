+++
title = '自鯖向けMisskey独自実装2023'
date = 2023-12-20T00:00:00+09:00
draft = false
categories = ["AdventCalendar", "Fediverse", "Misskey"]
+++

この記事は [Misskey Advent Calendar 2023](https://adventar.org/calendars/8742) 20日目の記事です。

## はじめに

みなさん、こんにちは。Misskeyサーバー・Polestarを運営している[Soli](https://mi.soli0222.com/@Soli_0222)です。
Misskey Advent Calendar 2023ということで、今年自鯖向けに独自実装した話を書こうと思います。

## なぜ独自実装したのか

そもそも、バニラのMisskeyで十分すぎるほど機能がありますが、これに独自実装を加えてるサーバーは多い印象があります。

弊鯖では、身内向けサーバーであるので、メンバーからの要望があったものや、極度な身内ネタに走ったおもしろ機能などを実装しており、8割がノリと勢い、2割がUXの向上のために実装をしています。

## 実装例

ここからはどんな実装をしたのか紹介していきます。([リポジトリ](https://github.com/Soli0222/misskey))

### myaize

Misskeyには「な」が「にゃ」になるユーザー困らせ機能、nyaizeがあります。これを模倣した機能で、「ま」が「みゃ」になります。
(極度の身内ネタが元になっています)

![myaize設定画面](https://media.soli0222.com/polestar/1d5999fb-d175-447e-ac1e-b6107d64d1cc.webp)

これが初めての独自実装なのですが、初っ端からDBに手を付けてしまい、非常に緊張しました。

![myaizeプレビュー](https://media.soli0222.com/polestar/632c1cd5-cd63-4b88-a9d1-2928f721538f.png)

### サークル

サーバーメンバーは元々Twitterサークルでエアリプを繰り返していた間柄なので、Misskeyにおいてもフォロワーのみ連合なしといった、閉鎖的な使い方をしています。そんなときに、公開範囲を簡単に絞れるようにボタンを実装しました。

![サークルプレビュー](https://media.soli0222.com/polestar/6c0e1f10-0cae-4686-9aff-9468b52a24fd.gif)

### Spotify NowPlayingボタン

Spotifyで再生している曲をMisskeyにいながら簡単にノートするためのウィジェットを追加しました。

![Spotify NowPlauingボタン](https://media.soli0222.com/polestar/67b0d129-fccc-4d37-8f4d-154963f1ed38.webp)

Misskey自体に変更を加えたのはこのボタンの実装のみで、ボタンをタップすると別サーバーでホスティングしているWebアプリに飛び、そのアプリがいい感じの文言で共有フォームに飛ばすといった感じになっています。

![spn実行画面](https://media.soli0222.com/polestar/4c967afb-2826-4013-811c-2f913a388dfd.gif)

### お気に入りボタン

ノートのリノートボタンの並びにお気に入りに追加するためのボタンを実装しました。

![お気に入りボタン](https://media.soli0222.com/polestar/59aa2b66-fb19-48b7-bccc-e46f911689da.png)

サーバーメンバーからの要望があり、個人的にも欲しかったので実装しましたが、なかなか便利です。

![お気に入りボタン](https://media.soli0222.com/polestar/79f5667d-07e0-4025-b6ac-fa295f9eda3d.gif)

## 終わりに

主要な独自要素は以上になります。こうして自分やサーバーメンバーの使いやすい用にカスタマイズするのも、オープンソースならではの楽しさですね。これからも、ノリと勢いでカスタマイズしていきたい気持ちでいます。
