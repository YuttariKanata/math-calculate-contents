# Decimal Expansion of the Maraldi Angle

このファイルは、**マラルディの角度 (Maraldi angle)** の十進展開に関する計算結果の参照用ドキュメントです。

## 1. データの概要

- **定義:** $\theta = \arccos\left(\frac{1}{3}\right) \approx 70.528779^\circ$
- **精度:** [ここに計算した桁数、またはbit数を記入] 桁
- **ファイルサイズ:** 154.1 MB
- **形式:** UTF-8 プレーンテキスト (.txt)

## 2. 数学的背景

マラルディの角度は、菱形十二面体の二面角であり、ハニカム構造（蜜蜂の巣）の底面を構成する菱形の角度として知られています。また、石鹸膜の接合角（プラトーの法則）など、自然界の最適化構造において重要な役割を果たす定数です。

## 3. データへのアクセス

ファイルサイズが100MBを超えているため、外部ストレージ（Google Drive）にホストしています。

- **[Download Result (Google Drive)](https://drive.google.com/file/d/1b6-ncrMT2QwTS_ICcd0vykmtFLrH7zl7/view?usp=drive_link)**

> [!NOTE]
> テキストファイルとして保存されています。非常に長大な桁数のため、閲覧には `less` や巨大ファイル対応のテキストエディタを推奨します。

## 4. 計算環境

- **言語:** Julia 1.10.x
- **アルゴリズム:** 逆三角関数の高精度計算 (MPFR `acos` 関数を使用)
- **計算コード:**

```julia
using BigFloat
setprecision([設定した精度])
theta = acos(BigFloat(1)/3)
# 度数法への変換が必要な場合はさらに計算
```

-----

[Return to Repository Top](https://github.com/YuttariKanata/math-calculate-contents)
