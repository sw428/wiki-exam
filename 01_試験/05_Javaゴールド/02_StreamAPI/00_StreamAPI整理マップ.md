# StreamAPI整理マップ

## 目的

Stream API を、中間操作、終端操作、遅延評価、戻り値で判断できる形に整理します。

## 問題で見る手がかり

- `filter` / `map` / `flatMap`
- `sorted` / `distinct` / `limit`
- `forEach` / `collect` / `reduce` / `count`
- 中間操作と終端操作
- 遅延評価
- Optional

## まず切る選択肢

- 中間操作だけで実行されると思っている選択肢
- 戻り値の型を取り違えている選択肢
- `map` と `flatMap` を混同している選択肢
- 終端操作後に同じStreamを再利用しているコード

## 似たAPIとの住み分け

- `filter` は残すか捨てるか
- `map` は1要素を別の1要素へ変換
- `flatMap` は入れ子を平らにする
- `collect` は集める
- `reduce` は畳み込む

## 認知アプローチ

Stream問題では、操作名を読む前に「中間か終端か」を見ます。次に、戻り値の型と、いつ実行されるかを追います。

## 次に見るリンク

- [Javaゴールド整理マップ](../00_Javaゴールド整理マップ.md)
