# 5-1 (P.269)

$$
w' = w - \eta \frac{\partial L}{\partial w}
$$

# 5-2 (P.270)
Adamの定義

$$
m(t+1) = \beta_1 m(t) + (1-\beta_1) \frac{\partial L}{\partial w}
$$
$$   
v(t+1) = \beta_2 v(t) + (1-\beta_2) (\frac{\partial L}{\partial w})^2
$$
$$
\hat{m} = \frac{m(t+1)}{1-\beta_1^t}
$$
$$
\hat{v} = \frac{v(t+1)}{1-\beta_2^t}
$$
$$
w' = w - \eta \frac{\hat{m}}{\sqrt{\hat{v}}+\epsilon}
$$

# 5-3 (P.275)

$$
L = \frac{1}{N_b}\sum_{s=1}^{N_b} L_s
$$

# 5-4 (P.287)

$$
L + \frac{\alpha}{2}|\mathbf{w}|^2
$$

# 5-5 (P.287)

$$
L + \frac{\alpha}{2}(w_1^2 + w_2^2 + \cdots + w_i^2 + \cdots + w_n^2)
$$

# 5-6 (P.289)

$$
w_i' = w_i - \eta (\frac{\partial L}{\partial w_i} + \alpha w_i)
$$

# 5-7 (P.289)

$$
w_i' = (1-\eta\alpha)w_i - \eta \frac{\partial L}{\partial w_i}
$$

# 5-8 (P.293)

$$
\alpha |\mathbf{w}|^2
$$

# 5-9 (P.293)

$$
\frac{\alpha}{2N} |\mathbf{w}|^2
$$

# 6-1 (P.326)

$$
\delta_{sj}^{(h)} = \sum_{m=1}^{n_o} \delta_{sm} w_{mj} f'(u_{sj}^{(h)})
$$

# 6-2 (P.328)

$$
\frac{\partial L_s}{\partial w_{ji}^{(h)}} = \delta_{sj}^{(h)} x_{si}
$$

# 6-3 (P.329)

$$
\frac{\partial L_s}{\partial w} = \sum \delta_{sj}^{(h)} x_{si}
$$

