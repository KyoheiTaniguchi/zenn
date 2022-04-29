---
title: "相対パスと絶対パスの違い、使い分け"
emoji: "🛣"
type: "tech" # tech: 技術記事 / idea: アイデア
topics: ["flutter", "パス"]
published: true
---

# 目次

1. パスって何？
2. 相対パスとは？
3. 絶対パスとは？
4. どうやって使い分けるの？

## 1. パスとは？

パス「Path」とは、その名の通り、経路という意味です。
つまり、特定のファイルへのアクセスを可能にします。
Appなどの開発をする際には、import文を使用することで、特定のパッケージなどをインストールして使用することができるようになります。

#### 例
```dart
import 'package:flutter/material.dart';
```
Flutterで言うと、上記のパスを通すことで、マテリアルデザインのUIパッケージをインストールして使用することが可能になります。

そして、パスには「相対パス」と「絶対パス」という２種類のパスが存在します。

-----
## 2. 相対パスとは？

簡単に言うと、経路の全てを表示しないパスということです。
例えば、下記ファイルのwidgets.dartというファイルにアクセスしたいとします。

User/Takuro/Developer/flutter/packages/flutter/lib/widgets.dart
ここにアクセスするときは、UserからUser名、Developerと辿ってwidgets.dartへと到達しています。

相対パスの場合は、このパスの一部分である/lib/widgets.dartののように、省略されて表示されることが多いです。
そうすることで、作業負担を軽くしています。

-----
## 3. 絶対パスとは？

逆に絶対パスは、User/Takuro/Developer/flutter/packages/flutter/lib/widgets.dart
の全てを表示します。
つまり、誰から見ても明確なファイルの場所が表示されるので、リンクとして安定した働きをします。

-----
## 4. どうやって使い分けるの？

結論、外部からパッケージなどをインストールしたり、外部サイトへのアクセスをする場合は絶対パスを使いましょう。
逆に、内部だけでデータ取得したりするだけであれば、相対パスの使用が望ましいです。


簡単ですが以上です！👍


[参考]
https://it-trend.jp/development_tools/article/32-0055
https://techacademy.jp/magazine/5801