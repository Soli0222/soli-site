+++
title = 'Fediverse2年目を振り返る'
date = 2024-12-19T00:00:00+09:00
draft = true
categories = ["AdventCalendar", "Fediverse", "Misskey"]
+++

この記事は[Fediverse Advent Calendar 2024](https://adventar.org/calendars/10064) 19日目の記事です。

## はじめに

みなさん、こんにちは。Misskeyサーバー・Polestarを運営していますSoliです。  
Fediverse Advent Calendar 2024ということで、Fediverse2年目の振り返りをしていこうと思います。

去年のFediverse Advent Calendarでは1年目として振り返りをしたので、年末の恒例行事のようなものですね。

![サーバートップページの画像](https://media.soli0222.com/polestar/134ad96f-3eb0-45a7-bee4-4327e21330d5.webp)

## 今年やったこと

去年はそもそもFediverseに参入し、Misskeyサーバーを建てるという一大イベントがありましたが、今年はそれに並ぶような出来事はなかったかなあと思います。それだけ堅実にサーバーを運営していた1年だったといえますね。

### 独自実装

とはいえ、ユーザーからの要望に基づく独自機能の実装はいくつか行いましたので、紹介していきます。

#### バブルゲームの全期間ランキング

年始の各Misskeyサーバーといえば、全員バブルゲームやってるみたいな、一大ブームがあったかと思います。  
Polestarでも暇さえあればやってるといったユーザーが多く、非常に楽しんでいました。

バブルゲームが流行したひとつの要因として、ランキング機能があるかと思います。  
ユーザー間でのスコアが比較されることで、中毒性により拍車をかけていた気がします。  

ただ、このランキングは直近7日間のスコアで表示されるので、サーバー内でのハイスコアは基本的には見れない物になっています。  
しかし、過去のスコア自体はすべてデータベースに存在しているので、これを使って全期間のランキングを実装しました。

![バブルゲーム_全期間ランキング](https://media.soli0222.com/polestar/4940b4d1-25d3-494f-beb2-7111783ad5a2.webp)

#### NoNyaizeモード

Misskeyといえば、猫耳を生やして猫語になる猫モードがありますが、この猫語の部分を無効化できるオプションを追加しました。  
猫耳だけ生やしたいという要望に応えた形です。

猫耳を生やしているが、`な`が`にゃ`になっていない図。  

<iframe src="https://mi.soli0222.com/embed/notes/a193o5jy2a" data-misskey-embed-id="v1_098fc0e1-c714-4ce1-8a19-0cad7bd9a4cf" loading="lazy" referrerpolicy="strict-origin-when-cross-origin" style="border: none; width: 100%; max-width: 500px; height: 300px; color-scheme: light dark;"></iframe>
<script defer src="https://mi.soli0222.com/embed.js"></script>

#### その他

他にも、以下のような独自実装を加えています。

- リバーシにて、フリーマッチ待機中ノートをできるように
- `ctrl + shift`で公開範囲を、連合なし&フォロワーのみに出来るように
- サーバーとの接続が切断されたときの設定に、警告しないオプションを追加
- D○site的な言葉の変換がされるモードを追加
- アップデート後のスプラッシュ画面でキャッシュクリアできるように

### 本体へのコントリビュート

だいぶ軽い不具合修正ですが、Misskey本体へのコントリビュートも行いました。  
来年も本体の不具合を見つけたら、PR送りたいですね。

<div class="iframely-embed"><div class="iframely-responsive" style="height: 140px; padding-bottom: 0;"><a href="https://github.com/misskey-dev/misskey/pull/13172" data-iframely-url="//iframely.net/nU9lATk?card=small"></a></div></div><script async src="//iframely.net/embed.js"></script>

## 来年に向けて

このように、今年はいくつかMisskeyサイドに独自実装を加える程度になりました。  
Misskeyサーバーとしての運営は、小規模サーバーだとこんな感じでうまく行ってしまうものなのかもしれません。

しかし、サーバーの運用面では以下のような課題を抱えています。

- アップデート作業がめんどくさい (サーバーに対するほとんどが手作業)
  - Misskeyがsystemdで動いているので作業手順が多い
  - 別ホストで動いているMisskey関連コンポーネントに対する作業も必要になる
- 監視周りが不十分
  - 現状はサーバーホストのNode Exporter, Misskeyの外形監視uptime kumaのみ
  - Lokiを導入してログの監視もしたい
  - まともにアラートも整備したい


後者に関してはやろうと思えば出来る状態にあるのですが、やってしまうと前者の手作業が多いという課題をより大きくしてしまいます。

そこで、Misskeyを含むすべての運用をKubernetesクラスタに移す計画を思案しています。  
このクラスタは、構築プロセスにTerraformとAnsible、KubernetesへのデプロイにHelmを用いるといったIaCベースなものになっています。

作業や保守コストをできる限り減らしつつ、より充実した運用を行えるよう、整えていく年にしていきたいです。  
(とはいえ、Misskey本体はこのままVPSに置いておいたほうがいいかなあとも思っている)

## おわりに

大きな動きはありませんでしたが、2年目も楽しんでMisskeyサーバーの運営を行うことができました。  
来年も楽しんでやっていきます。  
ご覧いただき、ありがとうございました。