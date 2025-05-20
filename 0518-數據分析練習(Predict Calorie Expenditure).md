【步驟一：建立新的 Kaggle Notebook】
登入 Kaggle 帳戶。
前往比賽頁面：Predict Calorie Expenditure
點擊「Code」標籤。
點擊「New Notebook」，建立一個新的 Notebook。Kaggle+1Reddit+1

【步驟二：撰寫基本的資料處理與模型訓練程式碼】
在新的 Notebook 中，您可以依序執行以下程式碼區塊：
1. 匯入必要的套件
python
複製編輯
import pandas as pd
from sklearn.linear_model import LinearRegression

2. 讀取資料
python
複製編輯
train = pd.read_csv('/kaggle/input/playground-series-s5e5/train.csv')
test = pd.read_csv('/kaggle/input/playground-series-s5e5/test.csv')

3. 檢視資料
python
複製編輯
print(train.head())
print(train.info())

4. 定義特徵與目標變數
python
複製編輯
X = train.drop(['id', 'Calories_Burned'], axis=1)   -要修改成正確名稱
y = train['Calories_Burned']                 -要修改成正確名稱
X = train.drop(['id', 'Calories'], axis=1)   -正確名稱–
y = train['Calories']		                  -正確名稱–

5. 訓練模型
python
複製編輯
model = LinearRegression()
model.fit(X, y)

6. 預測測試集
python
複製編輯
X_test = test.drop('id', axis=1)
predictions = model.predict(X_test)

7. 建立提交檔案
python
複製編輯
submission = pd.DataFrame({'id': test['id'], 'Calories_Burned': predictions})
submission.to_csv('submission.csv', index=False)

