# Qiita_multi-colinearlity
シミュレーション設定

データ：X1とX2に相関がある場合を考える。

- 使用するモデル：
    1. 全ての説明変数を使う
    2. x2を使わない
    3. 合算値を使う（x1+x2を使う） 
    4. PCR（主成分回帰）
    5. PLS（部分的最小二乗回帰）
    6. Ridge回帰
    7. Lasso回帰

それぞれ下記3つを調べる。
    1. 相関係数ごとの回帰係数の分散（各1,000回推定の分散）
    2. 相関係数ごとの回帰係数の平均（各1,000回推定の平均）
    3. 回帰係数に関するMSE（真の値に対する各1,000回推定の平均）
    4. 目的変数に関するMSE（未知データに対するに対する1,000回推定の平均）
    5. 相関係数が大きいとき（0.9のとき）にサンプルサイズを増やすと推定値はどうなるか（最大サンプルサイズ50,000）