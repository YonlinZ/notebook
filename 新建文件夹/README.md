# notebook
# 概率函数$f(x;\theta)$
* 一族概率函数$\{f(x;\theta):\theta\in\Theta\}$，$\Theta$是参数空间
# 参数$\theta$的估计量$\eta$
* $\eta = u(\xi_1,...,\xi_n)$
* 估计量是统计量
* 估计值$y = u(x_1,...,x_n)$，其中$(x_1,...x_n)$是一组观测值
# 矩法估计
* 子样矩依概率收敛于母体矩
* 用子样矩代替母体矩
* 母体有概率函数$f(x;\theta_1,...,\theta_k)$，并且$k$阶矩为：$v_k=E\xi^k$
* 子样$\xi_1,\xi_2,...,\xi_n$的$j$阶矩：$\bar\xi_j = \frac 1 n\sum_{i=1}n\xi_i^j$
* 假设有$v_j(\theta_1,...,\theta_k)=\bar \xi^j,j = 1,...,k$
* 所有可以得到$\hat\theta_i=\hat\theta_i(\xi_1,...,\xi_k), i=1,...,k$
