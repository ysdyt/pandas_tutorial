# データ分析で頻出のPandas基本操作

機械学習や深層学習が人気の昨今ですが、それらのモデルの精度に最もクリティカルに影響するのはインプットするデータの質です。データの質は、データを適切に把握し、不要なデータを取り除いたり、必要なデータを精査する前処理を行うことで担保することが出来ます。

本頁では、データ処理の基本ツールとしてPandasの使い方を紹介します。Pandasには便利な機能がたくさんありますが、特に分析業務で頻出のPandas関数・メソッドを重点的に取り上げました。

また、単に機能を説明するだけでは実際の処理動作がわかりにくいため、ここではSIGNATE(旧DeepAnalytics)のお弁当の需要予想を行うコンペのデータを拝借し、このデータに対して一貫してPandasの処理を適応していくことで、一連のPandas操作（前処理のプロセス）を体験してもらいます。

![pandas](./figs/pandas.jpg)

## 本頁で紹介するPandasメソッド一覧

**① Pythonのバージョン確認、モジュールのimport、データの読み込み**

- pd.read_csv()
- df.head()
- df.tail()

**② 簡単にデータの状態を確認する（行数列数カウント・データの選択的表示・重複の有無など）**

- df.shape()
- df.index
- df.columns
- df.dtypes
- df.loc[]
- df.iloc[]
- df.query()
- df.unique()
- df.drop_duplicates()
- df.describe()

**③ データの整形（データ型変更、列名変更、並び替えなど）**

- df.set_index()
- df.rename()
- df.sort_values()
- df.to_datetime()
- df.sort_index()
- df.resample()
- df.apply()
- pd.cut()

**④ データの欠損状態の確認** 

- df.isnull()
- df.any()

**⑤ 値（欠損）の置き換えや削除**

- df.fillna()
- df.dropna()
- df.replace()
- df.mask()
- df.drop()

**⑥ 集計**

- df.value_counts()
- df.groupby()
- df.diff()
- df.rolling()
- df.pct_change()

**⑦ 可視化**

- df.plot()
- df.corr()
- df.pivot()

**⑧ 変数の前処理**

- pd.get_dummies()

**⑨ 最後に、出来たデータをもう一度眺める**

- df.to_csv()