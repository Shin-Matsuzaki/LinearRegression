# 機械学習
- 説明変数：予測に使えるデータ
- 目的変数：予測対象<br>
単回帰とは，説明変数(x)→予測対象(y)の予測<br>

- 損失："駄目さ度合い"を定義<br>
y = ax + b<br>
という数理モデルを定義するとき，未知変数は a と b <br>
未知変数を求めるために，基準(損失関数)が必要<br>
　ex)最小二乗法では，二乗和誤差の最小化によって最適化
- 汎化性能<br>
未知のデータをどれだけ正しく予測できるか？
    1. 良し悪しの基準(評価指標 Metrics)
        - MSE
        - MAE
        - 決定係数(寄与率)
    2. どうやって測るか(評価プロトコル)
- ホールドアウト<br>
データをTrainingDataとTestData(とValidationData)に分けて学習と評価を行う

# 回帰問題
### 線形回帰
1. 単回帰：y = w<sub>0</sub> + w<sub>1</sub>x
1. 重回帰：y = w<sub>0</sub> + w<sub>1</sub>x<sub>1</sub> + w<sub>2</sub>x<sub>2</sub> + …
1. 多項式回帰：y = w<sub>0</sub> + w<sub>1</sub>x + w<sub>2</sub>x<sup>2</sup> + … + w<sub>M</sub>x<sup>M</sup>

下のモデルほど表現力(複雑度)が高い<br>
しかし，高ければ高いほどよいわけではなく，トレーニングデータにフィットしすぎない方がよい<br>
- 過学習：学習のしすぎ，モデルが複雑すぎて汎化性能が失われる．対策としては，データ増やす，正則化(複雑度下げる)