<!-- ELUCENIA technical documentation · indice-de-baux-revisado · ja · no clinical/professional/rights approval -->

# 改訂Baux指数

[条件・出典・許諾](https://elucenia.org/ja/tools/indice-de-baux-revisado)

## 使い方

ポータルでツールを使用するか、ローカルHTTPサーバー経由でindex.htmlを開いてください。言語を選択し、項目を入力して計算してください。

## 入力項目と単位

### 年齢

`idade`

年 · 範囲: 0–110

### 熱傷体表面積

`scq`

% · 範囲: 0–100

### 吸入損傷がありますか？

`inalacao`

- `0` — いいえ
- `1` — はい

## 方法の版

改訂Baux/Osler 2010：年齢+面積+17吸入損傷；原ロジスティックモデル

## 記載された計算式

改訂Baux = 年齢（歳）+熱傷面積（%）+17×吸入損傷（1=あり、0=なし）。

Oslerモデル（米国登録39888例）では年齢と面積の重みはほぼ同じで、吸入損傷は17歳または面積17%に相当。死亡確率はスコアのロジスティック変換で求めます。

## 限界・対象集団

改訂Bauxは、年齢、熱傷面積の百分率、吸入損傷がある場合の17を合計します。生の合計は死亡率の百分率ではなく、確率にはその版のロジスティック変換が必要です。論文では簡略モデルはより複雑なモデルより性能が低く、適切な臨床集団で解釈する必要があります。

## 参考文献

- [Osler T, Glance LG, Hosmer DW. Simplified estimates of the probability of death after burn injuries: extending and updating the Baux score. J Trauma, 2010.](https://doi.org/10.1097/TA.0b013e3181c453b3)

- [Dokter J et al. External validation of the revised Baux score for the prediction of mortality in patients with acute burn injury. J Trauma Acute Care Surg, 2014.](https://doi.org/10.1097/TA.0000000000000124)

## 技術テストの再現

このリポジトリのルートディレクトリでnode test.cjsを実行すると、記録された合成ケースを再実行できます。元の入力、期待結果、許容誤差は保持されています。技術テストは臨床的検証を意味しません。

```sh
node test.cjs
```

tool.jsonには出典、版、確認範囲が記録されています。examples.jsonには合成入力と期待結果が保持され、results.jsonには実際に得られた結果が記録されています。

[記録・参考文献](../tool.json) · [JavaScriptコード](../calculator.js) · [参照ケース](../examples.json) · [results.json](../results.json)

## 確認状況と使用条件

独立した臨床レビューは実施されていません。

このインターフェースは独自に作成した翻訳であり、公式版や認証済みの版ではありません。独立した臨床レビュー、専門家による言語レビュー、評価尺度等の権利許諾の確認は実施されていません。

式または分類の結果です。解釈、対応、適用可能性は専門家による評価と選択した出典に依存します。

## ライセンスと帰属表示

Apache-2.0はELUCENIAのコードにのみ適用されます。評価尺度等、出版物、翻訳、データの権利は、それぞれの権利者に帰属します。LICENSEとNOTICEを保持してください。

ELUCENIA · Felipe Guedes · Copyright © 2026
