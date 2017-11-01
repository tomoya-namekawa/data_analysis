# データ分析関連メモ

## モデル
- 線形回帰
    - 重回帰分析
- 時系列モデル
    - ARIMAモデル
        - ARMAモデル（ARモデルとMRモデルを組み合わせた）で、差分で分析できるようにしたもの
    - SARIMAモデル(seasonal ARIMA model)
        - ARIMAモデルに季節性を足したもの
    - ARCHモデル
        - ARモデルの発展
        - 分散が一定ではない（分散の不均一性）対象に適応
        - 下記のGARCHモデルのほうが有能
    - GARCHモデル
        - ARCHモデルの発展
- 状態空間モデル
    - ローカルレベルモデル
- ベイズ
- ホルトウインターズ
- Bassモデル
- ログログインバース曲線
- 成長曲線：ゴンペルツ１次式
- ベイジアン･コンセンサス
- 予測値合成法
- 最近隣（ＮＮ）モデル
- https://www.slideshare.net/berobero11/ss-29409382


## ハイパーパラメータの決め方
- グリッドサーチ
- ベイズ最適化(Bayesian Optimization)
- ランダムサーチ

## 用語
- 時系列分析関連
    - 和分過程(単位根過程)
        - ARIMA過程のうち、特に元の時系列ytytが非定常過程である一方で差分系列Δyt=yt−yt−1Δyt=yt−yt−1が定常過程である時、これを単位根過程（もしくは和分過程）と呼びます。
        - http://tjo.hatenablog.com/entry/2013/04/23/190417
        - [経済・ファイナンスデータの計量時系列分析 (統計ライブラリー)](https://www.amazon.co.jp/exec/obidos/ASIN/4254127928/hatena-blog-22/) 
    - 共和分
    - [時系列分析用語まとめ](https://upo-net.ouj.ac.jp/tokei/contents/sub_contents/c01_06_00.xml)
    - 状態空間モデル
    - カルマンフィルタ
    - カレンダー効果(calendar effect)
    - Ljung-Box test
        - 時系列データの自己相関があるかの検定（残差がホワイトノイズか調べるために使う）

## pythonライブラリ
- jupyter
- math
- numpy
- pandas
    - [pandas.DataFrame.plot](https://pandas.pydata.org/pandas-docs/stable/generated/pandas.DataFrame.plot.html)
    - [pandas.DataFrame.loc](https://pandas.pydata.org/pandas-docs/stable/generated/pandas.DataFrame.loc.html)
- matplotlib
- seaborn
- statsmodels
    - [statsmodels.tsa.statespace.sarimax.SARIMAX](http://www.statsmodels.org/dev/generated/statsmodels.tsa.statespace.sarimax.SARIMAX.html)
        - seasonal ARIMAモデル
    - [statsmodels.tsa.statespace.structural.UnobservedComponents](http://www.statsmodels.org/dev/generated/statsmodels.tsa.statespace.structural.UnobservedComponents.html)
        - 状態空間モデル
    - [statsmodels.tsa.statespace.structural.UnobservedComponents.fit](http://www.statsmodels.org/stable/generated/statsmodels.tsa.statespace.structural.UnobservedComponents.fit.html#statsmodels.tsa.statespace.structural.UnobservedComponents.fit)

- orange
- scipy
- simpy

## 検定
- t test
- F test
- Ljung-Box test
    - 帰無仮説は「残差に系列相関無し」
    - 時系列データの自己相関
- Jarque-Bera test(Bowman-Shenton test)
    - 帰無仮説は「分布が正規分布である」
    - 標本データが正規分布に従う尖度と歪度を有しているかどうかを調べる適合度検定
- [Heteroskedasticity test](http://www.statisticshowto.com/heteroscedasticity-simple-definition-examples/)
    - 分散不均一性の検定
- クラスカル・ウォリス検定
- マンホイットニのＵ検定

## リンク
- 検定
    - [Statistics How To](http://www.statisticshowto.com/probability-and-statistics/statistics-definitions/)
    - [NIST](https://www.nist.gov/itl/sed)
- 時系列分析
    - ARIMAモデル関連
        - [さくっとトレンド抽出: Pythonのstatsmodelsで時系列分析入門](http://data.gunosy.io/entry/statsmodel_trend)
        - [見せかけの回帰について（そして単位根過程・共和分など）](http://tjo.hatenablog.com/entry/2013/04/23/190417)
        - [季節調整済みARIMAモデルで電力使用状況を推定してみる](http://jbclub.xii.jp/?p=695)
            - SARIMAモデルを使ってる
        - [Seasonal ARIMA with Python](http://www.seanabu.com/2016/03/22/time-series-seasonal-ARIMA-model-in-python/)
        - [【 Python 時系列解析 】Yahoo Finance から FTSEロンドン株価データ を 取得して、経済時系列解析 の 作業手順 を通しで行ってみる 〜 データの定常性検定 から（G）ARCHモデル推定 まで](https://qiita.com/HirofumiYashima/items/a5d92607bedf3d58944d)
        - [時系列分析用語まとめ](https://upo-net.ouj.ac.jp/tokei/contents/sub_contents/c01_06_00.xml)
        - [STAT 510 Seasonal ARIMA models](https://onlinecourses.science.psu.edu/stat510/node/67)
            - 時系列分析の解説。Seasonal ARIMAのパラメータについて詳しく書いてある
    - 状態空間モデル
        - [Pythonで状態空間モデルを使う（StatsModels）](http://www.hirotsuru.com/entry/2017/08/13/232311)
        - [Pythonによる状態空間モデル](https://logics-of-blue.com/python-state-space-models/)
        - [時系列データ分析とPython](http://www.hirotsuru.com/entry/2017/07/02/230437)
- 機械学習
