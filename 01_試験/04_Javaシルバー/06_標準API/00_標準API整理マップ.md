# 標準API整理マップ

## 目的

Java Silver の標準APIを、破壊的変更、戻り値、比較、文字列処理の観点で整理します。

## 問題で見る手がかり

- `String` / `StringBuilder`
- 配列、`ArrayList`
- `equals` / `==`
- `length` / `length()` / `size()`
- 日付、ラッパークラス

## まず切る選択肢

- `String` が不変である点を見落とした出力
- `StringBuilder` が自身を変更する点を見落とした出力
- `==` と `equals` を混同している選択肢
- 配列、文字列、リストの長さ取得を混同しているコード

## 似たAPIとの住み分け

- 配列は `length`
- 文字列は `length()`
- `ArrayList` は `size()`
- `String` は不変
- `StringBuilder` は可変

## 認知アプローチ

API問題では、メソッド名よりも「元のオブジェクトが変わるか」「戻り値を受け取っているか」を見ます。

## 次に見るリンク

- [Javaシルバー整理マップ](../00_Javaシルバー整理マップ.md)
