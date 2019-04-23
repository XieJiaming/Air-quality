# Air-quality

本次主要分析UCI air quality https://archive.ics.uci.edu/ml/datasets/Air+Quality

而此次主要目的為預測第9238~第9357筆的NO2含量

此分析主要架構與流程:
# 1.  確認資料型態與資料內容。
1. 確定資料型態與類別
2. 內容格式錯誤，例如'1,1'應該改為'1.1'
3. NA是否存在
4. ""(empty)是否存在
5. 新增hour、weekdays、month、year、day變數
6. 對於各變數存在-200的期數做分析
7. 以auto.arima()所算得的p期來填補-200
# 2. EDA
1. 各變數的分布
2. 各變數在不同hour、weekdays、month的變化
3. 相關性

# 3. 定義空氣品質
# 4. 模型
1. base model (linear model)
2. lag model(linear model with previous NO2 information)
3. James-Stein model
# 5. Test set accuracy
