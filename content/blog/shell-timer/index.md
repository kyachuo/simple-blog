---
title: シェルスクリプトでカウントダウンタイマーを作成
date: "2023-08-06 22:00"
description: "勉強の時に使えるタイマーをシェルスクリプトの勉強と実用から作成しました。ターミナル上でカウントダウンを表示するタイマーです。タイマーを作るためのメモです"
---

勉強の時にタイマーを使いたいけれど、タイマーのアプリがOSになかったり、探すのがめんどくさいので、また、シェルスクリプトの勉強のためにも、実用的な自分の需要を満たすためにも、今回ターミナル上で実行してカウントダウンを表示するアプリを作成しました。今後も改良していくつもりですが、とりあえず基本として簡易的なものを作りました。と言ってもググって調べて作ったものです。

## 数字をカウントダウンするタイマー

方法は色々ある様ですが、シンプルで自分が理解しやすかったことと、古いOSでも動作した方法ということで下記を採用しました。

sleepというコマンドとfor文を使います。sleepは引数に数字を渡すと、その数字の秒数分、何もしないという動作をします。

```bash
sleep 1 //1秒待つ
```

sleepコマンドとfor文による数字の表示を組み合わせることで、1を表示し、1秒待ち、2を表示し、1秒待ち、...、ということを繰り返すことで、ターミナルに数字のカウントアップまたはカウントダウンを表示させることができます。

ターミナルに下記のように１行で書きます。

```bash
//1秒ごとに1から10までのカウントアップをターミナルに表示
for i in {1..10};do echo "${i}";sleep 1; done;

//1秒ごとに10から1までのカウントダウンをターミナルに表示
for i in {10..1};do echo "${i}";sleep 1; done;
```

上記の{10..1}の数字を変更することが、カウントダウンの秒数を変えることになります。  
例えば10分にしたいなら、10x60=600秒の600に変えます。({600..1})

## 作成したカウントダウンタイマーを実行する方法

そのままターミナルに例のように入力し、次回以降使うときはhistoryコマンドで入力したコマンドの履歴を確認し、コマンドの履歴から実行する方法と、シェルスクリプトのファイルを作成し、ファイルにコマンドを保存しておき、ファイルを実行することで実行する。

今回は勉強のためにも、継続して使える様にするためにも、ファイルを作成してみます。

### シェルスクリプトのファイルを作成する方法

任意のフォルダにシェルスクリプトのファイルを作成し、vimでファイルの中身を記載し保存します。  
そしてファイルに実行権限を追加すると実行できる様になります。

```bash
vim countdown-timer.sh

//シェルスクリプトファイルの中身
#!/bin/bash
for i in {600..1}
do
    echo "${i}"
    sleep 1
done
```

```bash
//ファイルの実行権限を付与して実行
chmod +x countdown-timer.sh
./countdown-timer.sh

```
