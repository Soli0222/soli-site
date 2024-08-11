+++
title = 'デスク周りの設備を良い感じにした'
date = 2024-08-12T01:26:00+09:00
draft = true
categories = ["Blog"]
+++

## はじめに

8ヶ月ぶりの更新らしい。こんにちは。  

デスク周りの設備を大幅に更新したのですが、その構成で、紆余曲折ありました。
モデルケースを探そうにも出てこないしで余計に時間がかかってしまったので、
同じようなことをしようとしている誰かの参考になればと思い、インターネットに記録を残しておきます。  

ここで触れる設備は、PCやゲーム機からの映像・音声の出力周りのことです。

## 環境

扱う映像ソースとモニターは以下の通りです。

- 映像ソース
    - M3 MacBook Air (メインPC)
    - 自作PC (ゲーム機/開発機)
    - 社用PC (リモートワーク用)
    - Nintendo Switch
- モニター
    - メイン: Dell U4025QW (5K2K/120Hz, USB-C/DP/HDMI)
    - サブ: JAPANNEXT JN-IPS315UHDR (4K/60Hz)

これらの機器を、ケーブルの抜き差し無くうまく切り替えて使いたいなあという軽いお気持ちで沼が始まりました。  
純粋に多ポートなディスプレイを用意したり、HDMIスプリッターのような切り替え機を用いたりすれば、
簡単に実現できそうですが、以下の条件が頭を悩ませました。

- メインPCはデュアルモニター
- 自作PCは120Hzで出力
- メインPCの音声と、ほかの機器の音声をミキシングして聴きたい
- メインディスプレイは5K2K 120Hzのディスプレイ(HDMI 2.1必須)
- 先走って買ったYamaha ZG01を使いたい

具体的なユースケースを上げるなら、メインPCでYouTubeをサブディスプレイで再生しながら、
メインディスプレイで自作PCやSwitchでゲームをするというような使い方が上げられます。

## 構成

いろいろ試行錯誤していたので細かな変更は大量にありますが、大きく分けて2構成あるので、2つ紹介します。

### 初期構成

初期は、以下のような構成でした。

![deskv1](https://media.soli0222.com/polestar/ee596527-82c8-4073-9221-27ae9a678d63.png)

Yamaha ZG01というのは、PCの音声と、HDMI入力の音声をミキシングしてくれるオーディオミキサーです。
HDMI入力が2発、出力が1発を備えており、この入力を切り替えて出力できるHDMIスプリッターのような機能を持っています。

<div class="iframely-embed"><div class="iframely-responsive" style="height: 140px; padding-bottom: 0;"><a href="https://jp.yamaha.com/products/proaudio/live_streaming_gaming/zg/zg01/index.html" data-iframely-url="//iframely.net/TrsxL9B?card=small"></a></div></div><script async src="//iframely.net/embed.js"></script>

最初見つけたときは、あまりに神機器で、もうこれだけあればもう終わりなのでは無いかと思いましたが、残念な点が一つ。
このHDMIはHDMI2.0なので、4K60Hzが入出力の限界になります。Switch側は問題無いのですが、自作PC側の出力がこれに制限されてしまいます。
つまり、5K2Kの出力すらできないし、120Hzも出ません。

そこで、自作PCからはDisplayPortを使って、モニターに直接入力、ZG01に対しても入力をするが、映像出力は使わないという方法を用いました。

ZG01は映像出力の有無に関係なく、入ってきた音声をミキシングするし、映像ソース側には映像出力機器として認識させるので、問題無く動いてくれます。

さて、この図には社用PCがいません。当初はリモートワークする予定が無かったので、これで十分でした。仮にもするなら、SwitchのHDMIを外せばいいやくらいに思っていました。

ところがどっこい、週一程度にはリモートをするようになり、毎週Switchと抜き差し繰り返すのはめんどくさいなあとなりました。
というかそもそも、ZG01のHDMI2.0な仕様にぶち当たってしまうので、社用PCから5K2Kの出力ができません。

### 確定構成

そこで、以下のような構成になりました。

![deskv2](https://media.soli0222.com/polestar/8ceea96c-708f-47c6-b15f-db0cda6ff940.png)

もうめちゃくちゃです。(図以上に物理配線がエグい)

まずは、ZG01のHDMI2.0仕様に阻まれるのを回避するため、モニターに対する入力はHDMI2.1なスプリッターを使うことにしました。  
こうすることで、社用PCからは5K2K出せますし、Switchからの入力も問題無く出せます。ケーブルの切り替え無く、切り替えもできます。

<div class="iframely-embed"><div class="iframely-responsive" style="height: 140px; padding-bottom: 0;"><a href="https://www.sanwa.co.jp/product/syohin?code=SW-HDR8K21BD" data-iframely-url="//iframely.net/DjoCEy4"></a></div></div><script async src="//iframely.net/embed.js"></script>

そんなに高いもんでもなかったので、もう一本買って、ZG01に対する入力にも使っています。  

社用PCにはHDMIポートがあり、もともとThunderboltドックを使うつもりで、ここにもHDMIポートが付いていたので、問題ありませんでした。

しかし、Switchからの出力は、1ポートしかないので、1入力2同時出力できる機器が必要になりました。  
Switchはまあ、HDMI2.0でも問題無いやろ(後継機もあって4K60Hzが限界だろ)という感じで、これを使いました。

<div class="iframely-embed"><div class="iframely-responsive" style="height: 140px; padding-bottom: 0;"><a href="https://www.amazon.co.jp/UGREEN-HDMI%E3%82%B9%E3%83%97%E3%83%AA%E3%83%83%E3%82%BF%E3%83%BC-%E3%80%90HDMI%E3%82%B1%E3%83%BC%E3%83%96%E3%83%AB%E4%BB%98%E3%81%8D%E3%80%91%EF%BC%92%E7%94%BB%E9%9D%A2%E5%90%8C%E6%99%82%E5%87%BA%E5%8A%9B3D%E6%98%A0%E5%83%8F%E5%AF%BE%E5%BF%9C-Nintendo-Switch%E5%8B%95%E4%BD%9C%E7%A2%BA%E8%AA%8D%E6%B8%88%E3%81%BF%E3%80%91/dp/B0B129NNV1" data-iframely-url="//iframely.net/nMaTYSb?card=small"></a></div></div><script async src="//iframely.net/embed.js"></script>

こんな感じで、現状満足いくような構成を実現しました。

#### 余談1

手前に見えるのがZG01、奥に見えるのが、モニターとZG01に入るスプリッターです。  
社用PCもしくはSwitchを使うときには、ZG01の切り替えボタンで、2系にします。  
また、Switchをスプリッターの2番ポートにしているので、スプリッターの切り替えボタンも両方押す必要があります。

![desk](https://media.soli0222.com/polestar/bce5bb7a-f3ce-4415-b73c-348c5d0a3cb1.jpg)

#### 余談2

ZG01は、箱を開けた瞬間ういママが出てきます。HDMIの仕様なんてどうでもよくなります。

![ui](https://media.soli0222.com/polestar/8c046571-c6b1-43d2-82c0-9236412e1445.jpg)

## まとめ

こんな感じで、ぼくのかんがえた最強の机が完成しました。  
誰かの参考になればいいなと思いつつ、もっと良いやり方があるかもしれません。

ぜひ皆さんも自分の机上設備を解説してください。