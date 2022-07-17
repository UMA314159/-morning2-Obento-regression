# タイトル
SIGNATE 
https://signate.jp/competitions/102

# 概要



# データ概要
課題種別：分類
データ種別：多変量
学習データサンプル数：445
説明変数の数：7
欠損値：あり


# ①モデル作成：LogisticRegression
- モデル：ロジスティック回帰：ハイパーパラメータ（設定なし）
- ライブラリ：Sklearn
- データ分割：holdout
- 目的関数：accuracy 

# その他
- 追加モデル：K近傍法、サポートベクターマシーン、ニューラルネットワーク、ランダムフォレスト、決定木、グラディエントブースティング
- 各モデルの検証を実施。サポートベクターマシーンは確率を算出できないため、確率予測タスクでは使用不可。

# ②モデル作成：GradientBoostingClassifier
- モデル：GradientBoostingClassifier
- ライブラリ：Sklearn,XGBoost
- データ分割：cross-validation
- 目的関数：accuracy
- ハイパーパラメータ： {'n_estimators':[100,200,300,400,500],'learning_rate':[0.01,0.03,0.06,0.09,0.12],'max_depth':[2,4,6,8]}

# ③モデル作成：ツリー系
- モデル：RandomForestClassifier,ExtraTreesClassifier,DecisionTreeClassifier
- ライブラリ：Sklearn
- データ分割：cross-validation
- 目的関数：accuracy
- ハイパーパラメータ： {'max_depth':[2,4,6,8,10],'max_features':[1,2,3,4,5],'n_estimators':[100,200,300,400,500]}