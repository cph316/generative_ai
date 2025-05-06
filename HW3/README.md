Colab : https://colab.research.google.com/drive/1pVaHl4AwRblE3AX7inQo-sqIbgdClLIr?usp=sharing

# 主題二

1.說明 Cross Entropy 與 KL Divergence

Cross Entropy 和 KL Divergence 主要是用來衡量兩個機率分佈的差異。在 GAN中，這兩個概念很重要，因為生成器要學習讓它的分佈𝑄盡可能接近真實數據分佈𝑃，而判別器則在幫助區分。

2.公式與計算

(1) Cross Entropy

H(P,Q)=−i∑iP(xi)logQ(xi) 

其中：

P(xi)  是真實分佈（通常是 one-hot 標籤）。

Q(xi)  是模型預測的機率分佈。

這代表「當我們使用𝑄來表達𝑃的時候，平均需要多少 bits 來表示這個系統的資訊？」

(2) KL Divergence

DKL(P∥Q)=∑iP(xi)logP(xi)/​logQ(xi) 

這代表「當我們用𝑄來代替𝑃，會額外產生多少錯誤資訊？」

(3) 兩者關係  H(P,Q)=H(P)+DKL(P∥Q) 

-如果𝑄和𝑃完全相同，那麼 KL 散度為 0，交叉熵等於熵。 -但如果𝑄與𝑃差異很大，KL 散度會變大，交叉熵也會變大。


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
