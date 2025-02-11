# 3-1 (P.106)
平均二乗誤差による損失関数
$$
L = \frac{1}{2N}\sum_{s=1}^{N} (y_s-t_s)^2
$$

# 3-2 (P.110)
分類に対する損失関数（クロスエントロピー）
$$
L = \frac{1}{N}\sum_{s=1}^{N} (-t_s \log y_s - (1-t_s) \log (1-y_s))
$$

# 3-3 (P.114)
クロスエントロピーのイメージ(N=1の場合)

$$
L = -t_1 \log y_1 - (1-t_1) \log (1-y_1)
$$

# 3-4 (P.117)

$$
y_s = f(u_s)
$$

# 3-5 (P.117)

$$
u_s = \mathbf{w} \cdot \mathbf{x}_s + b
$$

# 3-6 (P.118)

$$
y = f(u) = e^u = exp(u)
$$

# 3-7 (P.118)

$$
u(x) = x^2
$$

# 3-8 (P.120)

$$
L = \frac{1}{4}(-\log(1-y_1) - \log(1-y_2) - \log(1-y_3) - \log y_4)
$$

# 3-9 (P.120)

$$
b = -0.75(w_1 + w_2)
$$

# 3-10 (P.125)

$$
w_1' = w_1 - \eta \frac{dL}{dw_1}
$$

# 3-11 (P.128)

$$
w_1' = w_1 - \eta \frac{\partial L}{\partial w_1}
$$

# 3-12 (P.128)

$$
w_2' = w_2 - \eta \frac{\partial L}{\partial w_2}
$$

# 3-13 (P.132)　
重みの更新


$$w_i' = w_i - \eta \frac{\partial L}{\partial w_i}$$

# 3-14 (P.132)
バイアスの更新
$$b' = b - \eta \frac{\partial L}{\partial b}$$

# 3-23 (P.137)
※付録の解説あり

$$
   \frac{\partial L_s}{\partial y_s} \frac{\partial y_s}{\partial u_s}  = y_s-t_s
$$

# 3-24 (P.138)

$$\frac{\partial L}{\partial w_i} = \frac{1}{N}\sum_{s=1}^{N} (y_s-t_s)x_{si}$$


# 3-25 (P.141)
損失関数をバイアスで偏微分

$$
\frac{\partial L}{\partial b} = \frac{1}{N}\sum_{s=1}^{N} (y_s-t_s)
$$


# 4-1 (P.186)
隠れ層j番目のニューロンの活性
$$
u_{sj}^{(h)} = \sum_{i=1}^{n} w_{ij}^{(h)} x_{si} + b_j^{(h)}
$$

# 4-2 (P.186)
隠れ層j番目のニューロンの出力
$$
y_{sj}^{(h)} = f(u_{sj}^{(h)})
$$

# 4-3 (P.187)
出力層のニューロンの活性
$$
u_s = \sum_{j=1}^{n_h} w_j y_{sj}^{(h)} + b
$$

# 4-4 (P.187)
出力層のニューロンの出力
$$
y_s = f(u_s)
$$

# 4-5 (P.189)
活性Uskの計算
$$
u_{sk} = \sum_{j=1}^{n_h} w_{kj} y_{sj}^{(h)} + b_k
$$

# 4-6 (P.192)
多クラスのソフトマックス関数
$$
y_{sk} = \frac{e^{u_{sk}}}{\sum_{m=1}^{n_o} e^{u_{sm}}}
$$

# 4-7 (P.200)

損失関数を重みで偏微分

$$
\frac{\partial L}{\partial w_j} = \frac{1}{N}\sum_{s=1}^{N} (y_s-t_s)y_{sj}^{(h)}
$$

# 4-8 (P.200)

重みの更新

$$
w_j' = w_j - \eta \frac{\partial L}{\partial w_j}
$$



# 4-9 (P.201)

$$
   \delta_s = \frac{\partial L_s}{\partial u_s} = \frac{\partial L_s}{\partial y_s} \frac{\partial y_s}{\partial u_s}  = y_s-t_s
$$

# 4-10 (P.202

$$
L = \frac{1}{N}\sum_{s=1}^{N} L_s
$$

# 4-11 (P.202)

$$
\frac{\partial L}{\partial w_j} = \frac{1}{N}\sum_{s=1}^{N} \delta_s y_{sj}^{(h)}
$$

という式に変換することができる。

この式は、重みwjの更新を行うための式である。

# 4-12 (P.203)
損失関数を重みで偏微分した式をチェーンルールで変換

$$
\frac{\partial L_s}{\partial w_{ji}^{(h)}} = \frac{\partial L_s}{\partial u_{sj}^{(h)}} \frac{\partial u_{sj}^{(h)}}{\partial w_{ji}^{(h)}}
$$

# 4-13 (P.204)

$$
\frac{\partial L_s}{\partial w_{ji}^{(h)}} = \delta_{sj}^{(h)} x_{si}
$$

# 4-14 (P.204)
4-13式に4-10式を合わせると

$$
\frac{\partial L_s}{\partial w_{ji}^{(h)}} =  \frac{1}{N}\sum_{s=1}^{N} \delta_{sj}^{(h)} x_{si}
$$

# 4-15 (P.204)
重みの更新式を示している。

$$
w_j' = w_j - \eta \frac{\partial L}{\partial w_j}
$$

# 4-16 (P.204)
隠れ層における誤差の計算

$$
\delta_{sj}^{(h)} = \frac{\partial L_s}{\partial u_{sj}^{(h)}} = \frac{\partial L_s}{\partial u_{s}} \frac{\partial u_{s}}{\partial y_{sj}^{(h)}} \frac{\partial y_{sj}^{(h)}}{\partial u_{sj}^{(h)}}
$$

# 4-17 (P.205)

$$
\delta_{sj}^{(h)} = \delta_s w_j f'(u_{sj}^{(h)})
$$

# 4-18 (P.211)
隠れ層のバイアス

$$
\frac{\partial L_s}{\partial b_j^{(h)}} =  \frac{1}{N}\sum_{s=1}^{N} \delta_{sj}^{(h)}
$$

# 4-19 (P.211)
4-15式を置き換え

$$
b_j' = b_j^{(h)} - \eta \frac{\partial L}{\partial b_j^{(h)}}
$$

# 4-20 (P.212)
多層ニューラルネットワークの学習  
損失関数としてクロスエントロピーを用いる

$$
L_s = \sum_{k=1}^{n_o} -t_{sk} \log y_{sk}
$$

# 4-21 (P.215)
多変数関数の合成関数の微分

$$
\frac{\partial L_s}{\partial w_{kj}} = \frac{\partial L_s}{\partial u_{sk}} \frac{\partial u_{sk}}{\partial w_{kj}}
$$

# 4-22 (P.215)

$$
\frac{\partial L_s}{\partial w_{kj}} = \delta_{sk} y_{sj}^{(h)}
$$

# 4-23 (P.215)

$$
\frac{\partial L_s}{\partial w_{kj}} = \frac{1}{N}\sum_{s=1}^{N} \delta_{sk} y_{sj}^{(h)}
$$

# 4-24 (P.216)

$$
w_{kj}' = w_{kj} - \eta \frac{\partial L}{\partial w_{kj}}
$$

$$
b_k' = b_k - \eta \frac{\partial L}{\partial b_k}
$$

# 4-25 (P.216)

$$
\delta_{sk} = \frac{\partial L_s}{\partial u_{sk}} = \sum_{m=1}^{n_o} \frac{\partial L_s}{\partial y_{sm}} \frac{\partial y_{sm}}{\partial u_{sk}}
$$

# 4-26 (P.217)
※付録PDF参照

$$
\delta_{sk} = y_{sk}-t_{sk}
$$

# 4-27 (P.218)

$$
\delta_{sj}^{(h)} = \frac{\partial L_s}{\partial u_{sj}^{(h)}} = \sum_{m=1}^{n_o} \frac{\partial L_s}{\partial u_{sm}} \frac{\partial u_{sm}}{\partial y_{sj}^{(h)}} \frac{\partial y_{sj}^{(h)}}{\partial u_{sj}^{(h)}}
$$

# 4-28 (P.218)

$$
\delta_{sj}^{(h)} = \sum_{m=1}^{n_o} \delta_{sm} w_{mj} f'(u_{sj}^{(h)})
$$