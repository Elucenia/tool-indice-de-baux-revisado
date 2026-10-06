<!-- ELUCENIA technical documentation · indice-de-baux-revisado · zh · no clinical/professional/rights approval -->

# 修订 Baux 指数

[条件、来源与许可](https://elucenia.org/zh/tools/indice-de-baux-revisado)

## 使用方法

在门户中使用工具，或通过本地 HTTP 服务器打开 index.html。选择语言，填写各字段，然后计算。

## 输入与单位

### 年龄

`idade`

年 · 范围: 0–110

### 烧伤体表面积

`scq`

% · 范围: 0–100

### 是否有吸入性损伤？

`inalacao`

- `0` — 否
- `1` — 是

## 方法版本

修订Baux/Osler 2010：年龄+面积+17吸入损伤；原logistic模型

## 已记录的公式

修订Baux = 年龄（岁）+烧伤面积（%）+17×吸入损伤（1=是，0=否）。

Osler模型（美国登记39888例烧伤）中，年龄与烧伤面积权重几乎相同，吸入损伤相当于17岁或17%面积。死亡概率由分数的logistic转换得到。

## 限制与适用人群

修订Baux将年龄、烧伤面积百分比及吸入性损伤时的17相加。原始总分不是死亡率百分比；概率需要该版本的logistic变换（逻辑斯蒂变换）。在文章中，简化模型的表现不及更复杂模型，需要在适当临床人群中解释。

## 参考文献

- [Osler T, Glance LG, Hosmer DW. Simplified estimates of the probability of death after burn injuries: extending and updating the Baux score. J Trauma, 2010.](https://doi.org/10.1097/TA.0b013e3181c453b3)

- [Dokter J et al. External validation of the revised Baux score for the prediction of mortality in patients with acute burn injury. J Trauma Acute Care Surg, 2014.](https://doi.org/10.1097/TA.0000000000000124)

## 复现技术测试

在此仓库的根目录中运行 node test.cjs，以重复已记录的合成案例。原始输入、预期结果和容差保持不变。技术测试不构成临床验证。

```sh
node test.cjs
```

tool.json 包含来源、版本和审查范围。examples.json 保留合成输入与预期结果；results.json 记录实际得到的结果。

[记录与参考文献](../tool.json) · [JavaScript代码](../calculator.js) · [参考案例](../examples.json) · [results.json](../results.json)

## 审查与使用条件

尚未开展独立临床审查。

此界面为自主编写的翻译，并非官方或认证版本。尚未完成独立临床审查、专业语言审查或工具权利授权。

公式或分类结果。解释、处理及适用性须结合专业评估和所选来源。

## 许可与署名

Apache-2.0 仅适用于 ELUCENIA 代码。工具、出版物、翻译和数据的权利仍归各自权利人所有。请保留 LICENSE 和 NOTICE。

ELUCENIA · Felipe Guedes · Copyright © 2026

## 已记录的结果

以下信息保留该方法对合成示例的输出，不构成独立的临床验证。

### 1

评分越高，预测死亡率越高；吸入性损伤相当于17年（或体表面积的17%）

| 结果详情 | |
| --- | --- |
| 经典Baux（年龄 + 体表面积） | 70 |
| 吸入性损伤 | +17 |

经典Baux评分是作为死亡率的%估计而创建的；在当前治疗下，这种读法会高估风险。


### 2

评分越高，预测死亡率越高；吸入性损伤相当于17年（或体表面积的17%）

| 结果详情 | |
| --- | --- |
| 经典Baux（年龄 + 体表面积） | 110 |
| 吸入性损伤 | 否 |

经典Baux评分是作为死亡率的%估计而创建的；在当前治疗下，这种读法会高估风险。


### 3

评分越高，预测死亡率越高；吸入性损伤相当于17年（或体表面积的17%）

| 结果详情 | |
| --- | --- |
| 经典Baux（年龄 + 体表面积） | 38 |
| 吸入性损伤 | 否 |

经典Baux评分是作为死亡率的%估计而创建的；在当前治疗下，这种读法会高估风险。

