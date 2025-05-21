# 數據分析(Data Analysis)
一、分析流程面:
底下又分不同階段與不同深度。
1. 資料收集(Data Collection)
    ->抓API、爬蟲、上傳CSV、連接資料庫等等。
2. 資料清理與前處理(Data Cleaning & Preprocessing)
    ->處理缺失值、格式轉換、欄位重整。
3. 探索性資料分析(Exploratory Data Analysis,EDA)
    ->視覺化、統計摘要、初步假設、了解資料分布。
4. 資料建模與進階分析(Modeling & Advanced Analytics)
    ->機器學習模型、時間序列、分群等。
5. 視覺話與報告呈現(Visualization & Communication)
    ->Tableau、Power BI、報表匯出、Dashboard。
6. 決策應用與部屬(Deployment & Action)
    ->商業決策、智慧製造、推薦系統等。
    
二、分析技術面:
根據分析的「深度與複雜度」來分類。

先以常見順序排列:


| 分析類型     | 說明                                     | 常用方法                         | 工具/技術     |
| ---------- | ---------------------------------------- | ------------------------------ | ------------ |
| **描述性分析** | 告訴你「發生了甚麼」                   | EDA、平均值、標準差              | Excel、Pandas         |
| **診斷性分析** | 解釋「為什麼會這樣」                   | t檢定、交叉驗證、相關係數        | R、SQL                 |
| **預測性分析** | 預測「接下來會發生甚麼」               | 線性回歸、XGBoost、LSTM          | Python ML工具         |
| **規範性分析** | 建議「該做甚麼決策」                   | 最佳化模型、模擬、強化學習       | AI模型、自動化引擎        |
| **大數據分析** | 解決「資料量過大」、「來源多樣」的問題 | 分散式處理、漏斗分析、用戶行為流 |Hadoop、Spark、FineBI        |

以技術深度來排序:

| 分層  | 說明   | 常見工作職位 | 對應方法 | 常用工具 |
| ---- | ------ | --------- | ------- |------- |
| **第 1 層：基礎分析層（統計 + EDA）**   | 資料整裡 + 基本統計 + 視覺化，用來「了解資料」| 行銷分析師、商業分析師、初階資料分析師| EDA、平均數、標準差、分組、交叉分析、趨勢圖、直方圖、箱型圖 | Excel、Pandas、Power BI、Tableau|
| **第 2 層：進階分析層（預測 + 分群 + 機器學習）**| 利用數學模型找出潛在規律或預測未來，資料科學/AI起點  | 資料科學家、AI助理工程師、預測工程師| 線性回歸、分類、聚類、決策樹、時間序列分析| Python（scikit-learn、XGBoost、statsmodels）、R|
| **第 3 層：大數據與決策應用層（系統 + 大規模處理 + 自動化）** | 結合多資料源、即時分析、自動化部署與高複雜度商業應用 | 數據架構師、大數據工程師、數據決策分析師、IIoT分析顧問 | 漏斗分析、用戶路徑分析、即時監控、數據湖整合、強化學習 | Spark、Hadoop、Kafka、Airflow、FineBI、Power BI 自動化串接、Tableau server |


一、探索性資料分析(EDA，Exploratory Data Analysis)
二、資料視覺化(Data Visualization)
三、統計檢定(Statistical Testing)
四、機器學習與建模(Predictive Modeling)
五、資料前處理
六、時間序列分析
七、績效評估與報告

一、探索性資料分析(EDA，Exploratory Data Analysis)
了解資料的結構、特徵與潛在問題。
    1.敘述統計(Descriptive Statistics)
    * 平均數、中位數、標準差、最小值、最大值。     
    2.分布檢視(Distribution Analysis)
    * 直方圖、箱型圖(boxplot)、密度圖等觀察變數分布。
    3.缺失值與異常值檢查
    * 檢查是否有缺失值(NaN)、離群值(Outlier)。
    4.資料關聯性(Correlation Analysis)
    * 計算變數間的相關係數(如Pearson)。
    
二、資料視覺化(Data Visualization)
以圖像化的方式呈現資料趨勢與關係。
    *折線圖(Line Plot)、長條圖(Bar Chart)、圓餅圖(Pie Chart)。
    *熱力圖(Heatmap)用來觀察相關性矩陣。
    *散點圖(Scatter Plot)檢視兩變數關係。
    
    工具:matplotlib、Seaborn、Plotly、Tableau。

三、統計檢定(Statistical Testing)
驗證假設、比較不同群體的差異。

| 方法      | 用途      |
| -------- | -------- |
| t-test   | 比較兩組平均值是否有顯著差異|
| ANOVA    | 比較多組平均值差異        |
| 卡方檢定(Chi-Square Test)| 檢查分類變數間是否獨立     |
| 常態性檢定(Shapiro-Wilk、Kolmogorov-Smirnov)| 檢查資料是否服從常態分布|

四、機器學習與建模(Predictive Modeling)
建立預測模型、分群或分類。


| 分類(Classification) | 回歸(Regression) | 分群(Clustering) |
| -------- | -------- | -------- |
| 決策樹(Decision Tree)| 線性回歸(Linear Regression)| K-means|
| 隨機森林(Random Forest)| 多項式回歸(polynomial Regression)| 層次式分群(Hierarchical Clustering)|
| 支持向量機(SVM)|Lasso/Ridge Regression| DBSCAN|
| 邏輯回歸(Logistic Regression)| XGBoost/LightGBM| |
| 神經網路(Neurel Network)|      | |

五、資料前處理
提升模型效能，處理不完整或不乾淨的資料。
常見:
* 缺失值填補(補0、平均數、中位數、預測)
* 標準化與正規化(Standardization/Normalization)
* 類別型資料編碼(Label Encoding,One-hot Encoding)
* 特徵工程(Feature Engineering)

六、時間序列分析
針對時間性資料進行趨勢預測。
常見:
* 移動平均(Moving Average)
* 指數平滑法(Exponential Smoothing)
* ARIMA/SARIMA模型
* Prophat(Meta提供的時間序列工具)
    
七、績效評估與報告
衡量分析或模型的效果，產出報告支援決策。
指標:
* 準確率(Accuracy)、精確率(Precision)、召回率(Recall)
* MSE、RMSE、MAE(回歸誤差指標)
* 混沌矩陣(Confusion Matrix)
* A/B測試結果分析