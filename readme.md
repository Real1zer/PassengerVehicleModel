> 这是一个车辆动力学模型库。

# 2DOF

> 简化原理：
>
> - 忽略转向系统的影响，直接以前轮转角作为输入；
> - 忽略悬架的作用，认为汽车车厢只做平行于地面的平面运动，即汽车沿z轴的位移，绕y轴的俯仰角和绕x轴的侧倾角均为零；
> - 汽车沿x轴的前进速度u视为不变；
> - 侧向加速度不超过0.4g，确保轮胎侧偏特性处于线性范围；
> - 驱动力不大（受力分析不考虑驱动力），不考虑地面切向力对轮胎侧偏特性的影响，不考虑空气阻力；
> - 忽略左右轮胎由于载荷变化而引起轮胎特性的变化以及轮胎回正力矩的作用。

## 固结于车辆坐标系下的运动方程

### 微分方程

$$
(k_{1}+k_{2})\beta  +\frac{1}{u} (ak_{1}-bk_{2})\omega _{r}-k_{1}\delta =m(\dot{v} +u\omega _{r})
\\
(ak_{1}-bk_{2})\beta +\frac{1}{u}(a^{2}k_{1}+b^{2}k_{2})\omega _{r}-ak_{1}\delta =I_{Z}\omega _{r}
$$

$$
\tag{2}

\begin{align}
mV\frac{\mathrm{d}\beta}{\mathrm{d}t}+2\left(K_{\mathrm{f}}+K_{\mathrm{r}}\right)\beta+\left[mV+\frac{2}{V}\left(l_{\mathrm{f}}K_{\mathrm{f}}-l_{\mathrm{r}}K_{\mathrm{r}}\right)\right]r &= 2K_{\mathrm{f}}\delta 
\\
2\left(l_{\mathrm{f}}K_{\mathrm{f}}-l_{\mathrm{r}}K_{\mathrm{r}}\right)\beta+I\frac{\mathrm{d}r}{\mathrm{d}t}+\frac{2\left(l_{\mathrm{f}}^{2}K_{\mathrm{f}}+l_{\mathrm{r}}^{2}K_{\mathrm{r}}\right)}{V}r &= 2l_{\mathrm{f}}K_{\mathrm{f}}\delta
\end{align}
$$

### 状态空间方程



## 地面固定坐标系下的运动方程

###  微分方程

$$
\tag{3}

\begin{align}m \frac{\mathrm{d}^2 y}{\mathrm{d} t^2} + \frac{2 (K_{\mathrm{f}} + K_{\mathrm{r}})}{V} \frac{\mathrm{d} y}{\mathrm{d} t} + \frac{2 (l_{\mathrm{f}} K_{\mathrm{f}} - l_{\mathrm{r}} K_{\mathrm{r}})}{V} \frac{\mathrm{d} \theta}{\mathrm{d} t} - 2 (K_{\mathrm{f}} + K_{\mathrm{r}}) \theta = 2 K_{\mathrm{f}} \delta
\\
2 \frac{(l_{\mathrm{f}} K_{\mathrm{f}} - l_{\mathrm{r}} K_{\mathrm{r}})}{V} \frac{\mathrm{d} y}{\mathrm{d} t} + I \frac{\mathrm{d}^2 \theta}{\mathrm{d} t^2} + \frac{2 (l_{\mathrm{f}}^2 K_{\mathrm{f}} + l_{\mathrm{r}}^2 K_{\mathrm{r}})}{V} \frac{\mathrm{d} \theta}{\mathrm{d} t} - 2 (l_{\mathrm{f}} K_{\mathrm{f}} - l_{\mathrm{r}} K_{\mathrm{r}}) \theta = 2 l_{\mathrm{f}} K_{\mathrm{f}} \delta\end{align}
$$







