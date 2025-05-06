Colab : https://colab.research.google.com/drive/1pVaHl4AwRblE3AX7inQo-sqIbgdClLIr?usp=sharing

# 主題二

1.說明 Cross Entropy 與 KL Divergence

2.公式與計算

3.硬幣範例

- (1)公式建立
- (2)Python 程式
![image](https://github.com/user-attachments/assets/41be45cd-9efc-4478-bb90-334750d02191)
- (3)執行結果
 交叉熵（0.5919）：代表模型預測的機率分佈與真實標籤的誤差，如果𝑄越接近𝑃，交叉熵就會越 小。
 KL 散度（0.0915）：表示預測分佈與真實分佈的距離，數值越小代表模型學得越好。

## **結論**

以上範例可以更直觀理解：
- 交叉熵 用於訓練模型，幫助它學習接近真實分佈。
- KL 散度 是衡量兩個機率分佈之間的距離，數值越大代表模型預測越不準確。
  
這也與 GAN 的生成器訓練 有關，因為生成器希望讓 𝑄盡可能接近𝑃，這樣判別器就無法分辨真假數據，從而達到更好的生成效果
