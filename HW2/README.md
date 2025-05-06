Colab : https://colab.research.google.com/drive/15OoCqV0bx5OnDRM8tmVwQ7IEFnnI5SIY?usp=sharing

# HW2
## 以下為設計神經網路到訓練的步驟
1. 讀入套件 gradio

2. 讀入 MNIST 數據庫

3. 設計五層神經網路
   - 每層都使用relu激活函數
   - N1 = 512
   - N2 = 256
   - N3 = 128
   - N4 = 64
   - N5 = 32
   - 最後為固定為10的輸出

4. 打印並檢視神經網路
![image](https://github.com/user-attachments/assets/5c15294b-f1ee-40dd-b412-7765a7e5c725)


5. 訓練神經網路 (batch size = 100, epochs=10 批次100筆, 訓練10次)
   - 測試資料loss: 0.00952476542443037
   - 測試資料正確率 0.9387000203132629

6. 用 Gradio 做測試
