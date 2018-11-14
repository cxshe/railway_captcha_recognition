# railway_captcha_recognition 
# 基於CNN+RNN模型的台鐵驗證碼辨識

## ㄧ、前言
由於台鐵驗證碼的字數並不固定，可能是5或6碼。
先前的方法大都是做多個模型，先用一個模型判斷是5或6碼，再選用該字數的模型進行預測。
這種方法雖然能夠表現的很好，但仍有以下缺點：
1. 資料需求較大，因為5、6碼的模型需用不同的資料訓練
2. 前個模型預測的準確率會影響之後的模型
3. 多個模型的訓練及預測時間可能較長

## 二、方法
本專案使用一個CNN+RNN模型進行預測，取代先前多個模型的方法，詳細的訓練過程見training.ipynb

## 三、測試
在台鐵網頁上實測1000張驗證碼，準確率99.1%(991/1000)，詳細的測試結果見online_test.ipynb

## 四、參考資料
本專案學習自:實作基於CNN的台鐵訂票驗證碼辨識以及透過模仿及資料增強的訓練集產生器 
(https://github.com/JasonLiTW/simple-railway-captcha-solver)
