
# WARP

Form [2020-SAC-WARP: Revisiting GFN for Lightweight 128-Bit Block Cipher](https://link.springer.com/chapter/10.1007/978-3-030-81652-0_21)

* 分组长度: 128 bits
* 密钥长度: 128 bits
* 加密轮数: 40 + 一层 Sbox (无线性层)



<img width="1300" height="236" alt="image" src="https://github.com/user-attachments/assets/c27cae96-9b6d-41d4-a49f-3077a80f4500" />



如上图所示, 128-bit 分组被分成 32-branch Generalized Feistel Network, 初始状态被分为 32 个 nibbles. 即, $X^{r}=X_0^r \parallel X_1^r \parallel ... \parallel X_{31}^r$ .

轮密钥只加在一半的状态上 (Feistel 结构的特点), 所以 128-bit 密钥被分为两组, 各 64 btis, $K=K_0||K_1$, 第 $r$ 轮的密钥记为 $RK^r=K^{(r-1) \mod 2}$.



WARP 的 Sbox:



<img width="1058" height="135" alt="image" src="https://github.com/user-attachments/assets/d5c701b0-85c4-48fd-9933-c343fc9e95bb" />



WARP 的 线性层置换 $\pi$:


<img src="https://github.com/user-attachments/assets/6f725d63-97f9-44f1-bb97-fca91705c19c" style="zoom:10%;" />



## 算法特点:


## 应用场景:


## 最新分析结果:


