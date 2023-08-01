---
title: コンピューターグラフィックス技法まとめ | 応用情報午前対策
date: "2023-07-30"
description: "応用情報の午前問題でたまに出題されるコンピュータグラフィックス技法についての問題が苦手なので自分なりに技法をまとめてみました。"
---

コンピュータグラフィックス技法の用語と処理内容のイメージがなかなかイメージしづらいのもあって、用語と処理内容が覚えられない。勉強してもすぐ忘れてしまう。また、出てきた用語を行き当たりばったりに覚えようとするような感じで、体系的に整理できていないので自分用のメモとしてまとめてみました。現時点での内容なので、継続的に内容を追加修正します。

## テクスチャマッピング

ポリゴンと呼ばれる多数の多角形状で表された物体の表面に画像を貼り付けることで、ポリゴンの質感を高める技法のこと。テクスチャーは質感という意味なので、用語からイメージはしやすいので確実に覚えておく。

[テクスチャマッピングについてのわかりやすい記事](https://www.oit.ac.jp/is/L231/pukiwiki/?%E6%84%9F%E8%A6%9A%E3%83%A1%E3%83%87%E3%82%A3%E3%82%A2%E7%A0%94%E7%A9%B6%E5%AE%A4/OpenGL/%E3%83%86%E3%82%AF%E3%82%B9%E3%83%81%E3%83%A3%E3%83%9E%E3%83%83%E3%83%94%E3%83%B3%E3%82%B0)を参照する。

<br />

## メタボール

メタボールは、物体を球や楕円体の集合として表現することで滑らかな物体を表現する技術。用語と意味が覚えやすいのでこれも確実に覚えておく。blenderで出てくる。

<br />

## レイトレーシング

レイトレーシングは、3DCGを作成する時に必要となる陰影をつけるときに使われる手法。観察者(物体を見ている目)から光源の経路を逆に追跡し、算術演算をして陰影をつけるのに必要な物体表面の輝度を求める手法。

ray tracingの略で、日本語に訳すと光線追跡法。

レイトレーシングの前はラスタライズ法というレンダリング手法が主流だった。

[レイトレーシングやラスタライズ法についての記事](https://www.dospara.co.jp/5info/cts_str_parts_raytracing.html#:~:text=%E3%83%AC%E3%82%A4%E3%83%88%E3%83%AC%E3%83%BC%E3%82%B7%E3%83%B3%E3%82%B0%E3%81%AF%E3%80%81%E5%85%89%E3%81%AE,%E4%BD%9C%E3%82%8A%E5%87%BA%E3%81%99%E3%81%93%E3%81%A8%E3%81%8C%E3%81%A7%E3%81%8D%E3%81%BE%E3%81%99%E3%80%82)を参照する。

<br />

## レイキャスティング

レイトレーシングと用語の響きが似ているので混同に注意する。レイトレーシングよりも古くからある技術という位置関係を覚えておく。一つの光線を飛ばして物体に当たった具合で視点と物体との距離を計算して、距離に応じた描画をする。反射、透過方向への視線追跡は行わない。

[レイキャスティングについての記事](https://ja.scratch-wiki.info/wiki/%E3%83%AC%E3%82%A4%E3%82%AD%E3%83%A3%E3%82%B9%E3%83%86%E3%82%A3%E3%83%B3%E3%82%B0#:~:text=%E3%83%AC%E3%82%A4%E3%82%AD%E3%83%A3%E3%82%B9%E3%83%86%E3%82%A3%E3%83%B3%E3%82%B0%E3%81%AF%E3%80%81%E8%A6%96%E7%82%B9%E3%81%8B%E3%82%89,%E3%81%99%E3%82%8B%E6%96%B9%E6%B3%95%E3%81%8C%E5%8F%96%E3%82%89%E3%82%8C%E3%82%8B%E3%80%82)を参照する。

<br />

## ラジオシティ

ラジオシティは、各ポリゴンに光のエネルギー量を持たせて形状の相互反射を計算し間接光などを表現する技術。物体に反射して生じる間接光を表現できる。照明工学の分野で発達した技術を3DCGのレンダリングに応用したもの。拡散反射面間の相互反射による効果を考慮して拡散反射面の輝度を決める。


